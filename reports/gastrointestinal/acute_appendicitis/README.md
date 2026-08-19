# Acute Appendicitis — Complete RAG-Ready Clinical Corpus

**Pathology:** `Acute Appendicitis`  
**Category:** `Gastrointestinal`  
**Search Query:** `CONTAINS(BEFUND_ASCII_TEXT, '(acute & appendicitis) | (inflamed & appendix & stranding) | (appendicolith & appendicitis)') > 0`  
**Total Case Reports Extracted:** 80  
**Last Updated:** 2026-08-19 10:03:38  

---

## Modality Breakdown (RAG Dataset Files)

| Modality | Report Count | JSONL File (RAG Embeddings) | Markdown Reports File |
| :--- | :---: | :--- | :--- |
| **ULTRASOUND** | 56 | [`ultrasound.jsonl`](ultrasound.jsonl) | [`ultrasound_reports.md`](ultrasound_reports.md) |
| **CT** | 24 | [`ct.jsonl`](ct.jsonl) | [`ct_reports.md`](ct_reports.md) |
