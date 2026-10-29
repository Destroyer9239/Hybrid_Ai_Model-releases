<!-- Published to Destroyer9239/Hybrid_Ai_Model-releases as README.md by the release workflow,
     with 0.7.0 filled in. Edit this copy in the source repository, not the published one. -->

# Hybrid AI Model

A desktop assistant for chatting and coding with AI models that run on your own computer, with optional use of your ChatGPT subscription. Every file edit and command waits for your approval.

<p>
  <a href="https://github.com/Destroyer9239/Hybrid_Ai_Model-releases/releases/download/v0.7.0/Hybrid-AI-Model-Setup-0.7.0.exe"><img alt="Download for Windows" src="https://img.shields.io/badge/Download_for-Windows-0078D4?style=for-the-badge" height="44"></a>
  &nbsp;
  <a href="https://github.com/Destroyer9239/Hybrid_Ai_Model-releases/releases/download/v0.7.0/Hybrid-AI-Model-0.7.0-mac-arm64.dmg"><img alt="Download for Mac" src="https://img.shields.io/badge/Download_for-Mac-111111?style=for-the-badge&logo=apple&logoColor=white" height="44"></a>
</p>

**Version 0.7.0** · Mac button is for Apple silicon (M1 and later). Older Intel Mac? [Download the Intel version](https://github.com/Destroyer9239/Hybrid_Ai_Model-releases/releases/download/v0.7.0/Hybrid-AI-Model-0.7.0-mac-x64.dmg). Not sure? Apple menu › **About This Mac**: "Chip: Apple M…" means Apple silicon.

Once installed, the app updates itself: it tells you when a new version is out.

## Installing on a Mac

1. Open the downloaded `.dmg` and drag **Hybrid AI Model** into **Applications**.
2. Open it from Applications. The first time, macOS says it can't verify the app, because it isn't notarized by Apple yet. Click **Done**.
3. Open **System Settings › Privacy & Security**, scroll down, and click **Open Anyway** next to Hybrid AI Model. Confirm with your password.

It opens normally from then on. If macOS instead says the app **"is damaged"**, open **Terminal** and run this, then open the app again:

```
xattr -dr com.apple.quarantine "/Applications/Hybrid AI Model.app"
```

## Installing on Windows

Double-click the downloaded file. It installs in a few seconds and opens; no admin rights needed. If Windows says **"Windows protected your PC"**, click **More info**, then **Run anyway**. That appears because the app isn't code-signed yet.

## Local AI

Nothing else to install. If Ollama isn't on the computer, choose **Install local AI** in the app and it sets it up for you, then pick a suggested model. Cloud models work without it.

## Other downloads

A portable Windows version (no install, doesn't auto-update) and every past version are on the [Releases page](https://github.com/Destroyer9239/Hybrid_Ai_Model-releases/releases).
