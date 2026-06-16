# Parse Quality Report

Generated: 2026-06-16 02:34:58  
Corpus: `tests/data/resume/`  
LLM: **disabled** (deterministic tier-1 only)

**9 pass · 2 xfail (expected weak) · 0 fail · 1 error** / 12 total

---

## Per-file results

| File | Status | Name | Exp | Experiences (title @ company) | Skills | Top Skills | Edu | Links | Notes |
|------|--------|------|-----|-------------------------------|--------|------------|-----|-------|-------|
| Image Scanned Resume.pdf | ⚠️ error | — | 0 | — | 0 | — | 0 | — | scanned PDF — needs OCR (disabled in deterministic gate) |
| Likhitha_Data Scientist.docx | 🟡 xfail | SAI LIKHITHA ANUMULA | 1 | PROJECT: Intelligent Insurance Analytics & Risk Management Platform @ ? | 106 | natural language processing, collaborative filtering, azure data factory, prompt engineering, sentiment analysis, gradient boosting, survival analysis, chain-of-thought … +98 | 2 | linkedin: https://www.linkedin.com/in/sailikhitha543672/ | tier-1 drops title/company; LLM-rescued in prod |
| Nikhila_M_DS_Resume.docx | ✅ pass | Nikhila Reddy Mannem | 3 | Data Scientist @ Generative AI; Data Scientist @ Machine Learning; Associate Data Scientist @ Client: Elevance Health (Anthem) | 54 | hyperparameter tuning, logistic regression, feature engineering, prompt engineering, sentiment analysis, chain-of-thought, classification, decision trees … +46 | 2 | linkedin: http://www.linkedin.com/in/nikhila-m-980s734/ |  |
| Pavan_Kumar_UX-Designer_Resume.pdf | ✅ pass | Donthula Pavan Kumar | 2 | UX Designer @ Progrowth Technologies Inc; UX Designer @ Careerpedia | 23 | a/b testing, .net, UX Research, User Flows, Wireframing, UI Design, Prototyping, Visual Design … +15 | 1 | linkedin: https://www.linkedin.com/in/uxpavan/ |  |
| Prasanna_Resume.docx.pdf | ✅ pass | LAKSHMI PRASANNA | 3 | Generative AI Engineer (Senior Data Scientist) @ Huntington Bank; Data Scientist @ Liberty Mutual; Associate Data Scientist (Python Developer) @ Kroger | 101 | python, git, kafka, causal inference, nlp, azure ml, aws redshift, computer vision … +93 | 2 | linkedin: https://www.linkedin.com/in/lakshmi-prasanna-1a7a54146/ |  |
| RaviReddy_RESUME.docx | ✅ pass | RAVI REDDY | 3 | Software Engineer (Java Full Stack)USA @ Bank of America; Software Developer (Java Full Stack)                                                                                                                                 India @ Elevance Health; Junior Software Developer                                                                                                                                              India @ Johnson & Johnson | 49 | github actions, restful apis, blob storage, api gateway, spring boot, material ui, cloudwatch, postgresql … +41 | 2 | linkedin: https://www.linkedin.com/in/ravi-reddyrr/ |  |
| Resume.pdf | ✅ pass | KOPPARTHI VAMSI | 3 | Full Stack AI Engineer (GEN AI/LLMS) @ ; Software Engineer, Backend & Cloud @ ; Software Engineer, Data & Backend @  | 105 | prompt engineering, agentic workflows, github actions, cloudformation, restful apis, tailwind css, blob storage, api gateway … +97 | 1 | linkedin: https://www.linkedin.com/in/vamsi-kopparthi-51a6a51b5/ |  |
| RuthikshaReddy Data Analyst.docx | ✅ pass |  | 3 | Data Analyst @ Huntington Nation Bank; Data Analyst @ Apollo Hospitals; Associate Data Analyst @ Aditya Birla Sun Life Insurance | 62 | anomaly detection, elasticsearch, scikit-learn, transformers, postgresql, tensorflow, kubernetes, sagemaker … +54 | 0 | linkedin: http://www.linkedin.com/in/ruthiksha-reddy-505724261 |  |
| Srinitya_Resume.docx | ✅ pass | SRINITYA BYRI | 4 | JP MORGAN CHASE @ Generative AI-Driven Banking Intelligence Platform; JOHNSON & JOHNSON @ Predictive Analytics & Patient Risk Stratification System; EBAY @ Customer Behavior Analytics Platform; AIG (AMERICAN INTERNATIONAL GROUP) @ Enterprise Claims Analytics & Loss Forecasting Platform | 100 | hyperparameter tuning, logistic regression, feature engineering, github actions, random forest, azure openai, scikit-learn, transformers … +92 | 1 | — |  |
| Sushanth Kodipyaka Software Engineer (2).docx | ✅ pass | Sushanth Kodipyaka | 2 | Software Engineer @ JPMorgan Chase; Full Stack Developer @ Cognizant – India | 93 | github actions, elasticsearch, restful apis, spring boot, postgresql, typescript, javascript, confluence … +85 | 1 | linkedin: https://www.linkedin.com/in/sushanth-kodipyaka-69a933329?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3B%2F%2B9JuRvqRyWZQzdMsrJ2Mw%3D%3D |  |
| Test_Prasanna_Resume.docx | ✅ pass | LAKSHMI PRASANNA | 4 | Generative AI Engineer (Senior Data Scientist) @ Huntington Bank; Machine Learning Engineer (Data Scientist) @ UnitedHealth Group; Data Scientist @ Liberty Mutual; Associate Data Scientist (Python Developer) @ Kroger | 91 | python, git, kafka, causal inference, nlp, azure ml, aws redshift, computer vision … +83 | 2 | linkedin: https://www.linkedin.com/in/lakshmi-prasanna-1a7a54146/ |  |
| sandeep resume.docx | 🟡 xfail | Mohanthi Sandeep Addanki | 3 | Role: GenAI Engineer @ ?; Role: Machine Learning Engineer (Data Scientist) @ ?; Role: Associate Data Scientist @ ? | 81 | feature engineering, gradient boosting, classification, github actions, azure openai, scikit-learn, transformers, clustering … +73 | 3 | linkedin: https://www.linkedin.com/in/amohanthi01a69429b/ | tier-1 drops title/company; LLM-rescued in prod |

---

## How to update

```bash
# from services/ai/
venv/bin/python tests/golden/generate_report.py
git diff tests/golden/README.md   # see what changed
```

> **xfail** rows are resumes where tier-1 alone cannot parse cleanly.
> In production the LLM fallback rescues them. They are expected to fail this gate.
