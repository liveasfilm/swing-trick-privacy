# swing-trick-privacy

Privacy Policy site for the mobile game **Swing Trick**.

- Package / Bundle ID: `com.liveasfilm.swingtrick`
- Live URL: https://liveasfilm.github.io/swing-trick-privacy/
- Developer contact: liveasfilm@gmail.com

The policy is bilingual (Korean + English) and served as a single static
`index.html` via GitHub Pages. No JavaScript, no external assets.
The source of truth lives in the game repo at `store/privacy/index.html`;
copy it here when it changes and update the effective date in three places
(the header `.effective` span, the footer, and any dated text).

## What the policy actually claims

Keep these in sync with the game — a policy that overstates collection is as
bad as one that understates it.

| Claim | Source of truth (game repo) |
|---|---|
| Firebase Analytics only, mobile only | `game/analytics_service.gd`, `game/metrics.gd` `FIREBASE_EVENTS` |
| No advertising ID, no ATT | Android: `addons/firebase_analytics_plugin` removes AD_ID permissions and disables adid collection; iOS: no AdSupport, no ATT prompt |
| Local files `save.json`, `settings.json`, `m1_metrics.jsonl`, `analytics/events.jsonl` | `game/save_store.gd`, `game/settings_store.gd`, `game/metrics.gd`, `game/analytics_service.gd` |
| Photos: add-only | `ios_plugin/src/swing_share_native.mm` `PHAccessLevelAddOnly` |
| No ads, no in-app purchases, no push | no such SDKs in the project |

**If ads, payments, or new data collection are ever added, update the policy
before that release ships.**

## License

Source files in this repository are released under
[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).
