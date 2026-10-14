# Accountability Gate

**AI can’t feel consequences. Its permissions can change.**

An early, local prototype for putting explicit limits around AI work: a per-task spend cap, approval before each run, an audit trail, and access that pauses after repeated failures.

Built in public by [@simibharaj](https://github.com/simibharaj).

## Try the prototype

Open [`index.html`](./index.html) in a browser. No install, account, API key, server, or network connection is needed.

The demo lets you:

- Set a maximum spend for a task.
- Approve or deny each **simulated** run.
- See a run blocked when its estimate exceeds the remaining budget.
- Record whether the result succeeded or failed.
- Require review after a failure and pause access after repeated failures.
- Export or clear the local audit trail.

## Important: what this version does not do

This is a **working interaction prototype**, not a provider integration. It sends no AI requests and cannot see or control usage in ChatGPT, Claude, Gemini, Perplexity, or their subscriptions. The “allowed actions” are recorded as task rules in this demo; they do not block actions in another app. The budget and failure gates become real controls only when AI calls are routed through an integrated gateway or supported extension.

The next engineering step is to test a provider-neutral policy gate that requires a user-set budget and explicit authorization before an API-backed model call. Controlling usage inside each provider’s consumer subscription will require separate integrations and may not be technically available.

## Privacy

The prototype stores its demo state in this browser’s `localStorage`. It has no analytics, external scripts, or network calls. Use **Export data** to keep a copy or **Clear local data** to remove it from this browser.

## Product thesis

AI systems do not experience shame or pain. Accountability has to be external and observable: unauthorized spend is blocked, repeated failures reduce access, and actions leave a receipt the user controls. The product should automate capture and verification rather than make people maintain another log.

## Status

Early concept and local prototype. Provider integrations, automatic outcome verification, and willingness to pay have not been validated. Feedback and use cases are welcome through GitHub Issues.
