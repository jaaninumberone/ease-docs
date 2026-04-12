Canonical numbered list: **[References](workflows/reporting/references.md)**.

## Reporting and PDF generation

When Saakshi and I first met, the question posed was “how to get something useful” out of our EEG data, given the fact that

- a) we do not know anything about its accuracy and
- b) its constraints (4 channel data, in a csv format, at 250/500 hz, recorded with eyes open/closed at rest)

The first step was to set up a processing pipeline that could measure frequency power (most appropriate for time series data such as ours).

For a from-scratch problem (unknown hardware properties, few channel info, unique format), we had to build a from-scratch pipeline.

Existing pipelines such as HAPPE, EEGLab in Matlab, and MNE in Python etc. depended on assumptions about signal type and electrodes that did not apply to us, so using different libraries we constructed a sequence more suited for our data ([1](workflows/reporting/references.md#ref-1)).

This was posed with an assignment from Lakshay and Swapnil, where known generated waveforms were given in the same 4-channel CSV format and I was told to find out the composite waves ([2](workflows/reporting/references.md#ref-2)). I did this with SciPy’s FFT library ([3](workflows/reporting/references.md#ref-3)).

However, a direct Fourier transform does not help our use case, since high contact impedance, slow drift, physiological artefacts and electronic artefacts contaminate all the frequency bands and have to be removed.

See *waveform basics* ([4](workflows/reporting/references.md#ref-4)) for a full analysis of our use case, including scope and limitations of conventional EEG libraries.

So the first clinical report was made ([5](workflows/reporting/references.md#ref-5)), which focused on generating PSD values in a graph form, and also hemispherical symmetry of the detected wave frequencies and amplitudes. See references for building normative ranges for frontal presence of the frequency bands at Normative EEG Database ([6](workflows/reporting/references.md#ref-6)).

It then made certain inferences about symptom risks and cognitive indicators (for example, excessive theta+delta activity corresponding to poor cognitive control and frontal alpha asymmetry as a marker for withdrawal/avoidance).

This was made into a report that was consequently presented at ANCIPS by Debanjan Bannerjee.

Many reports were then handmade, as we found doctors like the feature and the delight factor. With every report, we refined the structure of reporting as well as the content, generating different visualizations and descriptions, which were iteratively refreshed and new ones brought in to replace the older ones.

Soon after, Lakshay requested an automated pipeline ([7](workflows/reporting/references.md#ref-7)) that could do end-to-end processing plus report generation from a single CSV, to be presented to investors in Bangalore. This was done in collaboration with Kiwimesh Illiyas and Atul, and we automated the process such that within a little more than 10 seconds the CSV could be processed and a report could be generated for the doctor dashboard.

This moved us onto ANCIPS, for which I decided to redesign the pipeline based on what I had learnt, namely:

1. The maximum contamination existed in the delta band and higher gamma bands, consistent with research on the use of few, frontal and dry electrodes.
2. Log-power alpha symmetry, specific ratios of relative PSD values, were far more reliable for our use case than individual power bands as a marker.
3. The relative deviation of an individual’s cognitive parameters over a period of time (score accumulates as there is more deviation and more number of epochs affected) could be a source of conditional logic for what high/low values of each cognitive parameter could indicate.

See EEG Basics → Cognitive Parameters ([8](workflows/reporting/references.md#ref-8)) for rationale of calculating reliable markers, and EEG Validation → frontal PSD ([9](workflows/reporting/references.md#ref-9)) for frontal-specific functions of frequency power bands. Additionally, see Cognitive Parameters ([10](workflows/reporting/references.md#ref-10)) and Conditional Logic ([11](workflows/reporting/references.md#ref-11)) for code implementation of the same.

This is what we presented at ANCIPS, along with a “multi-session” report that could show the difference in EEG markers between spaced sessions, which was my in-detail PDF-generating script focused on EEG processing ([12](workflows/reporting/references.md#ref-12), [13](workflows/reporting/references.md#ref-13)).

As of now, what exists as the production-current software are `core_processing_pipeline.py`, which has functions for loading the CSV data, calculating impedance, high-pass, low-pass and notch filtering, conducting artefact (eye blink and muscle movement) rejection using bipolar correlation between FP1 and FP2 based on MNE, and then finally Welch PSD.

That leads to cognitive parameters and their comparison generated by `json_export.py`, which calls these functions then outputs JSON lists which are used by Ashish to display in the report ([1](workflows/reporting/references.md#ref-1)).

The next concern was understandability, for patients, doctors and salespeople, such that they comprehend the reporting content and structure. Therefore **ease-eeg-manual** was made to launch a cohesive story about what is EEG, the power bands, the cognitive parameters, all the report sections with elaboration on what is the content, how to infer it, etc.

The HTML document was not in PDF format. An entire repo was set up to use JSON text (actual content), TypeScript for defining how JSON will be presented on React (mapping functions), CSS for styling (colour, page margins, etc.) and finally Vite dev, which mounts the JSON on a local server, launches the app to render and save the PDF. Now, using appropriate inputs for the content, document style and design, Cursor/Claude can make any PDF using this repo ([14](workflows/reporting/references.md#ref-14)).

### See also

- [Patents workflow](#patents)
- [Signal Quality](#signal-quality)
