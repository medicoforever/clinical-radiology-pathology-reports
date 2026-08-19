# Clinical Radiology Pathology Reports — Master Multi-Modality RAG Database

A comprehensive, production-grade clinical radiology reports database extracted directly from **Centricity RIS-i (2.12M+ records)**. Structured specifically for **Medical RAG (Retrieval-Augmented Generation)**, Vector Embeddings (ChromaDB, Pinecone, FAISS, Weaviate), and Clinical LLM benchmarking.

---

## 🚀 Key Database Highlights
- **Total Verified Clinical Reports:** **3,372 Reports**
- **Total Unique Pathologies:** **61 Pathologies** across 8 Subspecialties
- **Strict Modality Segregation:** Every pathology has individual datasets per modality (`mri.jsonl`, `ct.jsonl`, `ultrasound.jsonl`, `xray.jsonl`, `pet_ct.jsonl`, `angiography.jsonl`).
- **Format:**
  - **`.jsonl`**: Machine-readable JSON records with structured metadata (`id`, `pathology`, `modality`, `modality_code`, `report_date`, `clinical_indication`, `findings`, `impression`, `full_report_text`).
  - **`_reports.md`**: Full human-readable markdown reports with clinical headings.
  - **`README.md`**: Pathology overview and modality distribution breakdown.

---

## 🩺 Subspecialties Overview

| Subspecialty | Pathologies Curated | Total Reports | Modalities Covered |
| :--- | :---: | :---: | :--- |
| **Neuroimaging & Brain** | 14 | **800** | MRI, CT, PET-CT, Angiography |
| **Head & Neck** | 8 | **445** | CT, MRI, Ultrasound, PET-CT, X-Ray |
| **Spine & Spinal Cord** | 7 | **420** | MRI, CT, X-Ray |
| **Thoracic & Pulmonary** | 8 | **499** | CT, HRCT, X-Ray, PET-CT, Ultrasound |
| **Gastrointestinal** | 6 | **380** | CT, Ultrasound, X-Ray, MR Enterography |
| **Hepatobiliary & Pancreatic** | 5 | **300** | Triple Phase CT, MRI, MRCP, Ultrasound |
| **Genitourinary & Pelvis** | 7 | **420** | CT Urography, MRI Pelvis, Ultrasound |
| **Musculoskeletal** | 6 | **347** | High-Res MRI, Digital Radiography, CT |
| **TOTAL** | **61** | **3,372** | **Full Spectrum Multi-Modality** |

---

## 🤖 RAG Integration Quickstart (Python)

```python
import json

# Load MRI reports for Diffuse Axonal Injury
with open("reports/neuroimaging/diffuse_axonal_injury/mri.jsonl", "r", encoding="utf-8") as f:
    mri_cases = [json.loads(line) for line in f]

print(f"Loaded {len(mri_cases)} MRI cases for DAI")
print("First Case Impression:", mri_cases[0]["impression"])
```

---

## 📂 Navigation Links
- [Master Taxonomy & Index](TAXONOMY.md)
- [Extraction Progress Dashboard](PROGRESS.md)
- [User Feedback Log](FEEDBACK.md)
