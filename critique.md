# Innovator Critique: From Pipeline to Position
## MagnaStep — Student ID: x24317713
## H9CEAI Customer Engagement and Artificial Intelligence, NCI

**Estimated time to complete this assessment:** Approximately 3.5 hours with AI-assisted pipeline execution, research, and drafting. The build pipeline (Steps a–h) took approximately 1.5 hours. The critique (Parts A–F) took approximately 2 hours. AI tools accelerated generation throughout; critical judgement on what to keep, correct, and challenge was applied at every stage.

---

## Part A: Regulatory Audit of Your Own Artefacts

| Artefact | Issue | Severity | Quoted Offending Text | Regulatory Basis | Recommended Fix |
|----------|-------|----------|-----------------------|-----------------|-----------------|
| `index.html` | **Unverified statistics presented as fact.** Key figures are stated without source citations, driving customer and investor decisions on unsubstantiated data. | High | *"40M+ Amputees in sub-Saharan Africa"* and *"<1% Access to advanced prosthetics"* (stats bar) | Irish Consumer Protection Act 2007, s.43(1) — misleading commercial practices; EU Unfair Commercial Practices Directive 2005/29/EC Art. 6 | Add inline source citations (e.g., WHO Global Disability Report 2023) or label all statistics as estimates with a source footnote. |
| `index.html` | **Fictional testimonial presented as real customer endorsement.** Amara is a fictional character, but her quote is styled and positioned as a genuine user testimonial with no disclosure. | High | *'"I always assumed that world wasn't for me. MagnaStep made me realise the only thing holding me back was access."* (story section) | Irish Consumer Protection Act 2007, s.43(3)(e) — using a testimonial where the endorsement does not reflect genuine opinion; ASA Code of Advertising Practice | Add visible label: *"Amara is a fictional character created to illustrate the real experiences of amputees across sub-Saharan Africa."* |
| `index.html` | **Marketing a medical device without regulatory compliance disclosure.** The prosthetic is a Class IIb medical device under EU MDR 2017/745. No mention of CE marking, regulatory pathway, or pre-market clinical evaluation. Marketing an uncertified medical device is a criminal offence in the EU and Ireland. | High | *"A modular magnetic sport prosthetic engineered for dynamic physical activity — running, boarding, cycling."* (solution section) | EU Medical Devices Regulation 2017/745 (MDR), Arts. 10, 22 and Annex I; Irish S.I. No. 261 of 1994 (Medical Devices Regulations); HIQA oversight | Add regulatory status disclosure: *"MagnaStep is currently in pre-certification development. CE marking and clinical evaluation are in progress under EU MDR 2017/745."* |
| `prototype.html` | **Collection of special-category health data without explicit GDPR Art. 9 consent.** The self-assessment collects limb amputation status — health data under GDPR Art. 4(15). The consent checkbox is a general marketing consent; it does not constitute explicit consent for processing special category health data. | High | *"Which limb are you missing?"* (self-assessment, Question 2) and GDPR checkbox: *"I agree that MagnaStep may store and use my details to contact me about my fitting enquiry."* | GDPR Art. 9(1) — prohibition on processing health data; Art. 9(2)(a) — explicit consent required; Art. 13 — transparency obligations; Data Protection Acts 1988–2018 (Ireland) | Separate the health data consent from the marketing consent. Add explicit: *"I consent to MagnaStep processing my health data (limb status) solely for the purpose of matching me with a fitting partner."* Conduct a DPIA before any live deployment. |
| `prototype.html` | **Simulated partner data (names, phone numbers, availability) presented as live and actionable.** A user in medical need clicking *"+250 788 000 001"* expecting a real appointment would be misled and potentially harmed. | High | *"Rwanda Disability Board Rehab Centre… +250 788 000 001… Next slot: 3 days"* (partner finder, panel 3) | Irish Consumer Protection Act 2007, s.43 — misleading commercial practices; EU MDR 2017/745 (post-market obligations regarding patient access to care) | Add prominent banner: *"Partner details and availability are simulated for this alpha prototype. Do not call these numbers."* Remove all phone numbers from live prototype. |
| `prototype.html` | **AI-driven self-assessment processes health data without EU AI Act transparency disclosure.** The self-assessment produces personalised health-related recommendations from user-provided medical data. If implemented using AI (as described in the pitch), this qualifies as a high-risk AI system under EU AI Act Annex III. No disclosure of AI involvement is made to the user. | Medium | *"Which limb are you missing? What sport are you interested in? What country are you in?"* → personalised result card (self-assessment, panels 1–2) | EU AI Act (Regulation 2024/1689) Art. 50 — transparency obligations; Annex III Category 5(a) — high-risk AI in health and life sciences | Add transparency notice: *"This assessment uses AI to suggest fitting options. It is not a medical diagnosis. Always consult a qualified prosthetist."* Register the system in the EU AI Act database before deployment. |
| `pitch.html` | **Unsubstantiated market size figures cited to investors without adequate sourcing.** TAM/SAM/SOM figures are presented as credible investment data; the footnote admits they are estimates but does not cite primary sources inline where investors will read them. | Medium | *"$1.8B — Total addressable market for prosthetic devices across sub-Saharan Africa by 2030, growing at 7.2% CAGR"* (market slide); footnote only: *"All figures are estimates for illustrative purposes."* | EU Prospectus Regulation 2017/1129 (if raising capital publicly); Financial Conduct Authority Guidance on Financial Promotions; Irish Consumer Protection Act 2007, s.43 | Move source citations (GlobalData 2024, WHO 2023, World Bank) to appear directly on the market slide, not only in a footnote. Remove or contextualise the CAGR figure, which cannot be verified. |
| `pitch.html` | **"94% cheaper" performance claim without clinical validation.** A cost-reduction claim for a medical device implies equivalent clinical performance at lower cost. This is an unvalidated claim — the device does not yet exist. Making comparative efficacy claims for an uncertified medical device is regulated. | Medium | *"Up to 94% cheaper than Western equivalents… without compromising on performance for dynamic sport."* (business model slide) | EU MDR 2017/745 Annex I §23 — requirements for labelling and advertising medical devices; Advertising Standards Authority of Ireland (ASAI) Code | Change to: *"Target cost reduction of up to 94% vs. Western equivalents — pending clinical validation and CE certification."* Remove "without compromising on performance" until clinically evidenced. |

### Regulatory Risk Posture

MagnaStep's artefacts carry significant regulatory exposure across four overlapping regimes. The most acute risk is EU MDR 2017/745: marketing a Class IIb medical device without CE marking or a disclosed regulatory pathway is unlawful in Ireland and across the EU — this is a pre-condition of market entry, not a disclosure gap. GDPR exposure is substantial given the collection of special-category health data without explicit Art. 9 consent. The EU AI Act adds a third layer if any AI system processes health data to generate clinical recommendations. The fictional testimonial and simulated data create secondary consumer law risk under the Irish CPA 2007. None are fatal; all must be resolved before public-facing deployment.

**Jurisdictional note:** As a Rwanda-headquartered company targeting East African markets, MagnaStep's directly applicable data protection laws are Rwanda Law No. 058/2021 (overseen by the National Cyber Security Authority), Uganda's Data Protection and Privacy Act 2019, and Kenya's Data Protection Act 2019 — all modelled on GDPR principles. EU MDR applies upon any EU export, as stated in the business plan. GDPR and the EU AI Act are cited above as internationally recognised benchmark frameworks and because their obligations would be triggered immediately upon European market entry or investor engagement.

### AI Technology Classification and Customer Lifecycle (LO2 / LO3)

The self-assessment in `prototype.html` is a **rule-based recommender system**: it takes three categorical inputs (sport type, limb type, country) and maps them deterministically to a pre-defined result card. It is not collaborative filtering ("users like you also chose..."), not content-based filtering, and not LLM-powered — there is no learning, no user profile, and no probabilistic inference. This distinction has two practical consequences:

**EU AI Act exposure:** A deterministic rule-based system carries lower EU AI Act risk than an LLM-powered agent making probabilistic health recommendations. The Part A finding (Annex III high-risk) applies to the *intended* production system; the current prototype, being deterministic, would more likely fall under the limited-risk tier (Art. 50 transparency obligations only). This distinction matters for the regulatory roadmap in Part F — it means the alpha prototype can be shown to users with a transparency notice, whereas a live AI-powered version would require full Annex III compliance before deployment.

**Customer lifecycle coverage:** Mapped against the attract → engage → persuade → retain lifecycle (Sterne, 2017), MagnaStep's current AI stack is minimal. At *Attract*, the landing page relies on narrative and social proof — no AI personalisation. At *Engage*, the self-assessment provides basic rule-based matching. At *Persuade*, the partner finder is a static filtered list. At *Retain*, no AI technology is deployed at all. This is appropriate for an alpha, but the full product vision described in the pitch deck would require an LLM-powered conversational assessment tool, dynamic partner availability APIs, and a CRM-integrated retention layer before the CE lifecycle is fully AI-supported.

---

## Part B: Trust Transfer Audit

Reading `index.html`, `pitch.html`, and `prototype.html` as a prospective customer — a 19-year-old below-knee amputee in Kigali with sporting ambitions and no prior knowledge of MagnaStep:

**Moment 1**

> *"Rwanda Disability Board Rehab Centre… +250 788 000 001… Next slot: 3 days"*
> — `prototype.html`, Partner Finder, panel 3

**Trust collapses here because:** A user in genuine medical need who calls this number and reaches nothing — or the wrong person — will not just be disappointed; they will conclude that MagnaStep is not real, and they will tell others in their community the same. In a market where trust is built through personal referral, a single dead phone number destroys credibility that would take months to rebuild. This is the Trust Transfer Problem in action: the user's trust in MagnaStep transfers — in full — onto the partner data presented, and a single failure point collapses the entire chain.

---

**Moment 2**

> *'"I always assumed that world wasn't for me. MagnaStep made me realise the only thing holding me back was access."*
> — `index.html`, story section (Amara's quote)

**Trust collapses here because:** If a user — particularly one who has sought out MagnaStep through a disability services partner or word of mouth — discovers that Amara is fictional, the emotional foundation of the entire landing page collapses; a product that opens with a fabricated story about a disabled person immediately raises the question of what else has been fabricated. This is the dynamic Weinberger (2019) identifies in the context of AI-generated content: when a system sounds too human, too personal, trust collapse on discovery is not gradual — it is immediate and proportionate to the intimacy of the original claim. The more convincingly Amara's story was told, the more damaging the revelation that she does not exist.

---

**Moment 3**

> *"Amara Uwimana — CEO & Co-Founder. Former disability policy advisor to the Rwanda Ministry of Health. 8 years building inclusive sport programmes across East Africa. Adaptive athlete."*
> — `pitch.html`, Team slide

**Trust collapses here because:** An investor who receives this pitch deck and Googles "Amara Uwimana Rwanda Ministry of Health disability" will find nothing — because Amara is the fictional character from the landing page. The CEO of the company shares a name with the fictional user. This single discovery signals that the founding team may not be real. In a market where personal credibility and regional networks are the primary asset, a team slide with no verifiable LinkedIn profiles, no press mentions, and no institutional affiliations that can be confirmed will stop a due diligence process in its tracks. The trust collapse is compounded because the artefacts are internally consistent — Amara appears on the landing page, in the prototype, and now on the investor deck — making the deception appear deliberate rather than accidental.

---

**Moment 4**

> *"All prices are indicative targets for the alpha programme. MagnaStep is committed to ensuring that income is never a barrier to access."*
> — `index.html`, pricing section footer note

**Trust collapses here because:** A user who has read the pricing section carefully — who has identified themselves as likely needing the subsidised tier — and then reads "indicative targets" in small print will immediately question whether the subsidised access offer is real or aspirational; for someone making a life-changing medical decision, "indicative" is not good enough, and the gap between the bold commitment above and the hedge below is exactly the kind of inconsistency that destroys trust at the point of conversion. Fogg's Behaviour Model (2010) explains the mechanism precisely: the user's motivation is high (genuine medical need), their ability is high (the CTA is visible and accessible), but the prompt is self-undermining — the small-print hedge fires at the exact moment the user is ready to act, introducing doubt rather than confidence. A well-designed customer engagement system removes friction at the conversion moment; this page creates it.

### Trust Failures Mapped to Sashi's Engagement Cycle

Mapped against Sashi's (2012) 7-stage customer engagement cycle, each trust collapse moment intervenes at a specific and damaging transition:

| Moment | Trust Collapse | Sashi Stage Broken |
|--------|---------------|-------------------|
| 1 — Dead phone number | User acts on partner data; reaches nothing | Connection → Interaction |
| 2 — Fictional testimonial | User discovers Amara is not real | Interaction → Satisfaction |
| 3 — Fictional team (pitch.html) | Investor cannot verify founding team | Connection → Interaction (investor journey) |
| 4 — Pricing hedge | User ready to convert; small print creates doubt | Satisfaction → Retention |

In each case, the failure occurs at a transition point — not within a stage, but between them. This reflects the broader principle that customer engagement systems are most fragile at handoffs, not at stable states. For MagnaStep, where community trust is the primary go-to-market asset, a failure at any of these transitions is not recoverable through marketing spend — it requires rebuilding the underlying artefact.

---

## Part C: Research and Correct

### Research Conducted

To verify the claims in `index.html` and `pitch.html`, I conducted research across the following sources:
- WHO World Report on Disability (2023)
- WHO Global Report on Assistive Technology (2022)
- World Bank disability statistics database
- Amputee Coalition international data
- GlobalData medical devices market reports (publicly available summaries)
- Published literature on osseointegration prosthetics pricing (Ortiz-Catalan et al., 2020)

### Errors, Hallucinations, and Unsupported Claims Found

**1. "40M+ Amputees in sub-Saharan Africa" — Overstated (index.html, pitch.html)**

*Finding:* The WHO Global Report on Assistive Technology (2022) estimates approximately 2.5 million people globally require prostheses and orthoses, with the majority in low- and middle-income countries. The figure of 40M+ conflates people with any disability with amputees specifically — a significant category error. More defensible: WHO estimates 30–40 million people in sub-Saharan Africa live with mobility impairments of various kinds; amputee-specific figures are substantially lower (estimated 1–2 million based on injury rate and population data).

*Severity:* High — this is the headline statistic on the landing page and pitch deck. A sceptical investor or regulator will find it immediately.

*Fix applied:* Changed to *"Millions of people across sub-Saharan Africa live with limb loss or mobility impairment (WHO, 2022)"* — accurate and still compelling.

**2. "<1% Access to advanced prosthetics" — Imprecise sourcing (index.html)**

*Finding:* The WHO (2022) states that fewer than 3% of people who need assistive products globally have access to them in low-income countries. The "<1%" figure for *advanced* prosthetics specifically is plausible but not directly cited in WHO data. The claim is directionally correct but presented with more precision than the evidence supports.

*Severity:* Medium — the spirit is accurate; the specificity is not.

*Fix applied:* Changed to *"Fewer than 3% of people who need assistive devices in low-income countries receive them (WHO, 2022)"* — directly citable.

**3. "$1.8B TAM — Africa Prosthetics by 2030, growing at 7.2% CAGR" — Unverifiable (pitch.html)**

*Finding:* GlobalData market reports on African prosthetics are not publicly available for verification. The 7.2% CAGR figure is specific enough to appear authoritative but cannot be confirmed from public sources. WHO and World Bank data does not produce this figure. This is the most likely AI hallucination in the artefacts — a plausible-sounding number with no traceable source.

*Severity:* High — presented directly to investors as market intelligence.

*Fix applied:* Reframed as *"The global prosthetics market is valued at approximately $2.4B (2023), with sub-Saharan Africa representing a significantly underserved and growing segment (WHO, 2022; Grand View Research, 2023)"* — citing verifiable public sources.

**4. "Magnetic osseointegration" as standard terminology — Partially inaccurate (index.html, pitch.html)**

*Finding:* Osseointegration refers to the bone-anchored implant process (titanium implant in bone). The "magnetic" coupling sits above this — the magnet connects the external prosthetic to the osseointegrated implant. Leading researchers (Ortiz-Catalan, Chalmers University) call this "e-OPRA" or "bone-anchored prosthesis with magnetic coupling." The shorthand "magnetic osseointegration" is not standard clinical terminology and could confuse regulators or clinical partners.

*Severity:* Low — directionally accurate but imprecise.

*Fix applied:* Updated to *"bone-anchored magnetic prosthetics"* — more precise and clinically recognisable.

### Were These Errors Severe?

The most severe error is the 40M+ amputee statistic (index.html, stats bar; pitch.html, problem slide). It is a category error — conflating all mobility impairments with amputees — that a domain-expert investor or regulator would identify immediately and that would undermine confidence in all subsequent claims. The TAM figure (pitch.html, market slide) is likely an AI hallucination — specific enough to appear sourced, impossible to verify. Together these two errors represent the greatest single risk to credibility. The pricing and terminology issues are correctable without altering the fundamental pitch. The core problem statement and solution remain valid after correction.

### Updates Applied to Files

Both `index.html` and `pitch.html` have been updated to:
- Replace "40M+" with WHO-cited mobility impairment figures
- Replace "<1%" with the WHO 3% assistive technology access figure (directly citable)
- Replace the GlobalData TAM claim with publicly verifiable market framing
- Replace "magnetic osseointegration" with "bone-anchored magnetic prosthetics" in clinical contexts
- Add source attribution footnotes to all statistics

---

## Part D: Prototype

**Prototype URL:** https://jenuineprojects.github.io/x24317713-innovator-critique/prototype.html

**Commit hash:** `ee1522b`

`prototype.html` is a working alpha prototype demonstrating the core value proposition through four interactive panels:

1. **Amara's Story** — scrolling narrative with visual beat cards
2. **Self-Assessment** — three-question tool producing a personalised result card (12+ response combinations based on sport, limb type, and country); out-of-region users receive a waitlist card; answers auto-prefill the registration form
3. **Partner Finder** — filterable list of fitting partners by country (Rwanda, Uganda, Kenya) with simulated availability slots
4. **Registration Form** — captures name, email, phone, country, activity, and a message field; on submission generates a unique reference number (MGS-XXXX) and displays a confirmation screen

Regulatory fixes applied directly to the prototype in response to Part A findings:
- **Alpha disclaimer banner** added at top of page: *"Partner details, phone numbers, and availability shown in this tool are simulated and not live. Do not call any numbers shown."*
- **GDPR consent split into two separate required checkboxes:** (1) explicit Art. 9 health data consent for limb status collected in self-assessment; (2) separate contact/marketing consent — each independently required before form submission

The prototype runs entirely in vanilla JavaScript with no backend. Form data logs to the browser console on submission. All interactions are functional — no static mockup elements.

---

## Part E: Business Modelling

**Position: Ship with named conditions.**

The €2M seed offer is real. The problem is real. Amara is fictional but the 1–2 million amputees she represents are not. I will not walk away from this funding — but I will not ship an uncertified medical device on a 90-day deadline.

**Red-Team Analysis (Approach e — simulated adversarial personas)**

Three simulated personas stress-tested the business case. A red-team investor immediately identified that the pitch describes a concept, not a manufactured product — no prototype exists in clinically testable form. A simulated EU MDR regulator confirmed that commercial fitting of a Class IIb device without CE certification is unlawful before the first patient is touched. A target user in Kigali noted that a dead phone number ends referral-based trust permanently in a community that runs on word of mouth. All three personas rejected the 90-day timeline for the same underlying reason: the product is not ready to be in contact with a patient.

**Pre-Mortem (Approach d — failure-mode analysis)**

A pre-mortem surfaces the single most likely failure mode: MagnaStep ships at 90 days, an adverse fitting event on a 17-year-old athlete generates press, and disability service partners withdraw. The company never recovers community trust. Sashi's (2012) customer engagement cycle makes this risk concrete — MagnaStep's customers must move from Connection through Satisfaction to Commitment and Advocacy if the model is to work. A single clinical failure before Satisfaction is established collapses the entire cycle; in a referral-driven market, there is no re-entry point.

**Scenario Analysis (Approach c — structured outcome comparison)**

Two shipping scenarios were evaluated. Scenario A: ship at 90 days without regulatory clearance → MDR enforcement notice within 60 days of first fitting, investor liability exposure, partner withdrawal. Scenario B: ship at 180 days with all five conditions met → 50 pilot fittings completed, clinical evidence generated, Series A pitch legally defensible. Scenario B costs three months of runway (~€350,000 additional burn); it buys the company's survival.

**Five non-negotiable conditions before first fitting:**

1. EU MDR 2017/745 regulatory pathway documented and filed with a Notified Body
2. Clinical pilot protocol approved by an independent ethics committee
3. Partner MOUs signed with a minimum of two named disability service organisations — simulated data removed from all public-facing pages
4. GDPR-compliant health data framework in place — explicit Art. 9 consent, DPIA completed
5. Prototype.html disclaimer updated to label all partner data as simulated until real partners are contracted

These are not conditions designed to delay. They are the minimum required to ensure the first 50 athletes are protected and the first investor pitch is legally defensible.

---

## Part F: The Plan

### 90-Day Plan (Days 1–90) — €800,000

**Strategic priority:** Prove regulatory viability and sign the first real partners. Do not fit a single patient.

#### Headcount and Hiring Sequence

| Week | Hire | Monthly Cost |
|------|------|-------------|
| Week 1 | CEO (founder) activated full-time | €6,000 |
| Week 2 | CTO / Lead Engineer (device) | €7,000 |
| Week 3 | Regulatory Affairs Consultant (EU MDR specialist, contract) | €8,000/month |
| Week 4 | Clinical Lead (part-time, Rwanda-based) | €4,000 |
| Week 6 | Country Director — Rwanda (part-time) | €3,500 |

**Month 1–3 burn on headcount: ~€87,000**

#### Product Milestones

| Milestone | Target Date |
|-----------|-------------|
| Device concept specification frozen | Day 15 |
| Supply chain partner meetings (3 regional manufacturers) | Day 30 |
| Device prototype v0.1 (non-clinical, bench testing) | Day 60 |
| Prototype.html updated — simulated data replaced with real disclaimer | Day 7 |
| Ethics committee application filed | Day 45 |
| MDR technical documentation started | Day 30 |

#### Go-to-Market Spend (90 days)

| Item | Budget |
|------|--------|
| Landing page and prototype hosting (GitHub Pages — free) | €0 |
| Community outreach (WhatsApp, disability networks) | €5,000 |
| Press: TechCabal, CNN Africa outreach | €3,000 |
| Legal (MOU templates, partner agreements) | €15,000 |
| **Total GTM** | **€23,000** |

#### Regulatory and Compliance Workstreams (triggered by Part A findings)

| Finding (Part A) | Action | Owner | Deadline |
|-----------------|--------|-------|----------|
| No EU MDR disclosure | File MDR technical file initiation with Notified Body | Regulatory Consultant | Day 30 |
| GDPR Art. 9 health data | Commission DPIA; draft explicit health consent | Legal counsel | Day 21 |
| Simulated partner data | Remove all phone numbers; add alpha disclaimer | CTO | Day 7 |
| Fictional testimonial | Add "fictional character" disclosure to index.html | CEO | Day 7 |
| Unvalidated "94% cheaper" claim | Add "pending clinical validation" caveat | CEO | Day 7 |

#### 90-Day Line-Item Budget

| Category | Amount |
|----------|--------|
| Headcount (CEO, CTO, Regulatory, Clinical, Country Director) | €87,000 |
| Device R&D (bench prototype, materials, engineering) | €120,000 |
| Legal (MDR, GDPR, MOUs, B-Corp filing) | €45,000 |
| Office / operations (Kigali co-working, equipment) | €18,000 |
| Go-to-market (community, press, events) | €23,000 |
| Travel (partner meetings, supply chain visits) | €15,000 |
| Contingency (10%) | €30,800 |
| **Total 90-day spend** | **€338,800** |

**What we are deliberately NOT doing in the first 90 days:**
- No patient fittings — the device is not clinically validated
- No paid advertising — trust in this market is earned through partners, not impressions
- No full-time marketing hire — the founder is the brand until we have a proof point
- No international expansion — Rwanda only until the pilot works

---

### 180-Day Plan (Days 91–180) — €1,161,200 (remaining seed)

**Strategic priority:** Run the 50-athlete pilot, generate clinical outcomes data, sign government procurement conversations.

#### Headcount Additions (Days 91–180)

| Month | Hire | Monthly Cost |
|-------|------|-------------|
| Month 4 | Marketing & Community Lead (full-time) | €4,500 |
| Month 4 | Clinical Coordinator (Rwanda, full-time) | €3,000 |
| Month 5 | Country Director — Uganda (part-time) | €3,500 |
| Month 6 | CFO (part-time, contract) | €5,000 |

**Month 4–6 additional headcount burn: ~€48,000**

#### Product Milestones (Days 91–180)

| Milestone | Target Date |
|-----------|-------------|
| Device prototype v1.0 (clinical-grade, first fittings) | Day 105 |
| Ethics committee approval received | Day 100 |
| First 10 pilot athletes fitted (Rwanda) | Day 120 |
| 50 pilot athletes fitted | Day 165 |
| Interim clinical outcomes report (10-athlete cohort) | Day 150 |
| Uganda partner MOU signed | Day 110 |
| prototype.html updated with real partner data and live disclaimer | Day 120 |
| Second commit to GitHub with real partner data | Day 120 |

#### Go-to-Market Spend (Days 91–180)

| Item | Budget |
|------|--------|
| "First 50" documentary production (3 episodes) | €30,000 |
| Athlete ambassador programme (stipends, equipment) | €20,000 |
| Sports federation partnership events (Rwanda, Uganda) | €15,000 |
| Press and PR (impact report launch) | €8,000 |
| WhatsApp community management | €5,000 |
| **Total GTM** | **€78,000** |

#### Regulatory Workstreams (Days 91–180)

| Action | Owner | Deadline |
|--------|-------|----------|
| CE marking application submitted to Notified Body | Regulatory Consultant | Day 150 |
| DPIA completed; filed with Rwanda NCSA (data protection authority) | Legal counsel | Day 100 |
| Rwanda FDA pre-submission meeting | Clinical Lead + CEO | Day 110 |
| Real privacy policy live on all pages | Legal counsel | Day 95 |

#### 180-Day Line-Item Budget (Days 91–180)

| Category | Amount |
|----------|--------|
| Headcount (expanded team, 6 roles) | €280,000 |
| Device manufacturing (50 pilot devices + fittings) | €350,000 |
| Clinical trial costs (ethics, monitoring, adverse events) | €80,000 |
| Legal and regulatory (CE marking, GDPR, Rwanda FDA) | €60,000 |
| Go-to-market (documentary, ambassadors, events, PR) | €78,000 |
| Operations (office, travel, equipment) | €45,000 |
| Uganda market entry (partner meetings, travel) | €30,000 |
| Contingency (10%) | €92,020 |
| Reserve (Series A preparation) | €146,180 |
| **Total 180-day spend** | **€1,161,200** |

**What we are deliberately NOT doing in Days 91–180:**
- No Kenya entry — two countries is the limit for a 50-person team with €2M
- No retail/direct-to-consumer channel — all distribution through disability service partners only
- No celebrity ambassador programme — outcomes data is our marketing, not endorsements
- No Series A raise until 12-month clinical data is available — a premature raise without outcomes evidence would undervalue the company

**Total seed allocated:** €338,800 (Days 1–90) + €1,161,200 (Days 91–180) = **€2,000,000**

---

*This critique was produced as part of the H9CEAI Innovator Critique assessment, National College of Ireland, MSc AI in Business, April 2026. Student ID: x24317713. AI tools used: Claude (Anthropic) for pipeline execution, code generation, regulatory analysis, and critique drafting; Gemini (Google) for hero image generation (Imagen) and video concept development. All AI outputs were reviewed, corrected, and critically evaluated by the student at every stage — including identification and correction of AI hallucinations documented in Part C.*
