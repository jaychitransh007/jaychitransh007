<!-- Paste this block at the very top of Airboard/README.md, above the existing "# Airboard" heading. Then change that heading to "## For developers". -->

<div align="center">

# Airboard

**Let ideas flow into view.** A meeting whiteboard you run with your voice and hands.

[Open Airboard](https://airboard-pilot-web-634900453473.asia-south1.run.app/) · [Watch the 90-second demo](DEMO_VIDEO_LINK) · [How the voice agent works](Docs/Voice%20Agent%20Architecture%20and%20Observability.md)

</div>

<!-- Replace with a GIF: say "Airo, add a database connected to the API", the diagram appears, then "Airo, undo". Keep it under 8 MB. -->
![Airboard demo](docs/demo.gif)

## What it does

Say "Airo, …" or hold up an open palm and speak. Point at shapes and close your hand to move them. Present the Airboard tab in Google Meet and everyone sees the diagram build as you talk, with nothing to install.

## Why it is built the way it is

| Decision | Why |
| --- | --- |
| Fast phrase rules first, an LLM planner only when they fail | Short commands stay instant and cheap; the model handles the long tail |
| The planner returns a typed plan through one strict function call | The board only ever receives actions it knows how to validate |
| Every plan applies as one change, undone in one step | No confirmation dialogs mid-meeting; Undo is the safety net |
| Talk not addressed to Airo never changes the board | A whiteboard that edits itself during a meeting would be unusable |
| Evals score the final board state, not the model's words | A plausible-sounding answer that draws the wrong diagram is still a failure |

## Status

Production pilot on Cloud Run with Google sign-in. Release gates, open items and the evaluation suite are in [Docs/Project Status.md](Docs/Project%20Status.md) and [evals/README.md](evals/README.md).

---
