# Ne Alaka? 🧩

**A daily Turkish word-puzzle app, live on the [App Store](https://apps.apple.com/app/id6792897686).**

18 words on the screen. Find the four hidden groups of four, and don't fall for the two decoys.

> The app's source code is private because it's a commercial product. This page explains what I built and how.


| Daily puzzle | Solved | Challenge a friend |
|---|---|---|
| <img src="screenshots/1.png" width="220"> | <img src="screenshots/2.png" width="220"> | <img src="screenshots/3.png" width="220"> |


## The product

- **750+ hand-reviewed puzzles**, written for Turkish players rather than translated from English
- **Daily puzzle with a difficulty curve:** easier early in the week, hardest on Saturday
- **Game modes, streaks, badges and ranks** to bring players back every day
- **Challenge a friend:** a link opens the same puzzle for them and compares results, with no server of my own
- **Premium subscription** through in-app purchases

## How it's built

| Layer | What I used |
|---|---|
| App | React Native with Expo, TypeScript, Expo Router |
| Payments | RevenueCat SDK for subscriptions |
| Analytics | PostHog: funnels and events such as challenge sent, opened and completed drive product decisions |
| Delivery | Expo EAS for iOS builds and over-the-air content updates |
| Content QA | A Python pipeline that checks every puzzle for duplicate groups, repeated words, Turkish spelling and the daily difficulty schedule, plus an optional LLM API pass that reviews puzzles for meaning |

## How I work on it

I'm the product owner and editorial lead; AI coding tools (Claude Code, Codex) are my engineering team. I write each change as a numbered spec, review and test the build on a device, and ship. Puzzles are reviewed in batches of five, and every fix is logged with its reason. 86 commits between April and November 2026.

**Content mix:** 60% Turkish culture · 25% general knowledge and wordplay · 10% pop culture · 5% special days
