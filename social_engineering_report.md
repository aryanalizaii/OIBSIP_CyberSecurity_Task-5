# Research Report on Social Engineering Attacks

**A Study of Phishing, Pretexting, Baiting, and Other Human-Centered Attack Vectors**

---

**Author:** Muhammad Aryan Tariq
**Program:** BS Cyber Security, Section F24-B
**Roll Number:** 241552
**Institution:** Air University, Islamabad
**Course Area:** Network Security
**Date:** June 2026

---

## Abstract

Unlike attacks that exploit software vulnerabilities, social engineering attacks exploit human psychology — trust, fear, urgency, curiosity, and helpfulness — to bypass even the most well-funded technical defenses. This report examines the major categories of social engineering attacks, with particular focus on phishing, pretexting, and baiting, while also covering closely related techniques such as spear phishing, business email compromise (BEC), vishing, and quid pro quo attacks. The report presents documented real-world case studies — including the 2011 RSA SecurID breach, the 2015 Ubiquiti Networks wire-fraud incident, and the 2020 Twitter "Bitcoin scam" account hijacking — to illustrate the organizational impact of these attacks in terms of financial loss, reputational damage, and downstream security consequences. The report concludes with a consolidated set of preventive recommendations grounded in current industry frameworks, including NIST SP 800-50 Rev. 1 and NIST SP 800-53, and notes the accelerating role of AI-generated phishing, voice cloning, and deepfake video in the current threat landscape.

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [What Is Social Engineering?](#2-what-is-social-engineering)
3. [Types of Social Engineering Attacks](#3-types-of-social-engineering-attacks)
4. [Case Studies: Organizational Impact](#4-case-studies-organizational-impact)
5. [Current Threat Landscape and Statistics](#5-current-threat-landscape-and-statistics)
6. [Preventive Measures and Recommendations](#6-preventive-measures-and-recommendations)
7. [Conclusion](#7-conclusion)
8. [References](#8-references)
9. [Appendix: Publishing This Report to GitHub](#9-appendix-publishing-this-report-to-github)

---

## 1. Introduction

Information security is often framed as a purely technical discipline — firewalls, encryption, intrusion detection — but the single most exploited vulnerability in any organization is consistently its people. Social engineering attacks bypass technical controls entirely by manipulating a human being into voluntarily handing over credentials, money, or system access. Because these attacks target cognitive and emotional triggers rather than software flaws, they remain effective even against organizations with mature technical security programs, and they continue to be the dominant entry point for major breaches.

This report examines the most common forms of social engineering — phishing, pretexting, and baiting — explains the psychological mechanics behind each, documents real organizational case studies, and concludes with prevention guidance suitable for both individuals and enterprises.

## 2. What Is Social Engineering?

Social engineering is the use of deception and psychological manipulation to trick individuals into divulging confidential information, granting unauthorized access, or taking an action that benefits the attacker — such as transferring money or installing malware [1]. Rather than attacking a system directly, the attacker attacks the human operating it, exploiting predictable cognitive shortcuts: the tendency to trust authority, to want to be helpful, to fear consequences, to act on urgency, or to be curious about something unexpected.

Social engineering attacks are generally divided into two broad categories:

- **Digital attacks** — conducted via email, SMS, phone calls, social media, or fake websites (e.g., phishing, vishing, smishing, pretexting).
- **Physical attacks** — conducted in person or through physical objects (e.g., baiting via USB drives, tailgating into restricted areas, dumpster diving for discarded documents) [2].

## 3. Types of Social Engineering Attacks

### 3.1 Phishing

Phishing is the most widespread form of social engineering: attackers masquerade as a reputable company or trusted contact and send communications — most often email — designed to trick the recipient into clicking a malicious link, downloading an infected attachment, or revealing sensitive information such as login credentials [3]. Phishing emails are typically engineered to imitate legitimate organizations closely enough to pass a casual glance.

Several specialized sub-types of phishing exist:

- **Spear phishing** — a phishing attack directed at a specific person or group, customized with personal details such as the target's name, job title, or organization to appear more credible. Because of this personalization, spear phishing frequently results in significant data breaches or unauthorized access to corporate systems [4].
- **Whaling** — spear phishing aimed specifically at senior executives or other high-value targets.
- **Clone phishing** — the attacker resends a previously legitimate email, altered to include a malicious link or attachment, exploiting the trust already established by the original message; this technique is particularly effective because it bypasses the recipient's usual suspicion of an unfamiliar sender [5].
- **Smishing** — phishing delivered via SMS text message; the U.S. Federal Trade Commission reported $470 million in consumer losses tied to text-message scams in data published in April 2025 [6].
- **Vishing (voice phishing)** — phishing conducted over a phone call, frequently impersonating IT support, a bank, or a government agency; vishing attacks increased 442% between the first and second halves of 2024, increasingly relying on AI-generated voice clones to impersonate executives [7].
- **Quishing (QR code phishing)** — a malicious QR code, often placed on posters, parking signs, or emails, that redirects victims to a fraudulent login page when scanned [8].

### 3.2 Pretexting

Pretexting involves an attacker fabricating a believable scenario or false identity to justify a request for sensitive information or access — for example, impersonating a third-party IT provider asking for account credentials while "fixing" a problem, or posing as a bank representative requesting account verification [9]. Pretexting depends heavily on building credibility through a consistent storyline and a believable organizational role; attackers often pose as an IT administrator, HR representative, auditor, or vendor, and extended back-and-forth conversation frequently precedes the final request for credentials or data [10].

Pretexting is rarely used in isolation — it is the foundational technique underlying phishing, vishing, whaling, and business email compromise, because every one of those attacks requires a credible cover story to work. According to Verizon's 2024 Data Breach Investigations Report, pretexting now accounts for 27% of all social engineering incidents [11], and according to other 2025 industry analysis, pretexting became the dominant social engineering tactic of 2024, accounting for roughly half of all social engineering attacks — almost double the prior year's share [12].

A closely related variant is **Business Email Compromise (BEC)**, in which the attacker impersonates a trusted person such as a CEO or supplier to fool employees into wiring money or sensitive data to a fraudulent account [13].

### 3.3 Baiting and Quid Pro Quo

Baiting exploits curiosity or the promise of a reward to lure victims into compromising their own security. A classic real-world example involves leaving a USB drive in a public area with an enticing label such as "Q3 Payroll" or "Top Client Records"; a curious employee who plugs the drive into a work computer unknowingly installs malware on the network [14]. Baiting can also occur digitally, through free downloads, exclusive-sounding documents, or a public QR code promising a reward — the victim engages voluntarily because they believe they are gaining value, and the perceived reward masks the underlying risk [15].

**Quid pro quo** is a closely related variant in which the attacker offers an explicit exchange — for instance, a fake IT support agent who offers to "fix" a reported problem in return for the victim's login credentials [16].

### 3.4 Other Notable Techniques

- **Tailgating / piggybacking** — an attacker follows an authorized person into a physically restricted area without proper credentials.
- **Dumpster diving** — retrieving confidential documents, hardware, or notes from discarded trash to gather information useful for a future pretext.
- **Watering hole attacks** — compromising a website that a specific target group is known to visit, in order to infect their devices.
- **Deepfake-enabled impersonation** — using AI-generated synthetic voice or video to impersonate an executive in real time, discussed further in Section 4.4 [17].

## 4. Case Studies: Organizational Impact

### 4.1 RSA SecurID Breach (2011)

In March 2011, security firm RSA — then a subsidiary of EMC — was breached after attackers sent a small number of employees a spear-phishing email with the subject line "2011 Recruitment Plan" and an attached Excel spreadsheet. The spreadsheet contained a then-unknown ("zero-day") Adobe Flash exploit that installed backdoor access on the employees' machines [18]. From that initial foothold, the attackers escalated privileges and eventually exfiltrated sensitive data related to RSA's SecurID two-factor authentication tokens. Two months later, that stolen data was used in an attempted attack against defense contractor Lockheed Martin, which detected and contained the intrusion; Northrop Grumman and L-3 Communications were also reportedly targeted using data linked to the same breach [19].

**Impact:** RSA's parent company EMC spent an estimated $66 million on incident response and eventually replaced approximately 30,000 customers' SecurID tokens [19]. The case remains one of the most studied examples in cybersecurity because it demonstrates how a single successful phishing email against just a handful of low-level employees can cascade into a supply-chain compromise affecting hundreds of downstream organizations, including U.S. defense contractors.

### 4.2 Ubiquiti Networks Wire Fraud (2015)

In 2015, networking hardware manufacturer Ubiquiti Networks lost nearly $40 million after attackers compromised an employee email account in the company's Hong Kong office and used it to impersonate company executives and employees [20]. Using this access, the attackers requested fraudulent wire payments, and Ubiquiti's own accounting department processed the transfers, believing the requests to be legitimate internal instructions to change payment account details [21]. The company was able to recover only $8 million of the stolen funds after the theft was discovered, despite hoping to recover closer to $15 million [21].

**Impact:** This case is frequently cited as a textbook example of Business Email Compromise (BEC) — no malware or system exploitation was required; the entire attack relied on impersonating trusted internal colleagues convincingly enough that the finance department voluntarily authorized the transfers.

### 4.3 Twitter "Bitcoin Scam" Account Hijacking (2020)

On 15 July 2020, attackers compromised 130 high-profile Twitter accounts — including those of Elon Musk, Barack Obama, Bill Gates, Joe Biden, Kanye West, and corporate accounts such as Apple and Uber — to promote a cryptocurrency scam [22]. The attack began the prior afternoon when the hackers called Twitter employees by phone, claiming to be from Twitter's internal IT help desk and responding to a reported VPN issue; this vishing campaign directed employees to a phishing site designed to look identical to Twitter's legitimate VPN login page [23]. Using credentials harvested from lower-level employees, the attackers performed lateral movement within Twitter's internal network to ultimately obtain credentials from employees who did have access to powerful internal administrative tools.

Once in possession of admin-tool access, the attackers took control of 45 high-value accounts and posted near-identical tweets promising to double any Bitcoin sent to a specified wallet as a COVID-19 relief gesture. Within minutes, one wallet alone received over 320 deposits worth more than $110,000 before Twitter removed the messages [24]. The attackers also accessed the private direct-message archives of several users, including at least one elected official, which represented a far more serious — if less publicized — confidentiality breach than the public scam itself [25].

**Impact:** Beyond the direct financial loss, the incident caused significant reputational damage to Twitter and prompted an FBI investigation. In its aftermath, Twitter implemented new internal protocols, including heightened background checks for employees with access to sensitive user data, phishing-resistant security keys for day-to-day authentication, and mandatory social-engineering-awareness training for all customer-support staff [26]. The case is particularly notable for demonstrating that two-factor authentication (2FA) alone does not prevent social engineering, since the attackers were able to bypass employees' 2FA protections by directly compromising the internal tools those credentials granted access to.

### 4.4 Deepfake-Enabled CFO Impersonation (Hong Kong, 2024)

In a more recent and technologically advanced case, a finance employee at the Hong Kong branch of a multinational firm was instructed — during what appeared to be a live video conference call with the company's CFO and several other colleagues — to transfer over $25 million to multiple bank accounts. In reality, every other participant on the call, including the "CFO," was an AI-generated deepfake. Despite some initial hesitation, the employee complied and processed the transfer, only realizing the deception after contacting the company's head office directly [27].

**Impact:** This incident is widely cited as a landmark example of how generative AI has materially lowered the barrier to convincing real-time impersonation, moving social engineering beyond static phishing emails into fully interactive, multi-person synthetic-media deception.

## 5. Current Threat Landscape and Statistics

Several converging trends define the social engineering landscape entering 2026:

- Phishing volume reached a multi-year high in early 2025: the Anti-Phishing Working Group reported the largest quarterly number of phishing incidents since late 2023 in Q1 2025 [28].
- The EU cybersecurity agency ENISA forecast that more than 80% of social engineering activity worldwide would be driven by AI-powered phishing by early 2025 [28].
- Pretexting overtook phishing as the single most common social engineering tactic in 2024, accounting for roughly half of all social engineering incidents [12].
- Vishing attacks grew by 442% between the first and second halves of 2024, with AI voice cloning increasingly used to impersonate executives convincingly [7].
- In the Asia-Pacific region specifically, social engineering accounted for 25% of all breaches, with pretexting (40%), prompt bombing/MFA fatigue (34%), and phishing (26%) the leading sub-techniques [28].
- The average global cost of a data breach reached $4.44 million in 2025, with the U.S. average significantly higher at $10.22 million; faster identification and containment of social-engineering-driven incidents measurably reduces this cost [29].

A newer technique worth highlighting is **prompt bombing** (also called MFA fatigue), in which an attacker who has already obtained a victim's password repeatedly triggers multi-factor authentication push notifications until the victim, out of frustration or confusion, approves one — granting the attacker access without ever needing to socially engineer a conversation at all [28].

## 6. Preventive Measures and Recommendations

Because social engineering exploits human decision-making rather than a technical flaw, effective defense requires a combination of organizational policy, technical controls, and continuous behavioral training rather than any single tool.

### 6.1 Organizational Policy and Process Controls

- **Out-of-band verification for financial requests.** Any request to change payment details, wire funds, or approve an unusual transaction — especially one received by email, phone, or video call — should be independently verified through a separate, previously known communication channel (e.g., calling a known phone number from a directory, not a number provided in the suspicious message itself) [30]. This single control would likely have prevented both the Ubiquiti wire-fraud loss and the deepfake CFO transfer described above.
- **Least-privilege access and segmented administrative tools.** Limiting which employees can access powerful internal systems (as in the Twitter case) reduces the blast radius when any individual employee's credentials are compromised.
- **Clear, simple reporting mechanism.** Employees should have one obvious, low-friction way to report a suspected phishing or vishing attempt; organizations that measure and reward fast reporting reduce both the likelihood and the cost of a successful breach [29].
- **Incident response planning.** A documented, rehearsed incident response plan — aligned with frameworks such as NIST SP 800-61 — shortens the time between compromise and containment [31].

### 6.2 Technical Controls

- **Multi-factor authentication (MFA), implemented carefully.** MFA substantially raises the bar for attackers, but as the prompt-bombing technique shows, it is not sufficient on its own; organizations should use number-matching or app-based approval (rather than simple push-to-approve) to resist MFA fatigue attacks.
- **Email authentication standards (SPF, DKIM, DMARC).** These reduce the likelihood that a spoofed sender domain will reach a victim's inbox in the first place.
- **Phishing-resistant authentication (e.g., hardware security keys, FIDO2/WebAuthn).** Twitter's own post-incident remediation specifically adopted phishing-resistant security keys for this reason [26].
- **Endpoint and USB device controls.** Disabling autorun on removable media and restricting unknown USB devices directly mitigates baiting attacks of the kind described in Section 3.3.

### 6.3 Continuous Awareness Training

Modern guidance from NIST SP 800-50 Revision 1 (September 2024) — the federal blueprint for building a security awareness and training program — recommends a lifecycle approach: design, develop, implement, and measure, rather than a single annual training session [32]. Current best practice favors short, frequent "micro-lessons" (monthly or bi-weekly) combined with quarterly realistic phishing, vishing, and smishing simulations, since this cadence measurably outperforms once-a-year compliance training [33]. NIST SP 800-53 Revision 5 control family AT (Awareness and Training) — specifically AT-2 and AT-2(3) — formally requires literacy training that explicitly covers social-engineering recognition and reporting, not just general cybersecurity hygiene [33].

Effective training content should be tailored to the channels employees actually face: email pretexting, SMS-based smishing, voice-based vishing, QR-code quishing, and, increasingly, deepfake audio or video impersonation — each of which requires a distinct recognition skill and a distinct verification habit (e.g., "no financial approvals based on a live call or video alone; always confirm out-of-band") [30].

### 6.4 Summary Recommendation Table

| Threat Type | Primary Preventive Control |
|---|---|
| Phishing / Spear phishing | Email authentication (SPF/DKIM/DMARC), security awareness training, link/attachment sandboxing |
| Pretexting / BEC | Out-of-band verification for any financial or credential request, callback policies |
| Baiting / Quid pro quo | USB/endpoint device controls, policies against plugging in unknown media |
| Vishing | Caller-ID skepticism, employee training, callback to known numbers only |
| Quishing | Avoid scanning unsolicited QR codes, especially for login pages |
| Deepfake impersonation (audio/video) | Independent verification through a second channel before any high-value action |
| MFA prompt bombing | Number-matching MFA, rate-limiting push notifications, employee training to never approve an unexpected prompt |

## 7. Conclusion

Across more than a decade of documented incidents — from the 2011 RSA breach, to the 2015 Ubiquiti wire-fraud loss, to the 2020 Twitter account hijacking, to 2024's deepfake-driven $25 million wire transfer — the pattern is consistent: attackers do not need to defeat an organization's firewalls or encryption when they can simply persuade a single trusted employee to act on their behalf. As generative AI continues to lower the cost of convincing voice cloning, video deepfakes, and personalized phishing content, the sophistication of social engineering attacks is increasing faster than most organizations' awareness programs are adapting, with industry forecasts suggesting AI-powered phishing already drives the majority of social engineering activity. Effective defense therefore cannot rely on technology alone; it requires a combination of layered technical controls (phishing-resistant MFA, email authentication, least-privilege access), strict process discipline (out-of-band verification for any sensitive request), and continuous, realistic awareness training aligned with current standards such as NIST SP 800-50 Rev. 1 and NIST SP 800-53's AT control family. Organizations that treat social engineering defense as a one-time training checkbox rather than an ongoing, measured program remain the most vulnerable to becoming the next case study.

## 8. References

This report synthesizes information from the following sources, consulted in June 2026 for academic research purposes. All statistics, incident details, and technical descriptions are attributed to their original source below and have been paraphrased in the author's own words in accordance with academic integrity and copyright standards; no content has been reproduced verbatim.

1. Wikipedia contributors. *Social engineering (security).* Wikipedia, The Free Encyclopedia, 2026.
2. Keepnet Labs. *Top Social Engineering Examples.* 2026.
3. The Knowledge Academy. *Top Social Engineering Attacks to Watch Out For in 2025.*
4. The Knowledge Academy. *Top Social Engineering Attacks to Watch Out For in 2025* (spear phishing description).
5. Secureframe. *The 13 Most Common Types of Social Engineering Attacks in 2025 + How to Defend Against Them.* 2025.
6. CloudSEK. *16 Major Types of Social Engineering Attacks.* 2026 (citing FTC data, April 2025).
7. Spacelift. *70 Social Engineering Statistics for 2026.* 2026.
8. Doppel. *Types of Social Engineering Attacks: What's New in 2026.* 2026.
9. The Knowledge Academy. *Top Social Engineering Attacks to Watch Out For in 2025* (pretexting description).
10. CloudSEK. *16 Major Types of Social Engineering Attacks.* 2026 (pretexting mechanics).
11. Secureframe. *The 13 Most Common Types of Social Engineering Attacks in 2025* (citing Verizon 2024 DBIR).
12. Spacelift. *70 Social Engineering Statistics for 2026* (pretexting dominance in 2024).
13. Spacelift. *70 Social Engineering Statistics for 2026* (BEC definition).
14. The Knowledge Academy. *Top Social Engineering Attacks to Watch Out For in 2025* (USB baiting example).
15. CloudSEK. *16 Major Types of Social Engineering Attacks.* 2026 (baiting mechanics).
16. Doppel. *Types of Social Engineering Attacks: What's New in 2026* (quid pro quo description).
17. Guardz.com. *25 Social Engineering Statistics That MSPs Should Know About in 2026.* 2026.
18. Zoho eProtect. *Learnings from 5 Social Engineering Attacks That Cost Millions.* 2025.
19. ResearchGate / CISO Field Manual. *The Game You Are Already Playing: A CISO's Field Manual for Strategic Cybersecurity in Critical Infrastructure.* 2026 (RSA breach cost and downstream targeting).
20. Gatefy. *10 Real and Famous Cases of Social Engineering Attacks.* 2021.
21. Wikipedia contributors. *Social engineering (security)* (Ubiquiti case, recovered funds).
22. Wikipedia contributors. *2020 Twitter account hijacking.* Wikipedia, The Free Encyclopedia, 2026.
23. New York State Department of Financial Services. *Twitter Investigation Report.*
24. Wikipedia contributors. *2020 Twitter account hijacking* (Bitcoin wallet deposit figures).
25. arXiv. *A Diamond Model Analysis on Twitter's Biggest Hack.* (private message access).
26. Wikipedia contributors. *2020 Twitter account hijacking* (Twitter's post-incident remediation).
27. Guardz.com. *25 Social Engineering Statistics That MSPs Should Know About in 2026* (Hong Kong deepfake CFO case).
28. Spacelift. *70 Social Engineering Statistics for 2026* (APWG Q1 2025 data, ENISA forecast, APAC breakdown, prompt bombing).
29. Consilien. *Social Engineering Awareness Training Guide for Employees.* 2025 (IBM/Ponemon-sourced breach cost figures).
30. Consilien. *Social Engineering Awareness Training Guide for Employees* (out-of-band verification guidance).
31. ScienceDirect. *Reducing the Risk of Social Engineering Attacks Using SOAR Measures in a Real-World Environment: A Case Study.* (NIST SP 800-61 incident response lifecycle).
32. Petronella Cybersecurity News. *NIST 800-50 Rev 1: Awareness Training Blueprint.* 2026.
33. Hoxhunt. *Security Awareness Training: Examples, Metrics & Frameworks (2025).*

*Note on methodology: This report was compiled using a combination of current industry threat-intelligence and training-guidance publications (Spacelift, Secureframe, CloudSEK, Doppel, Guardz, Consilien, Hoxhunt, Petronella), encyclopedic technical references (Wikipedia, cross-checked against primary sources including the NY State Department of Financial Services' official Twitter Investigation Report), and academic/case-study sources (arXiv, ScienceDirect, Zoho eProtect, Gatefy). All sources were accessed in June 2026. Statistics and incident details are presented with their original attribution to avoid plagiarism; readers are encouraged to consult the original sources for full context.*

---

## 9. Appendix: Publishing This Report to GitHub

This section explains, step by step, how to upload `social_engineering_report.md` to GitHub as the required deliverable.

### Option A — Using the GitHub Website (No Command Line Required)

1. Go to [github.com](https://github.com) and log in (create a free account if you don't have one).
2. Click the **+** icon in the top-right corner → **New repository**.
3. Name the repository something descriptive, e.g. `social-engineering-report`.
4. Choose **Public** (so instructors/evaluators can view it) or **Private** if required, then click **Create repository**.
5. On the new repository page, click **Add file → Upload files**.
6. Drag and drop `social_engineering_report.md` into the upload area (or click "choose your files" and select it).
7. Scroll down, add a commit message such as `Add social engineering research report`, and click **Commit changes**.
8. Click on the file in the repository to confirm it renders correctly (GitHub automatically renders `.md` files as formatted text).

### Option B — Using Git from the Command Line (Recommended for Future Submissions)

```bash
# 1. Create a folder for your project and move the report into it
mkdir social-engineering-report
cd social-engineering-report
# (copy social_engineering_report.md into this folder)

# 2. Initialize a git repository
git init

# 3. Add and commit the file
git add social_engineering_report.md
git commit -m "Add social engineering research report"

# 4. Create a new EMPTY repository on github.com first (do not initialize it with a README),
#    then connect your local folder to it (replace the URL with your actual repo URL):
git remote add origin https://github.com/<your-username>/social-engineering-report.git

# 5. Push your file to GitHub
git branch -M main
git push -u origin main
```

### Tips for a Clean Submission

- Make sure the filename matches exactly what was requested: `social_engineering_report.md`.
- Add a short `README.md` to the repository describing the project (recommended — see the separate README.md provided alongside this report).
- Double-check the rendered Markdown on GitHub — headings, tables, and the table of contents should display cleanly.
- If submitting a link to your instructor, copy the repository URL (e.g., `https://github.com/<your-username>/social-engineering-report`) rather than a local file path.
- Keep the repository name lowercase and hyphen-separated, which is the conventional GitHub naming style.

---

*End of Report — Prepared by Muhammad Aryan Tariq, BS Cyber Security (F24-B), Air University Islamabad.*
