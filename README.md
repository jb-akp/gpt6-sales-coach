# GPT-6 AI Sales Coach — full tutorial template

Build a face-to-face sales practice partner in [Akapulu](https://akapulu.com). Nicole plays a fictional agency owner, challenges your offer, then gives transcript-based feedback. Mara is the avatar used in the video; Nicole is the character she plays.

This is a dashboard-only template. No server, ngrok, endpoint, SDK, or application code is needed. James is a co-founder of Akapulu Labs. The agency, offer, budget, and support terms are fictional training material, not a customer case study.

## Before you begin

- Create an Akapulu account and sign in.
- The recording uses **GPT-6 Sol**, which requires a paid Akapulu plan and a saved OpenAI API key. Save it under **Settings → OpenAI API key**, below the plan cards. This is separate from Secrets. Once saved, the account uses your key for its model calls; budget for that model usage as well as your Akapulu plan.
- **GPT-6 Luna** is available on Free without saving your own model key. This is an alternative setup, not a claim of equal behavior.
- As checked in the local product configuration on September 25, 2026, Free includes **10 total conversation minutes**, a **3-minute cap per call**, **2 concurrent calls**, and a watermark. Starter has a **7-minute call cap**. Check current [plan details](https://akapulu.com/pricing/) before recording or purchasing. A full roleplay can exceed Free's cap. For a short exercise, request feedback early; this does not extend the platform limit.
- Allow your browser to use your microphone when starting the call.

## The two files

| File | Paste into | Purpose |
| --- | --- | --- |
| [sales-coach.json](sales-coach.json) | Scenario editor's JSON mode | Conversation stages, instructions, transitions, feedback rubric |
| [runtime-vars.json](runtime-vars.json) | Hosted Link → Runtime variables | Prospect, business facts, offer, objections, success criteria |

Open each file and copy its **raw JSON contents**, not a GitHub URL, Markdown fence, or API request wrapper.

## Setup

1. Go to **Scenarios → New**, and name the scenario.
2. Switch the top-right toggle to **JSON**. Replace the editor contents with `sales-coach.json`.
3. Return to **Visual**. Open **Scenario Menu → Settings → LLM model**, choose your accessible model, and **Save**. If Sol is unavailable, check your paid plan and saved account key.
4. In Visual mode, open **Scenario Menu → Hosted Link → + Add hosted link**.
5. Choose an available avatar (Mara in the video), add a label, and paste `runtime-vars.json` into **Runtime variables**.
6. Optionally add STT keywords: `Nicole`, `Northpeak`, `Marcus`. Recording and redirect are optional. Keep the visible AI label enabled.
7. Click **Add Link**, then **Save** in the editor's upper right. Both steps matter.
8. Open the generated URL, click **Start Call**, allow your microphone, and wait for the avatar to be ready.

Anyone with your hosted link can start calls against your account's minutes. Share it intentionally. The repository contains templates, not the creator's live session link or credentials.

## Practice

Ask how the agency makes client reports and how much team time that takes. Pitch an automation that collects numbers, drafts a summary, and leaves a human to review it. Work through the objections and propose a next step with Marcus.

The prospect has consistent fictional facts: twelve total staff-hours per week, fifty dollars per staff-hour, and an initial project budget of $2,500. Savings remain unmeasured; current labor cost is not guaranteed savings.

To stop early, say **“Stop the roleplay and give me feedback now.”** Allow time for coaching before your plan's call cap. A normal exercise can end in agreement or rejection; both lead to feedback. Agreement is simulated, not a booking or purchase.

## Make it yours

Change the values in `runtime-vars.json`, keeping all field names. Keep company size, pain points, offer, budget, objections, and close criteria consistent. Every `{{runtime.*}}` placeholder needs a matching key. For example, change an agency prospect into a buyer for your own service, then replace the objections with ones that buyer would actually raise.

The default feedback rubric covers discovery, explanation of value, reliability/support, decision-maker and next step, and clarity/responsiveness. Each receives 0–2 points. Change the rubric in the **coach** node if practicing a different skill. Scores are model judgments, not validated assessments or evidence of improved real-world sales results. The tool evaluates conversation text, not body language, eye contact, or vocal delivery.

## If something does not work

- **JSON rejected:** copy the full raw object, without code fences, and keep quotes and commas valid.
- **Missing runtime variable:** paste the entire second file; preserve every required key.
- **Cannot edit:** an existing scenario opens in view mode; click **Edit**, then use Visual/JSON.
- **Link not retained:** click **Save** after **Add Link**.
- **Call stops before coaching:** check remaining minutes and the per-call cap. Use a shorter attempt and request feedback earlier.
- **No microphone audio:** check browser and macOS microphone permissions.

## Verification status

The original version was successfully used by the creator. This revision has structural validation and runtime-variable checks. The changed dialogue and rubric still need a live rehearsal; do not assume a higher score or successful close.
