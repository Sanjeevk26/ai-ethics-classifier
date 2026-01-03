# AI Ethics Case Studies (Memory Pack)

These case studies are designed as short “memory anchors” to help you remember and apply the four principles:
- **Privacy**
- **Transparency**
- **Accountability**
- **Fairness**

Each case includes:
1) **Scenario**  
2) **What’s at stake**  
3) **Which principle(s) apply**  
4) **What “good” looks like (actions + safeguards)**  

---

## Case Study 1 — The Support Chatbot That Stored Too Much
**Principle(s): Privacy + Accountability**

### Scenario  
A customer-support chatbot goes live. Users paste order IDs, phone numbers, addresses, and sometimes medical/financial details. Conversations are stored for “improvement,” but there is no clear opt-out, no retention policy, and no deletion workflow.

### What’s at stake  
- Sensitive data collected beyond what’s necessary  
- Weak consent boundary (users don’t realize storage and reuse)  
- No deletion/correction process  
- Higher risk of breaches, legal exposure, and reputational damage  

### What “good” looks like  
**Privacy**
- Data minimization (collect only what is required to resolve the issue)  
- Automatic PII redaction (mask phone/email/address patterns)  
- Clear notice (“avoid sharing sensitive information”)  
- Opt-out + retention policy + deletion workflow (“right to delete/update”)  

**Accountability**
- Named owners: data owner, model owner, product owner  
- Access controls and audit trails for stored conversations  
- Incident response playbook for AI-related data exposure  

---

## Case Study 2 — Web Scraping Without Permission
**Principle(s): Privacy + Transparency**

### Scenario  
A team scrapes user posts from a public forum to train an assistant. The forum’s terms prohibit scraping and users never consented to their posts being used for AI training.

### What’s at stake  
- “Publicly visible” does not automatically imply permission or consent  
- Terms-of-service violation + potential IP/copyright disputes  
- Loss of user trust and reputational harm  

### What “good” looks like  
**Privacy**
- Avoid collecting personal identifiers and sensitive attributes  
- Filter names, emails, locations, and minors’ data  
- Prefer licensed/open datasets or explicit partnerships  

**Transparency**
- Document sources and licensing terms  
- Maintain data provenance metadata (where/when/how acquired)  
- Provide clear disclosure of training data categories where appropriate  

---

## Case Study 3 — The Black-Box Loan Denial
**Principle(s): Transparency + Fairness**

### Scenario  
A bank uses an AI model to approve or deny loans. Customers receive a generic “declined” message. Internally, staff cannot explain the rationale. Complaints rise that applicants from certain regions are rejected more often.

### What’s at stake  
- High-impact decisions without explainability  
- Users cannot contest or correct inputs  
- Proxy features (ZIP/region) can silently introduce bias  

### What “good” looks like  
**Transparency**
- Provide understandable decision explanations (“reason codes”)  
- Maintain system documentation and model cards  
- Communicate limitations and confidence boundaries  

**Fairness**
- Measure performance across subgroups (not only overall accuracy)  
- Identify proxy variables and assess their impact  
- Monitor for fairness drift post-deployment  

---

## Case Study 4 — Hiring Screen That Reinforced Elite Bias
**Principle(s): Fairness + Accountability**

### Scenario  
A hiring screen model is trained on past employee resumes. Historically, the company hired heavily from a few elite colleges. The model learns those patterns and downranks equally capable candidates from other institutions.

### What’s at stake  
- Historical bias becomes automated policy  
- Opportunity loss for qualified candidates  
- Discrimination risk, brand damage, legal exposure  

### What “good” looks like  
**Fairness**
- Ensure representative coverage beyond past hiring outcomes  
- Measure subgroup error rates and selection rates  
- Mitigate bias via reweighting, balanced sampling, and proxy review  
- Human review for borderline or high-impact decisions  

**Accountability**
- “Go/no-go” release gates and red-teaming before launch  
- Documented ownership and escalation path for reported harms  
- Periodic audit schedule after deployment  

---

## Case Study 5 — Hospital Data Used Without Sufficient Transparency
**Principle(s): Privacy + Transparency + Accountability**

### Scenario  
A health-tech app partners with a hospital to detect risk of acute kidney injury. Large volumes of patient records are used. Patients were not clearly informed, and oversight controls were insufficient.

### What’s at stake  
- Use of sensitive health data without meaningful transparency  
- Weak governance over access and permissible use  
- Rapid collapse of public trust, regulatory risk  

### What “good” looks like  
**Privacy**
- Strong lawful basis and clear consent/notice strategy  
- De-identification, encryption, strict access control  
- Data minimization aligned to the clinical objective  

**Transparency**
- Plain-language patient communications  
- Clear explanation of purpose, retention, sharing, and limitations  

**Accountability**
- Defined responsibility: humans remain accountable for clinical decisions  
- Audit logs, change logs, incident response procedures  
- Formal oversight (ethics review, governance board)  

---

## Case Study 6 — Viral Deepfake and Public Confusion
**Principle(s): Transparency + Accountability**

### Scenario  
A realistic AI-generated image goes viral and is treated as real news. It is shared widely before verification and causes reputational harm and confusion.

### What’s at stake  
- Misinformation spreads faster than corrections  
- Trust erosion (“seeing is no longer believing”)  
- Pressure on platforms and creators to prevent abuse  

### What “good” looks like  
**Transparency**
- Provenance indicators/watermarking where feasible  
- Clear labeling for synthetic media in appropriate contexts  
- User education and verification pathways  

**Accountability**
- Reporting and takedown workflows  
- Incident response for misinformation events  
- Policy enforcement for repeat abuse and coordinated manipulation  

---

## Case Study 7 — Context Failure: Slang Misread as Fact
**Principle(s): Transparency + Accountability**

### Scenario  
A chatbot misinterprets slang (“throwing bricks”) literally and produces a false claim that vandalism occurred. The output is confident and gets shared.

### What’s at stake  
- Hallucinations or context errors presented as facts  
- Overconfidence increases harm and reduces trust  
- Risk escalates when outputs are redistributed as “news”  

### What “good” looks like  
**Transparency**
- Clear limitation messaging and uncertainty where appropriate  
- Avoid definitive claims without grounding in reliable sources  
- Encourage verification for sensitive or factual assertions  

**Accountability**
- Logging and monitoring to detect recurring failure modes  
- Human escalation for sensitive topics and reputational risk  
- Feedback loop: incidents → fixes → evaluation → redeploy  

---

## Case Study 8 — Voice Cloning Without Consent
**Principle(s): Privacy + Accountability + Consent/IP**

### Scenario  
A voice actor licensed recordings years ago. Later, a company trains a voice clone and uses it commercially. The actor discovers it when clients start choosing the AI version.

### What’s at stake  
- Consent is not future-proof if AI reuse wasn’t explicitly covered  
- Identity, ownership, and labor rights concerns  
- Unclear accountability across data owners, model builders, and deployers  

### What “good” looks like  
**Privacy + Consent**
- Explicit consent for voice cloning and derivative reuse  
- Clear opt-out, revocation, and contract updates as technology evolves  

**Accountability**
- Traceability: dataset provenance, licensing documentation, usage logs  
- Clear responsibility: who approved the model and where it is deployed  
- Enforcement mechanisms when misuse is detected  

---

## Case Study 9 — Fairness Drift After Deployment
**Principle(s): Fairness + Accountability**

### Scenario  
A model performs well at launch. Over time, user behavior and demographics change. The model begins performing worse for one subgroup, but the drift is unnoticed because only overall metrics are tracked.

### What’s at stake  
- Silent degradation creates unequal outcomes  
- Harm accumulates gradually, making it harder to detect and correct  
- Compliance and reputational risk increases over time  

### What “good” looks like  
**Fairness**
- Continuous subgroup monitoring (not just overall accuracy)  
- Regular fairness regression testing  
- Re-audits on schedule and after major data shifts  

**Accountability**
- Clear retraining triggers and rollback plans  
- On-call ownership for AI incidents  
- User reporting mechanisms and transparent incident handling  

---

## One-Page Memory Map

- **Privacy**: minimize data, pseudonymize/anonymize, consent, deletion workflows  
- **Transparency**: plain-language disclosures, explain decisions, model/system documentation  
- **Accountability**: named owners, audit trails, incident response, human oversight  
- **Fairness**: subgroup testing, proxy review, monitor drift, governance sign-off
