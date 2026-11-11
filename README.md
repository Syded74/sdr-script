# SDR Call Assistant

A one-page call companion for Health Advisors SDRs working the **Acquity Medicare / ACA** campaign in ConvoSo. It walks you through the script step by step, tells you when a lead qualifies or doesn't, and gives you the right rebuttal in one tap.

**Live site:** https://syded74.github.io/sdr-script/

Works in any browser on iPad, phone or computer. Nothing to install and no login.

---

## What's on the screen

| Area | What it does |
|---|---|
| **Step card** (left) | The exact line to read, a short tip, and answer buttons. Tap the customer's answer to move to the next step. |
| **Path tag** (top right of the card) | Shows where the call is heading: **Medicare** (blue), **ACA** (green), **VA/TRICARE** (blue) or **Not qualified** (red). |
| **Transfer banner** | Appears on the transfer steps, for example "✓ MEDICARE TRANSFER, tell the agent: Medicare lead from Texas". On a disqualified call it shows the reason. |
| **State box** (under the step card) | Type a 2-letter abbreviation (`tx`) to see the full name (**Texas**). It also fills the state into the script lines. |
| **Objections** (right side, or top on iPad and phone) | Tap what the customer said to see the rebuttal, plus the line to get back to the script. |

Yellow text such as **Customer Name** or **State** is a placeholder. Say the real name, not the placeholder.

---

## Keyboard shortcuts (computer)

| Key | Action |
|---|---|
| `1`–`6` | Pick an answer button (each button shows its number) |
| `Backspace` | Go back one step |
| `/` | Jump to the objection search. Type a word, then press `Enter` to open the first match. |
| `Esc` | Close the rebuttal |

On iPad and phone, just tap.

---

## Call flow

### 1. Opening
- **Outbound:** "Hi [Name]! [Agent] here with Health Advisors on a recorded line! It's NOW open enrollment for 2027! …"
- **Inbound:** tap **Inbound call instead** for "Thank you for calling in! …"
- Then: "And can you please verify your first and last name for me." Update the name in ConvoSo and save.

### 2. Age
"Now I know you sound young but I do have to ask… Are you under the age of 65?"

### 3. Medicare Parts A & B
"Do you have Medicare Parts A&B?"

| Age | Has A & B | Goes to |
|---|---|---|
| Under 65 | Yes | **Path A: Under-65 Medicare** |
| Under 65 | No | **ACA path** |
| 65 or older | Yes | **Path B: Over-65 Medicare** |
| 65 or older | No | **Not qualified** |
| Any | Only one part | **Not qualified** |

### Path A: Under 65 with Medicare (disability)
1. "Are you also receiving disability benefits and Medicaid?" They need **yes to both**, otherwise not qualified.
2. Medicare transfer (see step 4).

### Path B: 65 or older with Medicare
1. **Card:** "Just to make sure you have the red, white, and blue Medicare card…" No card = not qualified.
2. **Name again:** "Can you please confirm your first and last name?"
3. **Employer / union:** "Do you have insurance coverage through an Employer or Union?" Yes = not qualified.
4. **VA / TRICARE:** "Ok, and how about coverage through the VA or TriCare Program?"
   - **Yes:** transfer to the **VA/TRICARE accepted campaign**. Skip the medications question.
   - **No:** continue.
5. **Medications:** "Yes or no is fine for this question… Do you currently take 8 or more medications, including over the counter?" Enter yes or no in ConvoSo. **The answer doesn't affect qualifying.**
6. Medicare transfer (see step 4).

### ACA path: under 65, no Medicare
1. "And you are not currently on Medicaid, right?" On Medicaid = not qualified.
2. "Do you have insurance coverage through an employer, union, VA, or TRICARE?" Yes = not qualified.
3. "You're still living in [State], correct?"
4. "Okay, great, and is your ZIP code still [ZIP]?" Update ConvoSo if it's wrong.
5. ACA transfer: "…you may qualify for multiple ACA plans based on your zip code…"

### 4. Transfer
1. **Permission:** "Okay, great! It looks like you may qualify for multiple Medicare plans based on your zip code. … Do I have your permission to transfer you now to a licensed insurance agent?" Transfer **only on a clear yes**.
2. **Bring them on:** "Alright I'm bringing them on the line now, they'll be a big help and let you know what you may qualify for. Please stay on the line with me."
3. **Hold protocol:**
   - Stay on hold until the licensed insurance agent answers.
   - Transfer button: **Medicare DS 1 - PDM Inhouse ACA Medicare DS 1** (VA/TRICARE leads use the VA/TRICARE campaign).
   - Small talk while waiting: "How is your day going so far?" · "Any plans for the upcoming weekend?" · "How is the weather where you are?"
4. **Handoff:** "Hi, I have [First Name] on the line with me from the state of [State]. Can you please help them from here?" Stick to the scripted handoff only. Once the agent and lead are talking, leave the line.

### Not-qualified close
"Unfortunately, it looks like you don't qualify at this time. Thank you for taking my call and have a great day!" Then set the disposition in ConvoSo.

---

## Disqualification rules at a glance

| Path | Not qualified if |
|---|---|
| Medicare, 65 or older | No Medicare A & B · no Medicare card · employer or union coverage |
| Medicare, under 65 | Not receiving **both** disability benefits and Medicaid |
| ACA | On Medicaid · employer, union, VA or TRICARE coverage |
| Any | Has only one of Part A or Part B |

VA/TRICARE on the Medicare path is **not** a disqualification. It goes to the VA/TRICARE campaign.

---

## When the customer says no

Each "no" gets **one** rebuttal made for that step. The step card turns green so you know you're in a rebuttal.

| Where | Rebuttal is about |
|---|---|
| Opening: not interested / busy / wrong person | Making sure they're not missing an option, keeping it quick |
| Won't give name | Making sure you're speaking with the right person |
| Won't give age | Plans depend on age |
| Won't confirm state or ZIP | Plans are different in every state and ZIP |
| Won't transfer | No obligation, they don't have to change anything |

- **"Agrees"** goes straight back into the script.
- **"Still declines"** closes politely: "No problem. Thank you for your time, and have a good day."
- **"Do not call"** ends the call immediately on every step. Mark DNC in ConvoSo right away. Never rebut a do-not-call request.

---

## Objection rebuttals (right panel)

Not interested · Already have insurance · Happy with my insurance · Don't want to change my plan · I'm busy · Call me back · Too many calls · Already did this · Is this a scam? · How did you get my number? · Who are you? · Where are you calling from? · Wrong number · Is it free? · Question about benefits · Where do benefits come from? · Why do you need my age? · What are Parts A & B? · What's a licensed agent? · Take me off your list

After every rebuttal, go back to the script: *"So, could you confirm your first and last name for me?"*

---

## Buttons

| Button | Action |
|---|---|
| **← Back** | Undo the last answer |
| **↻ New call** | Clears everything (step, state, rebuttal, search). It turns green and says "✓ New call started". |

---

## Compliance reminders

- Never say you're licensed or that you're from Medicare.
- Don't promise $0 plans, specific benefits or eligibility. Say "may qualify" and let the licensed agent explain.
- If you don't know an answer: "Great question, the licensed agent can explain that in detail."
- Transfer only after clear permission.
- Honor every do-not-call request immediately.

---

## Privacy

The page runs entirely in your browser. **No customer information is saved or sent anywhere.** Refreshing the page or pressing **New call** clears everything.

---

## Updating the site

The whole tool is the single file `index.html`.

1. Go to **github.com/syded74/sdr-script**.
2. Click **Add file → Upload files**.
3. Drag in the new `index.html` (and this `README.md` if it changed).
4. Click **Commit changes**.
5. Wait 1–2 minutes, then refresh the live site. On iPad, close the tab and reopen it if the old version still shows.

**Check it worked:** the page title says **SDR Call Assistant**, and the opening line starts with "It's NOW open enrollment for 2027!"

### Changing the script
All script lines and rules are near the top of the `<script>` section in `index.html`:
- `nodes`: each call step (`say` = what you read, `hint` = the tip, `choices` = the answer buttons and where they lead).
- `objections`: the rebuttal list.

Keep the wording identical to the approved Acquity script.

---

*For internal use only. Script source: ACQUITY Medicare Script (Confidential).*
