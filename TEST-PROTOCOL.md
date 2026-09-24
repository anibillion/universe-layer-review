# Creator Review Test — Protocol

## Before the session

1. Open `review.html` in your browser. Confirm it loads.
2. Open DevTools (F12) → Console tab. Keep it open.
3. Say to the creator:

   > "I made this from your chapter and notes. Pretend this is what you receive after publishing. Go through it however you naturally would."

4. Do not explain the buttons. Do not say "we're testing whether this saves you time."

## During the session

Watch. Do not help unless they genuinely cannot understand a button.

Note where they hesitate. Note what they say spontaneously.

## After the review (before reader preview)

Ask:

1. "What would you change before you used this on your next chapter?"
2. "Would you actually use the version you just described?"
3. "What would make you stop using it?"

Then let them see the reader preview.

## Extract the data

In DevTools console:

    copy(JSON.stringify(window.__reviewData, null, 2))

That copies the review data to your clipboard. Paste into a text file and save.

Or open the Application tab → Local Storage → find `review_data`.

## Calculate

- **Total review time** — from the finish panel
- **Average per entry** — total / 15
- **Correction ratio** — (edits + rejects) / 15

## Interpretation

| Result | Meaning |
|---|---|
| Avg < 10s, correction < 30% | Strong — they're confident |
| Avg 10–30s, correction 30–60% | Mixed — useful but imperfect |
| Avg > 30s or correction > 60% | Weak — the system is a burden |

## Do not skip

Bring back:
1. Total time
2. Correction ratio
3. What they said to the three questions
4. Anything they asked for spontaneously
5. Anything they hesitated on
