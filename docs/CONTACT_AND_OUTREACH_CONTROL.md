# Contact and Outreach Control Protocol

**Version:** 1.0  
**Effective date:** 21 November 2026  
**Applies to:** Agricultural Ecosystem Intelligence project outreach to companies, government agencies, research institutions, development partners, buyers, suppliers and programme offices.

## 1. Purpose

Prevent duplicate messages, fragmented conversations, premature follow-ups and loss of reply history. Outreach is an execution activity governed by the action tracker and the Outreach Register.

## 2. Required pre-send checks

Before drafting or sending any message:

1. Search `registers/OUTREACH_REGISTER.md` for the organisation, contact, domain, purpose and prior OUT ID.
2. Search Gmail Sent and Inbox for the organisation, address/domain and related subject/topic. Inspect the complete existing thread.
3. Check for an earlier message sent through another channel (web form, portal, phone or social account) where known.
4. If a message already exists and is awaiting a response, stop. Do not send another initial email or repeat the same questions.
5. If a message bounced, do not retry the same address. Verify a replacement address through an authoritative source first.
6. If a substantive reply exists, continue in that thread. Prepare a reply draft for review; do not open a duplicate conversation.
7. Only create a separate thread when the purpose is genuinely different and the existing correspondence does not provide an appropriate channel.

## 3. Conversation states

- **Draft not sent:** no contact attempt has occurred.
- **Sent — awaiting reply:** email successfully appears in Sent; no reply received.
- **Acknowledged — substantive reply pending:** automated receipt only.
- **Substantive reply received:** human or official response contains information requiring review.
- **Delivery failed:** bounce or delivery failure confirmed.
- **Follow-up eligible:** a deliberate waiting period has elapsed and a reason to follow up is recorded.
- **Closed:** objective achieved or contact route rejected, with evidence.

An automated acknowledgement must never be classified as a substantive reply. Silence is not proof of rejection, closure or non-operation.

## 4. Follow-up discipline

No automatic or repeated follow-up. A follow-up must:
- Refer to the existing conversation and remain in the same thread.
- Be justified by elapsed time, urgency or a specific unresolved matter.
- Be recorded with date, reason and approval.
- Avoid repeating questions already answered.
- Be sent only after the user has reviewed/approved the message.

## 5. IDs and linking

Use stable IDs OUT-0001, OUT-0002, etc. One OUT ID represents one recipient organisation/contact and purpose/thread. Link it to related ACT, INV, OPP and EVD records. Do not reuse IDs. If the contact changes, retain history and add a dated update rather than replacing the old record.

## 6. Responsibilities and source of truth

- Gmail is the source of truth for message delivery, thread contents and replies.
- `registers/OUTREACH_REGISTER.md` is the project index for organisations, purpose, dates, state and next handling.
- `registers/ACTION_TRACKER.md` records the project objective/action and links its outreach IDs.
- Daily briefs summarise reply events but do not replace the register.
- Never claim an email was sent unless Gmail Sent confirms it. Never claim a response unless the incoming thread confirms it.
- Do not place full private message bodies, personal mailbox IDs or credentials in the public GitHub repository.

## 7. Daily operating sequence

1. Read current GitHub registers and prior brief.
2. Check Gmail for replies and delivery failures against all active OUT IDs.
3. Update the existing OUT record and linked action/investigation.
4. Only then decide whether any new outreach is necessary.
5. Before any send, run the duplicate-prevention checks in Section 2.
6. Record what was actually done and what remains pending.

## 8. Project rule

**One enquiry, one tracked conversation, one reply thread. Wait for the response before sending another message on the same matter.**
