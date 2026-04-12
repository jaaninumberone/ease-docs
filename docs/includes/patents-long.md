**Expanded narrative.** The canonical numbered and public URL list is **[References](workflows/patents/references.md)**. Below is the mediating overview between the short executive narrative and raw research notes, with inline links. Replace **`YOUR_DOC_ID`** everywhere you paste real Google Doc IDs.

Deep-dive material for teammates with access lives in a **Google Doc** structured by section: [hub](https://docs.google.com/document/d/YOUR_DOC_ID/edit), [patent basics primer](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....), [FTO](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....), [Oura vs Ultrahuman](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....), [closest patents](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....), and [claims → limitations → design-around](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....). Public sources used while building this understanding include [Wikipedia](https://en.wikipedia.org/wiki/Category:Patent_search_services), [WIPO](https://www.wipo.int/edocs/mdocs/patent_policy/en/wipo_ip_bkk_11/wipo_ip_bkk_11_ref_topic14.pdf), [USITC notices](https://www.usitc.gov/secretary/fed_reg_notices/337/337_1478_notice01142026sgl.pdf), and patent PDFs linked from [References](workflows/patents/references.md).

---

## Executive framing

Reviewing **Indian, international, and foreign** patent practice helped the team align on a few recurring ideas. **[Freedom To Operate (FTO)](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....)** became a central theme: competitors often pursue **broad method and system claims** (for example in the neuromodulation space, filings associated with names such as **Flow** and **Soterix**) that can make it harder for others to commercialize similar devices without careful claim analysis. **Narrower** filings around **specific devices and applications** (including work attributed to colleagues such as **Swapnil** and organizations such as **Boston Scientific** in our notes) can strengthen a niche and interact differently with those broader fences.

**FTO** is not only “one patent at the system level.” It requires mapping **subsystems and components**—including parts you might buy from vendors—because infringement and design-around questions can attach to **partial** feature overlap. See the [FTO notes in Google Docs](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....) and the [WIPO background on FTO-style analysis](https://www.wipo.int/edocs/mdocs/patent_policy/en/wipo_ip_bkk_11/wipo_ip_bkk_11_ref_topic14.pdf).

Practical clarity came from following **consumer hardware litigation** as a teaching example: **Oura**’s actions against **Ultrahuman** (and others) illustrated how **broad claims** plus **doctrine-of-equivalents** style reasoning can support enforcement, and why **incremental hardware or app tweaks** may not establish a **non-obvious** distinction if the claim language still reads on the accused product. Follow the [Oura case study notes](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....), [USITC notice (PDF)](https://www.usitc.gov/secretary/fed_reg_notices/337/337_1478_notice01142026sgl.pdf), [related USITC notice](https://www.usitc.gov/secretary/fed_reg_notices/337/337_1468_notice12182025sgl.pdf), and representative patent PDFs ([US11868178](https://patentimages.storage.googleapis.com/59/39/c8/aca188e24d2b70/US11868178.pdf), [US12222759](https://patentimages.storage.googleapis.com/6b/25/0c/be6db7373c2de2/US12222759.pdf), [US12346159 B2](https://patentimages.storage.googleapis.com/e7/50/29/45606aac2076aa/US12346159B2.pdf), [US12353244 B2](https://patentimages.storage.googleapis.com/a4/32/18/0893bbd1014e75/US12353244B2.pdf)). Settlements (for example with **RingConn**) show how **commercial resolutions** carve out product surfaces (apps, accessories) even when patents remain contentious.

For **our** strategy, a **two-pronged** approach emerged:

1. **Top-down:** a broad filing that states a **novel neuromodulation system** (claims aligned to what we actually build and can support with embodiments).
2. **Continuations / parallel filings:** change **one** controlled axis at a time—**monitoring**, **interactive display / therapeutic techniques**, **stimulation**—so each application has a clear **delta** from the parent disclosure.

Parallel work includes **landscaping close patents**: scope and **limitations** of their claims, **IPC** classes, and explicit **design-around** notes. The table of “relevant patents” in our research (see [closest-patent analysis in Google Docs](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....) and landscape examples such as [US9339642](https://patents.justia.com/patent/9339642), [US12453854](https://patents.justia.com/patent/12453854), [US9511222](https://patents.google.com/patent/US9511222B2/en?q=(Transcranial+direct+current+stimulation)&assignee=Boston+Scientific+Neuromodulation+Corporation&peid=64a9dbccf5080%3A2da%3A43f3694b), [artifact-detection example PDF](https://patentimages.storage.googleapis.com/ac/c1/a7/36782d994c8b37/US20110224569A1.pdf)) contrasts **core idea**, **claim breadth**, **limitations**, and **where our architecture differs** (for example control-policy emphasis vs pure **state → trigger stimulation** loops).

**Substantive novelty (synthesis):** prior art often describes **closed-loop neuromodulation** as **detect state → trigger modulation**. Our direction emphasizes **personalization using data that can live outside the immediate biosignal loop**—patient characteristics, subjective inputs, and other context—so that **therapy** is chosen by an explicit **control policy** (decision logic), not only by a short-latency state classifier feeding stimulation. That distinction is the bridge from landscape analysis to **claim drafting** and **FTO**; see [claims and design-around notes](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....).

---

## Patent basics primer

Before FTO and landscaping work, the notes anchored on a small set of **main questions**: Is the device **patentable**? Are we **infringing** anyone in a given jurisdiction? How do we file so the **claims** match what we can **disclose** and **defend**? How do we **search** top-down (by assignee / competitor) vs bottom-up (by keywords and IPC)? Full notes: [Google Doc — patent basics primer](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....).

Core vocabulary included **specifications** (sufficiency of disclosure), **independent vs dependent claims**, the **International Patent Classification (IPC)** system, and the **[doctrine of equivalents](https://en.wikipedia.org/wiki/Doctrine_of_equivalents)** (function–way–result; **all-elements** style tests in US jurisprudence; see also [Cornell WEX](https://www.law.cornell.edu/wex/doctrine_of_equivalents)). Patent **families**—continuations, continuation-in-part, divisionals—explain why similar-looking documents differ in **claim scope** while sharing priority. Background: [patent (overview)](https://en.wikipedia.org/wiki/Patent), [patent claim](https://en.wikipedia.org/wiki/Patent_claim), [prior art](https://en.wikipedia.org/wiki/Prior_art), [certificate of contested validity](https://en.wikipedia.org/wiki/Certificate_of_contested_validity).

---

## Freedom To Operate (FTO)

FTO analysis asks whether a product feature-set is **covered by any enforceable claim** in relevant jurisdictions and periods. A recurring mistake is only searching **whole-system** patents. Subsystems (algorithms, UI flows, electrode control modes) need **their own** mapping because **partial overlap** can still matter for components and software. **[Working FTO notes (Google Doc)](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....)** · [WIPO PDF context](https://www.wipo.int/edocs/mdocs/patent_policy/en/wipo_ip_bkk_11/wipo_ip_bkk_11_ref_topic14.pdf)

---

## Oura vs Ultrahuman (case study)

The research narrative used **Oura**’s enforcement as a **case study**: complaints to the **USITC** (Section 337), arguments that competitor hardware and software features still fall within **broad claim language**, parallel litigation threads (including India), and **settlements** that exempt certain product areas. **[Case study notes (Google Doc)](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....)** · [USITC notice](https://www.usitc.gov/secretary/fed_reg_notices/337/337_1478_notice01142026sgl.pdf) · [USITC notice (related)](https://www.usitc.gov/secretary/fed_reg_notices/337/337_1468_notice12182025sgl.pdf) · patent PDFs on [References](workflows/patents/references.md) (items 11–14)

This is **not** legal advice; it is a **pattern language** for how **claim breadth** and **equivalence** interact with product differentiation.

---

## Analysis of closest patents

Landscape work listed **assignees** and **product areas** in non-invasive neuromodulation and related monitoring, then focused on a **matrix** of patents: **core idea**, **claim scope**, **limitations**, and **our design-around angle**. **[Closest-patent notes (Google Doc)](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....)** · [US9339642](https://patents.justia.com/patent/9339642) · [US12453854](https://patents.justia.com/patent/12453854)

Examples captured in the notes include:

| Patent (examples) | Core idea (summary) | Typical limitation called out in notes | Design-around direction (examples) |
|-------------------|---------------------|----------------------------------------|--------------------------------------|
| US9339642 | Multi-electrode stimulation + integrity / contact sensing | Hardware + sensing focus; not full adaptive-task coupling | Differentiate on **control / software policy** and task coupling |
| US12453854 | Biosignal stream → **signature** → modulate stimulation | Strong reliance on **state/signature** mapping | Emphasize **policy** and outcomes beyond a single signature label |
| US2015351655 | Implant-leaning closed loop: condition → stimulate | Event / condition triggers | Continuous optimization framing vs binary triggers |
| US10932688 | EEG + behavior + adaptation | Anchors to **neural targets** | Outcome-driven control vs fixed neural targets |
| US20190069796 | EEG-informed learning tasks | Weaker stimulation–task coupling | Explicit **coupled** task–stimulation law |
| US20230191130 | RL for stimulation | Stimulation-only optimization | Joint task + stimulation co-optimization |
| NeuroPace-style / seizure | Event detect → stimulate | Binary event loop | Avoid pure event binary; use continuous performance framing |

IPC codes collected for neuromodulation / EEG-related buckets appear in the raw notes (A61N, A61B families) for search strategy.

---

## Claims → limitations → design-around strategy

**Claims** set the legal boundary; **limitations** narrow or sharpen that boundary (preamble, transition phrases like *comprising*, element-by-element mapping). **Design-around** means changing the product or claim strategy so that **each element** of a relevant claim is **not** met—or so that your **novel** combination is **non-obvious** and **distinctly** supported in the specification. Readings: [patent claim](https://en.wikipedia.org/wiki/Patent_claim), [doctrine of equivalents](https://en.wikipedia.org/wiki/Doctrine_of_equivalents).

The **synthesis** section above is the intended **inventive step** story: move from “closed loop exists in prior art” to “**how** therapy is **personalized** and **decided** using richer inputs and an explicit **control policy**,” rather than only **detect state → stimulate**. **[Drafting / strategy notes (Google Doc)](https://docs.google.com/document/d/YOUR_DOC_ID/edit#heading=h....)**

---

## See also

- [References](workflows/patents/references.md) — full numbered list and repository line  
- [Research notes folder](research/patents/README.md) — optional placement for redacted long-form exports  
