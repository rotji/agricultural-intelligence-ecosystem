# Outreach Register

**Last reviewed:** 22 November 2026  
**Purpose:** Prevent duplicate or premature contact, maintain one record per organisation/contact thread, and coordinate replies and follow-ups.  
**Source:** Gmail sent-folder and inbox review on 21 November 2026. Dates below are Africa/Lagos local dates; Gmail timestamps were converted from UTC.

## Mandatory contact-control rule

1. **One organisation/contact + one subject = one active conversation thread.** Before any new email, search this register and Gmail Sent/Inbox for the organisation, address, domain and subject.
2. If an email has already been sent and no substantive reply has arrived, **do not send another initial email**. Wait. Do not create a second subject/thread to repeat the same questions.
3. When a reply arrives, read the complete thread and prepare a reply **inside that existing thread**. Do not send a new email unless there is a clearly different purpose and the existing conversation makes a separate thread appropriate.
4. Automated acknowledgements are not substantive answers. Keep the thread waiting for the promised human response.
5. Delivery failures are recorded as failed. Do not retry the same address until the address is independently corrected or verified.
6. Follow-up is allowed only after a deliberate waiting interval and review of the existing thread. Record the reason, proposed wording and approval before sending. No automatic follow-up.
7. Record every attempt, reply, bounce, next step and evidence. Never invent a sent date, reply or outcome.
8. The Gmail thread is the conversation source; this Markdown register is the project-level index. Do not publish message bodies or private mailbox identifiers in this public repository.

## Current outreach ledger

| OUT ID | Organisation / contact | Purpose | Sent (Lagos date) | Current state | Next handling |
|---|---|---|---|---|---|
| OUT-0001 | Plateau State Potato Value Chain Support Project / PVCMT — plateaustatepotato@gmail.com | Facility operation, management, capacity, access and project participants | 20 Nov 2026 | Awaiting substantive reply | Wait in existing thread; no second email |
| OUT-0002 | Fruits and Veggies Global — contact@fruitsandveggiesng.com | Potato seed role, sourcing, requirements and intermediary participation | 20 Nov 2026 | Awaiting reply | Wait; no duplicate enquiry |
| OUT-0003 | National Root Crops Research Institute — info@nrcri.gov.ng | Potato varieties, seed systems, research and Plateau links | 20 Nov 2026 | Awaiting reply | Wait |
| OUT-0004 | International Potato Center — cip-nbo@cgiar.org | Nigeria potato projects, partners, technologies and research | 20 Nov 2026 | Awaiting reply | Wait |
| OUT-0005 | GIZ SEDIN — sedin@giz.de | Previous potato value-chain work, stakeholder network and reports | 20 Nov 2026 | Awaiting reply | Wait |
| OUT-0006 | Danny Cool Associates — dannycoolassociates@yahoo.com | Potato farmers, cooperatives and commercial production | 20 Nov 2026 | Awaiting reply | Wait |
| OUT-0007 | PLACOM — info@placom.ng | Commodity market, producers, buyers, storage and services | 20 Nov 2026 | Delivery failed — domain not found (NXDOMAIN) | Do not resend; independently verify a current official address first |
| OUT-0008 | Plateau State Ministry/Commerce contact — commerceandindustry@yahoo.com | Plateau agricultural stakeholder and market information | 20 Nov 2026 | Sent; awaiting reply | Wait |
| OUT-0013 | Plateau State Citizen to Government Platform — egov@citigov.ng | Route request to relevant departments/project coordination and stakeholder contacts | 20 Nov 2026 (request acknowledged 21 Nov) | Automated receipt acknowledgement; substantive routing response pending | Wait in existing thread; no repeat request |
| OUT-0014 | Plateau State RAAMP Project Implementation Unit — website contact form; attempted email: plateaustate@raamp.gov.ng | Plateau agricultural marketing, agro-logistics, project locations, facilities, information resources and participation channels | 22 Nov 2026 | Website contact form submitted successfully (user-confirmed); separate email attempt bounced (554) | Await any response to the website submission; do not repeat the form or retry the bounced email until needed and verified |
| OUT-0015 | National Agricultural Extension and Research Liaison Services (NAERLS) — director@naerls.gov.ng | Agricultural market intelligence, data access, Plateau coverage, information networks and legitimate participation channels | 22 Nov 2026 | Sent; awaiting reply | Wait in the existing thread; no duplicate enquiry |

## Reply events — 21 November 2026

- **OUT-0013 / Citizen to Government Platform:** Automated E-Participation Team acknowledgement confirms receipt and says a team member will respond. This is not yet a substantive referral to a department or project office.
- **OUT-0007 / PLACOM:** Gmail delivery failure states the placom.ng domain could not be found (NXDOMAIN). The message was not delivered. Do not retry this address until a verified replacement is found.

## Review rules and cadence

- Daily: check for replies, bounces and changes in existing threads before proposing any outreach.
- Weekly: review waiting threads, identify whether any follow-up is justified, and approve follow-up individually.
- Before every send: search the organisation, email address/domain and topic in this register and Gmail; check whether a thread already exists.
- Follow-up waiting period: not fixed globally. Set a reasonable period according to the recipient and urgency; record the reason and date. Never send a duplicate initial enquiry simply because a reply has not arrived.

## Update history

### 21 November 2026
- Created this register after Gmail review exposed multiple already-sent agricultural enquiries, one automated acknowledgement and one delivery failure.
- Confirmed the potato project email was already sent on 20 November 2026. The suggested second email in the daily brief must not be sent.
- No new email was sent during this correction.


## Project-boundary correction — 21 November 2026

This register is exclusively for the **Agricultural Ecosystem Intelligence** project. The following contacts belong to separate projects and must not be treated as agricultural outreach, agricultural actions or agricultural follow-ups:
- Reelaay — purchase-order financing enquiry.
- micro1 — company data partnerships/referral programme.
- Turing / Project Lazarus — data/referral partnership.
- Patronus AI — data partnerships/referral programme.

Their messages remain in their own Gmail threads and must be tracked in their respective project records. They have been removed from this agricultural register; no email was deleted or changed. Do not transfer their status or reply events into this project's action tracker. OUT-0009 to OUT-0012 are not reassigned in this project.

Only agricultural-project enquiries are included in the ledger above. OUT-0013 is the Plateau Citizen to Government request concerning routing to agricultural departments/project contacts, so it remains in this register.


## Google Sheets entry confirmation — 21 November 2026

- **Workbook operation:** The user reports that the ChatGPT extension connected to the existing Google Sheet created and used the `Outreach_Register` tab after reviewing the existing workbook tabs and finding no suitable outreach register or existing `OUT-` records.
- **Rows added:** Nine agricultural outreach records, OUT-0001 to OUT-0008 and OUT-0013. The extension reported zero existing rows updated and zero duplicates created, and reported saving and re-reading the updated range `Outreach_Register!A1:R10`.
- **Recorded states:** Seven contacts awaiting reply/substantive reply; OUT-0007 (PLACOM) marked delivery failed due to NXDOMAIN; OUT-0013 (Citizen to Government Platform) marked automated acknowledgement received, substantive routing response pending.
- **Project boundary:** Reelaay, micro1, Turing / Project Lazarus and Patronus AI were not added.
- **Verification limitation:** The extension reported a successful save and read-back, but the original Gmail threads were not independently inspectable in that session. The corresponding source details remain marked as supplied/unverified in the spreadsheet notes. This register therefore records the workbook operation as user-reported, not as an independent Gmail audit.
- **System boundary:** This was a manual extension-assisted spreadsheet update, not an automated two-way synchronisation or an approved canonical-system cutover. GitHub remains the project source of truth under the current pre-cutover governance.


## Outreach events — 22 November 2026

- **OUT-0014 / Plateau State RAAMP:** Sent to `plateaustate@raamp.gov.ng` at 22:55 Africa/Lagos (20:55:14Z). Gmail returned a delivery failure at 22:56 Africa/Lagos: address not found / SMTP 554. Classify as **Delivery failed**, not awaiting reply. Do not retry until a current official address is independently verified.
- **OUT-0015 / NAERLS:** Sent to `director@naerls.gov.ng` at 23:08 Africa/Lagos (21:08:45Z). Gmail Sent confirms the message. The actual recipient differs from the earlier suggested `nfhl@naerls.com`; record the actual recipient only. Await reply.
- Gmail Sent and the RAAMP failure notice were checked. No duplicate initial enquiry was created for either organisation.

## Update history

### 22 November 2026
- Added OUT-0014 (RAAMP) and OUT-0015 (NAERLS) using Gmail Sent and delivery-status evidence.
- RAAMP website form submission is recorded as successfully submitted (user-confirmed); its separate email attempt is recorded as bounced. NAERLS is recorded as sent and awaiting reply.
- No resend is authorised until the contact-verification and existing-thread rules are satisfied.


## Clarification — RAAMP website contact form, 22 November 2026

The user clarified that the RAAMP enquiry was also submitted through the official website contact form and the website displayed a successful-submission message. Therefore:
- Keep OUT-0014 as one organisation-level outreach record, not two separate organisations or duplicate enquiries.
- Record the website contact-form channel as **Submitted successfully — user-confirmed; awaiting response**.
- Retain the separate email attempt and its SMTP 554 bounce as channel-level history only.
- Do not classify the overall RAAMP outreach as simply failed or tell the user that RAAMP was not contacted.
- The website-form success is based on the user's direct report; no form receipt/reference number was supplied.
- Wait for a response; do not submit the same enquiry again.
