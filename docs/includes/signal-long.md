**Expanded narrative.** Canonical links: **[References](workflows/signal-quality/references.md)** (repo paths, project docs, optional Google Docs).

## Motivation: ideal data first

With **Swapnil**, **Lakshay**, and the team, we asked how to **validate** digital signalling choices for EEG when comparing hardware contexts (e.g. **220 kΩ vs 47 kΩ** resistor paths). The conclusion was to run the processing stack on **sinusoidal tones** at known **frequency** and **Vpp**, recorded through the same **EEG electrodes** used in hardware work — so each stage is judged against **ground truth** before clinical noise dominates interpretation.

## Rebuild: DSP aligned to hardware

That enabled a **ground-up rebuild**: calibrate **DSP** modules to **known hardware properties** in a sequence of steps that **additively** improve **SNR** and reliability. Document the calibration story in [**SIGNAL_PROCESSING_NARRATIVE.md**](https://github.com/YOUR_ORG/signal-quality/blob/main/docs/Project%20Details/SIGNAL_PROCESSING_NARRATIVE.md) and the repo layout in [**PROJECT_MAP.md**](https://github.com/YOUR_ORG/signal-quality/blob/main/docs/Project%20Details/PROJECT_MAP.md) once the repo is public.

## What exists in-repo

The **Signal Quality** repository ([root](https://github.com/YOUR_ORG/signal-quality)) includes modules for **filter** design (types and parameters), **FFT**, **visualization**, **calibration**, and **testing**. **Optimization** scripts explore filter types, parameters, and **step order**, comparing outputs to reference test data (including **hardware lab** captures). After experiments, decisions were consolidated in **`detect_sine.py`**, verified to recover **frequency** and **amplitude** of ideal waves and reconstruct them in the **time domain**.

Optional working notes: [filter optimization experiments](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....); lab exports (*Signal Quality*.txt, *Filter Optimization Experiment*.txt) — add blob links in [References](workflows/signal-quality/references.md) when committed.

## Next: ERP and artefacts

**ERP** experiments (averaged trials with known peaks) and **artefact** protocols are next — to refine DSP toward **state-of-the-art** reliability and a **journal-ready** narrative.

### See also

- [Report Generation](#report-generation) — downstream use of processed EEG
