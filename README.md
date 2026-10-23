![Mrityunjay Nigam — AI products, interactive systems, and analytics](assets/profile-header.svg)

# Hi, I'm Mrityunjay

I build applications that turn complex decisions into understandable interactions: finding an outfit, editing a diagram, or staying connected through a daily check-in.

My background is in **operations analytics**. My projects bring that interest in decisions and evidence into **AI applications, web interfaces, and mobile products**.

[Explore the projects](#selected-projects) · [Engineering approach](#how-i-approach-engineering) · [Analytics work](#analytics-foundations) · [Get in touch](#lets-connect)

## Selected projects

### Vibe · Conversational fashion discovery

An application for exploring clothing recommendations around personal preferences, an occasion, a budget, and wardrobe context. The engineering challenge is connecting a conversational request to useful outfit suggestions and evidence about retailer products.

**Explore:** request interpretation, explicit constraints, style knowledge, product verification, conversation continuity, and evaluation.

**Stack:** Python · JavaScript · FastAPI · PostgreSQL / Supabase

[Read the case study](projects/vibe.md) · [Public project overview](https://github.com/jaychitransh007/Vibe-Shopping)

*The standalone application is under active development and its source is private. The public overview distinguishes it from the earlier Shopify prototype.*

### Airboard · Intent-driven diagram editing

A diagram canvas controlled through typed commands, voice, pointer input, and camera gestures. Familiar commands take a deterministic path; less structured requests can use a model to propose a validated edit plan. Accepted changes are applied as a single undoable transaction.

**Explore:** real-time interaction, transcription, structured model output, reference grounding, stale-state rejection, and undo.

**Stack:** TypeScript · pnpm workspace · WebSocket services · Supabase

[Read the case study](projects/airboard.md) · [Explore the source](https://github.com/jaychitransh007/Airboard)

*A local-first prototype; provider-backed voice and semantic interpretation need their own server credentials.*

### Flow · Daily check-ins and connection

A Flutter application organized around a simple daily check-in, with reminders, community interaction, and a nominated contact. Its technical story centers on state: authentication, returning-user onboarding, check-in timing, persistence, and device permissions.

**Explore:** mobile journeys, time-dependent state, reactive navigation, local and push notifications, and integration testing.

**Stack:** Flutter / Dart · Riverpod · GoRouter · Supabase

[Read the case study](projects/flow.md) · [Explore the source](https://github.com/jaychitransh007/TheSigmaFlow)

*The repository contains implementation and release records. Current store availability is not asserted here.*

### VOnn · Fashion recommendation pipeline

An earlier Python and Streamlit project exploring a staged fashion workflow: profile and occasion inputs, styling rules, garment attributes, catalog retrieval, and virtual try-on.

**Explore:** modular pipeline design, semantic retrieval, typed data models, and generated-image integration.

**Stack:** Python · Streamlit · Google Cloud · BigQuery

[Read the case study](projects/vonn.md) · [Explore the source](https://github.com/jaychitransh007/TheSigmaFit4.0.0)

*A historical implementation snapshot, with its own architecture and provider dependencies.*

## How I approach engineering

| Concern | Example in these projects |
| --- | --- |
| Make intent explicit | Translate a clothing request or diagram edit into a structured, checkable representation. |
| Give models a bounded role | Validate proposed actions and apply product rules around model output. |
| Preserve user context | Keep outfit refinements tied to the right request; ground diagram edits against the board that was interpreted. |
| Design recovery paths | Offer undo, explain rejected commands, and distinguish missing evidence from a successful result. |
| Explain the evidence | Separate code tests, replayed fixtures, live integrations, and proposed research. |

The case studies explain the problem, workflow, architecture, important tradeoffs, and what still needs verification. Project documentation describes implemented behavior; it does not substitute for a current benchmark or live-service check.

## Analytics foundations

My earlier work includes exploratory notebooks in people analytics, statistics, and data visualization.

- [HR analytics](https://github.com/jaychitransh007/HR_Analytics): explore employee attrition alongside satisfaction, workload, salary categories, and tenure. [Project guide](projects/hr-analytics.md).
- [Data visualization](https://github.com/jaychitransh007/Kaggle-Data-Visualization): Python plotting exercises using pandas and Seaborn.
- [Statistics](https://github.com/jaychitransh007/Statistics): notebooks exploring statistical concepts.

These are learning and exploratory projects, presented separately from the application work above.

## Let's connect

Interested in engineering collaboration, AI product development, or a product walkthrough? [Open a conversation in this portfolio](https://github.com/jaychitransh007/jaychitransh007/issues/new) and mention the project and what you would like to explore.
