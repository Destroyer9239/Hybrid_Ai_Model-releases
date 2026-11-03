<!-- Template for SECURITY.md in the public releases repository
     (Destroyer9239/Hybrid_Ai_Model-releases). Edit this copy in the source repository.
     Before it helps anyone, turn on "Private vulnerability reporting" in that repository's
     Settings > Code security. -->

# Security policy

Thank you for helping keep Hybrid AI Model and its users safe.

## Report a vulnerability privately

Please **do not open a public issue** for a security problem.

1. Go to the **Security** tab of this repository.
2. Choose **Report a vulnerability** (GitHub's private security advisories).
3. Describe what you found, how to reproduce it, which version and operating system you used, and what an attacker could do with it.

Only the maintainer can see the report. If the button is not available, open a normal issue that says only "I have a security report" and no details, and the maintainer will arrange a private channel.

Please do not include real passwords, API keys or other people's data in a report. The app's Settings > About > Report a problem text is safe to attach: it contains no chat text, keys or personal folder names.

## What is in scope

- The Hybrid AI Model desktop app for Windows and macOS, in the versions published on this repository's Releases page.
- The installers and the update path (what the app downloads and installs).
- Anything that could let a web page, a model, a file or another program read your files, run commands, reach your saved keys or chat history, or bypass the approval prompts without your say-so.

## Out of scope

- Problems in software the app talks to but does not ship: Ollama, the GitHub CLI, the Codex CLI, local image servers, OpenAI, GitHub and the web services listed in the privacy note. Please report those to their own projects.
- Issues that need an attacker who already controls your computer or your user account. The app protects your files and keys from web content and models, not from a program already running as you. Commands you explicitly allow in a project run with your full user access and are not sandboxed; that is documented behaviour.
- The Windows and macOS warnings shown when you first open the app. The builds are not signed with a paid certificate; this is known and listed in the known issues.
- Test builds ("Hybrid AI Model Alpha"), which are not published here.
- Findings from automated scanners with no demonstrated impact.

## What to expect

This is a small project maintained by one person, so these are goals, not guarantees:

- A first reply within **7 days**.
- A fix or a clear explanation within **30 days** for confirmed, serious problems, sooner when users are at risk.
- You will be told when a fix is published, and credited in the release notes unless you prefer not to be.

Please give the maintainer a reasonable time to fix a problem before you tell anyone else about it.

## Supported versions

Only the latest published version is supported. The app tells you when a new one is out.
