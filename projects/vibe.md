[← Portfolio](../README.md) · [Public project overview](https://github.com/jaychitransh007/Vibe-Shopping)

![Vibe — conversational fashion discovery](../assets/vibe-header.svg)

# Vibe: from a clothing request to an explained recommendation

**Product:** personalized fashion discovery. **Status:** active development; standalone source is private. **Audience:** people exploring outfits and engineers interested in recommendation systems.

## The problem

A clothing request carries several kinds of information at once. “A relaxed dinner outfit under ₹8,000” includes an occasion, a style direction, and a budget. A follow-up such as “keep the shirt and change the trousers” adds a continuity requirement. A useful shopping suggestion also depends on the actual product, retailer, currency, availability, and destination market.

Vibe brings those concerns into a conversational application. The intended value is an understandable path from a person's request to clothing options they can inspect and refine.

## A representative journey

1. Complete the application's profile and onboarding requirements.
2. Describe an occasion, preferences, and spending constraints.
3. Inspect outfit suggestions, explanations, and retailer product details.
4. Refine the request or refer back to a particular outfit.
5. Save a look or explore the supported visualization and wardrobe surfaces.

This is a walkthrough of the product's design. Specific query families, live inventory, and visualization quality need verification against the version being demonstrated.

## How the pieces fit together

![Architecture overview: browser, server boundary, recommendation engine, and supporting data](../assets/vibe-architecture.svg)

| Layer | Responsibility |
| --- | --- |
| Consumer interface | Onboarding, chat, recommendation cards, saved looks, and product inspection. |
| Server boundary | Handle the browser session and forward allowed requests to the engine without exposing server credentials. |
| Python engine | Interpret the request, combine relevant context and constraints, coordinate recommendation work, and format a response. |
| Style knowledge and prompts | Supply explicit styling vocabulary, rules, configuration, and model instructions. |
| Product evidence | Acquire and check retailer information used to support shopping suggestions. |
| Persistence | Store the profile, conversation, and other application state needed across requests. |
| Evaluation | Exercise contracts, deterministic fixtures, pipeline behavior, and deployed journeys in distinct lanes. |

The diagram is a conceptual overview. Some advisory requests do not require product retrieval, and a request can return a partial result or an explanation of missing evidence.

## Engineering decisions worth exploring

### Separate requirements from preferences

A spending ceiling or explicit retained garment has a different meaning from a general aesthetic preference. Representing them separately makes it possible to check whether a recommendation respects the actual request. It also makes failures easier to investigate than treating all user context as undifferentiated prompt text.

**Tradeoff:** explicit contracts require vocabulary, normalization, and regression coverage as query types grow. A parser handling one phrase does not establish broad language coverage.

### Combine explicit knowledge with model-based interpretation

The source organizes styling knowledge, configuration, prompts, planning, composition, and response formatting as distinct parts. This creates places to inspect and improve behavior without making every decision depend on one large prompt.

**Tradeoff:** rules and model behavior can diverge. Evaluation needs to exercise the executed route, including fallbacks, rather than only the intended prompt behavior.

### Treat shopping information as evidence

A plausible outfit description and a currently actionable product recommendation are different outputs. Retailer facts need their own checks and freshness context. Missing price, stock, shipping, or return evidence should remain visible as missing evidence.

**Tradeoff:** live acquisition adds failure modes and time. Frozen retailer fixtures are useful for deterministic regression checks but cannot establish today's availability.

### Preserve references across turns

“Change the trousers in the second outfit” requires both scope and identity: which outfit, which item, what should stay, and what constraints remain active.

**Tradeoff:** conversation state must avoid carrying stale anchors into a new task. Broad multi-turn reliability needs complete journey observations, beyond helper-level tests.

### Measure different claims with different checks

The evaluation tooling separates code contracts, frozen acquisition fixtures, recorded observations, the recommendation pipeline, public server integration, and browser journeys.

**Tradeoff:** one green test run cannot certify all of those surfaces. Quality, latency, retailer freshness, and subjective usefulness need appropriately scoped evidence.

## What this page establishes

This case study describes the architecture and engineering questions documented in the source snapshot reviewed on **23 October 2026**. It publishes no current accuracy, conversion, latency, cost, or user-benefit claim. Research protocols are proposals until the relevant study is performed.

The documented shopping scope is the **United States and India**. Coverage and behavior must be checked for the current release. Generated visualizations should not be interpreted as measurements or guarantees of physical fit.

## Project history and access

The public [Vibe-Shopping repository](https://github.com/jaychitransh007/Vibe-Shopping) originally documented a Shopify storefront prototype. The current standalone application has its own private source and product boundary. The two versions should not be combined into a single claim about current features or deployment.

For a walkthrough or technical discussion, [open a portfolio conversation](https://github.com/jaychitransh007/jaychitransh007/issues/new). The public overview provides context without requiring access to the implementation.
