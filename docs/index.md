# My Workflows

Over this contractual period, I contributed to **4 workflows** that are explained in a short overview, you can expand the same for a **detailed narrative** with appropriate **references** and links to documentation/code. 

## Report Generation {#report-generation}

When I first joined this company, it was because I wanted to be helpful to the entire process of constructing a neuromodulation device and leverage my expertise in psychology, neuroimaging and research to be an effective developer of this device's features.

What we figured was the most immediate fit was that the **EEG** part of the trifecta (**tDCS+CET+EEG**) is most underdeveloped—and as **Saakshi** asked in the very first meeting: given the raw EEG we obtain, how best to get something useful out of it?

Through many iterations we went from hand-typed reports (hemispheric symmetry, relative PSD plots; code-backed figures at **ANCIPS** with Dr Bannerjee) to today’s live stack: **`core_processing_pipeline.py`** and **`json_export.py`** (pre–post JSON for **Ashish**’s doctor-dashboard PDFs; single-session detail from the pipeline). We added an **HTML** explainer for sales, patients, and doctors, then a **JSON + React + CSS** repo to render and save versatile **PDFs** with traceable design and content.

??? note "Expand: full narrative and sources"
    --8<-- "includes/report-generation-long.md"

## Patents {#patents}

Analysis of Indian, international, and foreign patent law sharpened concepts such as **Freedom To Operate**: broad **method/system** claims (e.g. Flow, Soterix) fence the market, while narrower **device/application** claims (e.g. Swapnil, Boston Engineering) protect a niche. The **Oura** / **Ultrahuman** case showed how FTO plays out in practice—designing around prior art, and how patents can be used against similar products.

We pursue a **two-prong** strategy: a top-down **novel neuromodulation system** claim plus continuations that vary one axis at a time (monitoring, display/therapeutics, stimulation), with **closest patents** and **IPC** tracked for scope and limitations. Our **novel step**: **personalization** and **control policy** using data outside the immediate loop—therapy as a whole, not only detect-state → stimulate.

??? note "Expand: full narrative and sources"
    --8<-- "includes/patents-long.md"

## Clinical Success {#clinical-success}

I supported **Marbles Health** as a neuromodulation voice through proposals and evidence: **AIIMS NCAHT** stroke **tDCS** research; **Drs. Shabbari and Sridhar** (**C3/C4** motor rehab); license framing and **EASE** as a domestic alternative to imported devices. A **NIMHANS** abstract (Go/No-Go, Stroop ERPs) was selected but not pursued; a **systematic review** (50–60+ papers, risk-of-bias scoring, Neural Studies tables); **Safdarjung** protocol (**EEG+tDCS+CET**, at-home vs clinic, personalization later). I contributed **newsletter** case studies, a **brain stimulation / health gaps** article, a **tDCS + SSRI/SNRI** webinar, **ANCIPS** talks for **Dr Kavitha**, and **current-spread** notes for future hardware. **Next:** **DSIR**; new **CET** paradigm.

??? note "Expand: full narrative and sources"
    --8<-- "includes/clinical-long.md"

## Signal Quality {#signal-quality}

With **Swapnil** and **Lakshay**, we validated DSP on **ideal sinusoids** through our electrodes (including **220 kΩ vs 47 kΩ** contexts), then **rebuilt the pipeline** so DSP steps align to **known hardware** and additively improve **SNR**. The **signal quality** repo has filter/FFT tooling, optimization, and **`detect_sine.py`** verified on ideal waves; **hardware lab** test data grounds selection. **Next:** **ERP** and **artefact** protocols toward **journal-grade** reliability and publishable results.

??? note "Expand: full narrative and sources"
    --8<-- "includes/signal-long.md"
