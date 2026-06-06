# 🌍 Project Background — pediatric-support-g4

> For technical implementation details see [`TECHNICAL.md`](TECHNICAL.md).
> For project status and disclaimer see [`README.md`](README.md).

---

## 🎯 Project Vision

Healthcare is frequently delivered far from high-tech urban centres. Pediatric specialists in remote or resource-limited clinics often work without peer consultation, reference libraries, or reliable internet access.

This is an **independent applied research initiative** with the long-term goal of engineering a compliant, offline, zero-cost clinical decision support tool — a locally-running assistant that supports — but never replaces — the specialist's clinical judgment for tropical and endemic pediatric diseases, entirely on-device.

By eliminating any connection to external APIs or cloud infrastructure, patient data never leaves the clinical environment — removing third-party data processing, cross-border data transfer, and API logging from the workflow entirely. This is not a convenience feature; it is a data protection requirement in any clinical setting governed by patient data regulations.

This project is aligned with the **UN 2030 Agenda for Sustainable Development** [15], specifically:

- **SDG 3** (Good Health and Well-Being) — directly targeting SDG 3.2 (ending preventable deaths in children under five), SDG 3.3 (ending the epidemic of neglected tropical diseases), and SDG 3.8 (universal health coverage, including access to quality essential services).
- **SDG 10** (Reduced Inequalities) — addressing the healthcare access gap between remote, under-resourced communities and urban centres in low- and middle-income countries.
- **SDG 17** (Partnerships for the Goals) — built entirely on open-source infrastructure, open-weight models, and open datasets, contributing to the technology transfer and open knowledge principles that underpin SDG 17.

---

## 🌍 International Context

This project is grounded in a convergent body of evidence from international health institutions across three dimensions: the disease burden this project targets, the structural health workforce deficit in the region, and the institutional case for on-device AI as an appropriate technical and ethical response.

### The disease burden in the Americas

The Americas is facing an escalating tropical disease crisis with a disproportionate impact on children. In 2024, the region recorded the largest dengue epidemic since records began in 1980, with over 12.6 million cases — nearly three times more than in 2023 — including over 21,000 severe cases and more than 7,700 deaths [4]. The pediatric toll is acute: in Guatemala, 70% of dengue-related deaths occurred in children [4].

Beyond dengue, neglected tropical diseases including Chagas disease, leishmaniasis, trachoma, and rabies disproportionately affect the most vulnerable populations in the Americas, with communities in remote areas facing the greatest burden and the most inequitable access to essential medicines and diagnostics [5]. Leishmaniasis alone is endemic in 15 countries in the region, with its presence directly linked to poverty and the structural conditions of remote and rural communities [6]. Early diagnosis and timely access to treatment are identified by PAHO as critical — and currently unresolved — bottlenecks in disease elimination [5].

### Health workforce scarcity in the region

The clinical rationale for augmenting specialist judgment with AI decision support tools is grounded in a documented and worsening workforce deficit specific to the Americas. A PAHO report published in April 2025 found that 14 out of 39 countries in the region lack sufficient doctors, nurses, and midwives, with a projected deficit of between 600,000 and 2 million health workers by 2030 [7]. The distribution problem compounds the shortage: health workers are concentrated in capitals and large cities while rural and underserved areas face critical gaps [8]. In Bolivia, 73% of health personnel are concentrated in just three departments; in Peru, 85% are concentrated in urban areas alongside an estimated shortage of more than 54,000 health workers [8]. These are the precise clinical environments this project targets.

### On-device AI as a data protection requirement and technical response

The WHO's 2024 guidance on the ethics and governance of large multimodal models for health explicitly identifies data privacy as a primary risk of cloud-based LLMs in clinical contexts, issuing recommendations to governments and developers on responsible deployment [9]. The offline, on-device architecture of this project is a direct response: by keeping both model inference and patient data local, it eliminates the data exposure risks associated with cloud transmission entirely. This is a data protection requirement, not a design convenience.

This project is further aligned with the ICRC Handbook on Data Protection in Humanitarian Action (3rd edition, 2024) [16], a foundational reference on personal data protection law and its application to humanitarian organizations. The Handbook explicitly addresses data protection challenges arising from the use of AI and machine learning systems in the humanitarian sector, and establishes that data protection principles apply with particular force in exactly the settings this project targets — remote and underserved communities, in the most vulnerable circumstances. The on-device, offline architecture of this project is a direct implementation of the Handbook's core principle: that patient data must be protected by design, not merely by policy.

The technical feasibility of this approach for clinical applications is confirmed by recent research: a 2025 Stanford University benchmarking study of on-device LLMs for clinical reasoning found that deploying LLMs on smartphones is feasible for medical applications — enhancing privacy and eliminating cloud dependency — with compact models achieving a strong balance between speed and accuracy on everyday mobile hardware [3].

### Smartphone penetration and the offline deployment assumption

A critical feasibility question for any on-device clinical AI tool is whether the intended users — clinicians working in remote and underserved settings — actually have a smartphone capable of running it. GSMA data for Latin America supports this assumption, while also grounding the offline architecture in operational reality rather than just data protection principles.

Latin America has a 72% mobile subscriber penetration rate, and smartphone adoption continues to grow steadily across the region [12]. Critically, the end user of this tool is a trained clinical specialist — a population with smartphone ownership rates significantly above the regional average. The deployment assumption is not that every patient or community member in a remote area has a capable device; it is that the clinician does.

At the same time, GSMA data highlights two structural realities that directly reinforce the offline architecture. First, more than a third of mobile internet subscribers in Latin America and the Caribbean are still using 3G smartphones or feature phones [13] — a reminder that hardware capability is not uniform, and that the quantised mobile export planned for v0.4 must be optimised for the widest feasible range of devices. Second, the coverage gap affects 7% of the regional population — 44 million people — who lack mobile internet network access entirely, while a further 28% live in areas with nominal coverage they cannot reliably use [14]. In remote clinics, internet connectivity is intermittent at best. An offline, on-device architecture is therefore not only a data protection requirement — it is an operational necessity in the exact settings this project targets.

### Institutional alignment

This project is aligned with the Global Initiative on Artificial Intelligence for Health (GI-AI4H), established in 2023 by three UN specialised agencies — WHO, ITU, and WIPO — to develop technical standards and policy guidance for health AI and to advance ethical, equitable, and operational implementation, particularly in low- and middle-income countries [10]. The World Bank's Digital Progress and Trends Report 2025 further identifies affordable, on-device AI solutions designed to run on smartphones as the appropriate AI strategy for low- and middle-income countries where large-scale cloud infrastructure is not feasible [11].

---

## 📚 References

[1] Google DeepMind. *MedGemma.* Google Health AI Developer Foundations. https://developers.google.com/health-ai-developer-foundations/medgemma — Google Research and Google DeepMind. (2026). *MedGemma 1.5 Technical Report.* arXiv:2604.05081v2. https://arxiv.org/abs/2604.05081v2

[2] Google DeepMind. *Gemma 4 Model Card.* https://ai.google.dev/gemma/docs/core/model_card_4

[3] Nissen, L. et al. (2025). *Medicine on the Edge: Comparative Performance Analysis of On-Device LLMs for Clinical Reasoning.* Stanford University / University Hospital Bonn. arXiv:2502.08954. https://arxiv.org/abs/2502.08954

[4] PAHO. (2024, December 10). *PAHO highlights increase in dengue, Oropouche, and avian influenza cases in the Americas.* https://www.paho.org/en/news/10-12-2024-paho-highlights-increase-dengue-oropouche-and-avian-influenza-cases-americas-and

[5] PAHO. (2025, February 11). *Access to Critical Supplies for Neglected Diseases in the Americas.* https://www.paho.org/en/news/29-1-2025-access-critical-supplies-neglected-diseases-americas

[6] PAHO. *Leishmaniasis.* https://www.paho.org/en/topics/leishmaniasis

[7] PAHO. (2025, April 30). *New PAHO report reveals that 14 countries in the Americas face health worker shortages.* https://www.paho.org/en/news/30-4-2025-new-paho-report-reveals-14-countries-americas-face-health-worker-shortages

[8] PAHO. (2026, April 29). *Overview of the health labor market in nine South American countries.* As reported in: DevelopmentAid. https://www.developmentaid.org/news-stream/post/206605/paho-flags-critical-gaps-in-south-americas-health-workforce

[9] WHO. (2024). *Ethics and Governance of Artificial Intelligence for Health: Guidance on Large Multi-Modal Models.* https://www.who.int/publications/i/item/9789240084759

[10] Muralidharan, V. et al. (2025). *Global Initiative on AI for Health (GI-AI4H): strategic priorities advancing governance across the United Nations.* npj Digital Medicine, 8, 219. https://doi.org/10.1038/s41746-025-01618-x

[11] World Bank Group. (2025). *Digital Progress and Trends Report 2025: Strengthening AI Foundations.* https://www.worldbank.org/en/publication/dptr2025-ai-foundations

[12] GSMA. (2024). *The Mobile Economy Latin America 2024.* https://www.gsma.com/solutions-and-impact/connectivity-for-good/mobile-economy/latam-2024/

[13] GSMA. (2024). *State of Mobile Internet Connectivity 2024.* https://www.gsma.com/newsroom/press-release/new-gsma-report-shows-mobile-internet-connectivity-continues-to-grow-globally-but-barriers-for-3-45-billion-unconnected-people-remain/

[14] GSMA Intelligence. (2024). *Connectivity Gaps in Latin America.* https://www.gsma.com/about-us/regions/latin-america/connectivity-gaps-in-latin-america/

[15] United Nations. (2015). *The 17 Goals — 2030 Agenda for Sustainable Development.* https://sdgs.un.org/goals

[16] Marelli, M. (Ed.). (2024). *Handbook on Data Protection in Humanitarian Action* (3rd ed.). Cambridge University Press. ISBN: 9781009414654. https://doi.org/10.1017/9781009414630
