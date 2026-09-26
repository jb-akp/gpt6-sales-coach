# GPT-6 Sales Coach

A sales roleplay on a live AI avatar. You call a prospect (Nicole, who owns a marketing agency), pitch her an AI automation build, and work through her three objections. At the end she drops the roleplay and coaches you: one thing you did well, your weakest moment and what to say instead, the objection you handled worst, and a score out of 10.

It runs on [Akapulu](https://akapulu.com). No code needed.

## Files
- `sales-coach.json` is the scenario: intro → discovery → pitch → objection → close or no sale → coach.
- `runtime-vars.json` holds the prospect, the product you're selling, and her objections. Edit it to practice your own pitch.

## Setup (about 10 minutes)
1. **Pick the model.** GPT-6 Luna works on the free plan. GPT-6 Sol is smarter, but it needs a paid plan and your OpenAI key saved at akapulu.com/settings → **OpenAI API key** (below the plan cards, not in Secrets).
2. **Create the scenario.** Go to akapulu.com/scenarios → New, flip the top-right toggle to **JSON**, and paste `sales-coach.json`. Open Scenario Menu → Settings, choose GPT-6 Luna or Sol, and click **Save**.
3. **Make a hosted link.** Go to Scenario Menu → Hosted Link → **+ Add hosted link**. Pick a female avatar and paste the values from `runtime-vars.json` into Runtime variables. Add STT keywords (Northpeak, Nicole, Marcus), click **Add Link**, then click **Save** in the upper right.
4. **Call her.** Open the link and click Start Call. When you hang up, call back to try again.

Anyone with your hosted link can start a call on your minutes, so keep it private.

## Make it yours
Every `{{runtime.*}}` value in the scenario comes from `runtime-vars.json`: the prospect's name, role, company, budget, pain points, what you sell, the objections, and what counts as a win. To switch to a SaaS buyer or a real estate client, change those values. The scenario itself stays the same.
