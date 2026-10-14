# Security policy

TalkerApp is published by OneFinger, a sole proprietorship in Poland. This page says how to report a security problem and what happens next. It covers the TalkerApp desktop app (macOS, Windows) and the components we ship with them (Tauri, the `llama-server` sidecar, Rust crates, npm packages).

## Reporting a vulnerability

E-mail **hello@gettalker.app** with "SECURITY" in the subject. Do not open a public issue.

Please include:
- the TalkerApp version (Settings → Advanced) and the operating system;
- what an attacker can do, and the steps to reproduce it;
- whether you know of anyone using it against real users right now.

You can write in English or Polish. Encrypted mail is not set up yet. If the details are sensitive, say so in the first message and we will agree on a channel.

## What happens next

| When | What |
|---|---|
| ≤ 3 working days | You get a reply confirming we have the report |
| ≤ 14 days | A fix for a high-severity issue ships; lower severities go into the next release |
| With the fix | Release notes describe what was fixed. You are credited if you want to be |

If a vulnerability is already being exploited, we notify the EU authorities as the Cyber Resilience Act requires (Art. 14), through ENISA's Single Reporting Platform to CERT Polska, and tell users what to do.

Please give us a reasonable time to ship a fix before you publish details — 90 days, or less once a fix is out. We will not take legal action against good-faith research that respects users' privacy, does not degrade the service, and does not access other people's data.

## Supported versions

Security fixes go into the latest release, published at <https://github.com/LukaszCzerwinski/TalkerApp/releases>. Free updates keep coming after a Pro licence expires, so every user can always install the fixed version.

## Scope notes

- **Cloud providers** (Google, ElevenLabs) and **Polar** run their own services; report problems in those services to them. Report it to us if TalkerApp misuses them — for example, if it leaks an API key.
- **Local data** is not encrypted by the app (see the user guide, chapter 18). Reading files from an unlocked account is out of scope.
- The machine-readable contact for the website and the app is `https://gettalker.app/.well-known/security.txt`.
