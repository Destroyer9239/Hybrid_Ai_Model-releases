<!-- Published to Destroyer9239/Hybrid_Ai_Model-releases as README.md by the release workflow,
     with 0.8.1 filled in. Edit this copy in the source repository, not the published one.
     The in-app About page links to the #privacy and #known-issues sections below. -->

# Hybrid AI Model

A desktop assistant for chatting and coding with AI models that run on your own computer, with optional use of your ChatGPT subscription. Every file edit, and every command the AI suggests, waits for your approval.

<p>
  <a href="https://github.com/Destroyer9239/Hybrid_Ai_Model-releases/releases/download/v0.8.1/Hybrid-AI-Model-Setup-0.8.1.exe"><img alt="Download for Windows" src="https://img.shields.io/badge/Download_for-Windows-0078D4?style=for-the-badge" height="44"></a>
  &nbsp;
  <a href="https://github.com/Destroyer9239/Hybrid_Ai_Model-releases/releases/download/v0.8.1/Hybrid-AI-Model-0.8.1-mac-arm64.dmg"><img alt="Download for Mac (preview)" src="https://img.shields.io/badge/Download_for-Mac_(preview)-111111?style=for-the-badge&logo=apple&logoColor=white" height="44"></a>
</p>

**Version 0.8.1.** The Mac button is for Apple silicon (M1 and later) and is a **preview: not yet tested on a real Mac**. Once installed, the app tells you when a new version is out.

## Which file do I download?

| Your computer                                                               | File                                           | Notes                                                                                                                                                                |
| --------------------------------------------------------------------------- | ---------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Windows 10 or 11, Intel or AMD (x64)**                                    | `Hybrid-AI-Model-Setup-0.8.1.exe`        | Recommended. Installs for your account only; no administrator rights needed. Updates itself.                                                                         |
| **Windows 10 or 11 on ARM (ARM64)**, such as a Surface Pro X or Copilot+ PC | `Hybrid-AI-Model-Setup-0.8.1.exe`        | The same installer file; it installs the ARM64 version automatically.                                                                                                |
| Windows x64, no install                                                     | `Hybrid-AI-Model-0.8.1-portable-x64.exe` | Runs from anywhere, such as a USB drive. **x64 only** (use the installer on ARM). Starts more slowly. Does not update itself: the app tells you and opens this page. |
| **Mac with Apple silicon** (M1 or later)                                    | `Hybrid-AI-Model-0.8.1-mac-arm64.dmg`    | **Preview: not yet tested on a real Mac.** Open it and drag the app to Applications.                                                                                 |
| **Mac with an Intel processor**                                             | `Hybrid-AI-Model-0.8.1-mac-x64.dmg`      | **Preview: not yet tested on a real Mac.** Same steps.                                                                                                               |

Not sure which Mac you have? Apple menu, **About This Mac**: "Chip: Apple M…" means Apple silicon; "Processor: Intel…" means Intel. The `.zip`, `.blockmap` and `latest*.yml` files are used by updates and can be ignored.

## System requirements

- **Windows 10 or 11 (64-bit)**, or **macOS 11 or later**.
- **Cloud-only use** (your ChatGPT subscription or your own API key): any computer that runs the OS above. No GPU needed.
- **Models on your own computer** (optional):
  - **8 GB of memory** runs small models (about 3 to 4 billion parameters).
  - **16 GB or more** is recommended for 7 to 8 billion parameter models.
  - A **GPU is optional**. It makes answers faster, but everything also runs on the processor.
  - **Disk space:** about 5 to 10 GB for a first model, and about 2 GB more for Ollama (the program that runs the models). Setup checks this before downloading.
- An internet connection is needed to install, to download models and for cloud models. Local chats work offline once a model is downloaded.

## First launch: this app is not code-signed

The builds are not signed with a paid certificate yet, so Windows and macOS warn you the first time. This is expected, and you only do it once.

**Windows.** SmartScreen says "Windows protected your PC".

1. Click **More info**.
2. Click **Run anyway**.

**Mac.** macOS blocks the app because it is ad-hoc signed and not notarized.

1. Drag **Hybrid AI Model** into **Applications**.
2. Right-click (or Control-click) the app, choose **Open**, then click **Open** again.
3. Or: try to open it once, then open **System Settings**, **Privacy & Security**, scroll down and click **Open Anyway**.

If macOS says the app **"is damaged"**, open **Terminal** and run this, then open the app again:

```
xattr -dr com.apple.quarantine "/Applications/Hybrid AI Model.app"
```

## Local AI

The first time you open the app, a setup window looks at your computer and recommends a model that fits it. Both steps are one click, and nothing happens until you click:

1. **Install local AI** downloads Ollama's own installer (about 1.6 GB on Windows, 230 MB on a Mac), checks that Ollama signed it, installs it without administrator rights and starts it.
2. **Finish and download** downloads the recommended model. You can see progress, cancel, and try again.

Cloud models work without any of this. On Linux, install Ollama from [ollama.com/download](https://ollama.com/download) yourself.

## Privacy

Your chats, files and settings stay on your computer. There is no account, no analytics and no crash reporting. Something leaves your computer only when you allow cloud for a chat (ChatGPT through Codex, or your OpenAI API key), tick the internet tools for a chat, ask about the weather (only the place name goes to Open-Meteo; you can turn this off), click a button that says so, or when the app checks this page for updates. Read the full note: [PRIVACY.md](PRIVACY.md).

## Known issues

Some things have been tested less than others. Plainly:

- **Not code-signed.** Windows SmartScreen and macOS Gatekeeper warn on the first start (see above). The app is safe to run if you downloaded it from this page.
- **The Mac version is a preview.** It has never been opened on a real Mac. It was built and checked only by automatic tests on GitHub's Mac machines. It does not update itself: when a new version is out, the app tells you and opens this page.
- **Windows on Intel or AMD:** the x64 version has been run only under emulation on an ARM PC and in automatic builds, not yet on a real Intel/AMD PC. The ARM64 version has been run on a real ARM PC.
- **Pictures:** making pictures on your computer needs an image server you run yourself (AUTOMATIC1111, Forge, SD.Next or the stable-diffusion.cpp server). It has not been tried with a real one of those, nor with a real OpenAI picture edit. ComfyUI is not supported. Ollama's own image models only work on Ollama 0.14.0 to 0.32.5.
- **Paid OpenAI API:** tested with simulated answers only, never with a real API key.
- **ChatGPT sign-in:** reusing an existing Codex sign-in and sending a message were tested for real. Signing in from scratch in the browser, or with a device code, was not run.
- **Model list:** some suggested model names were written from memory and not checked against Ollama's library. If a download says the model was not found, pick another. Setup downloads were not run on a clean computer.
- **Claude skills and plugins** can be imported, but this was not tried with real public ones.
- **Screen readers:** buttons and controls are labelled and keyboard use was checked with automated accessibility snapshots, but not with NVDA, Narrator or VoiceOver.
- **Commands are not sandboxed.** If you allow a project to run commands, they run with your full user access. A command the AI suggests always needs your approval first.
- **In development, not part of this download:** using several PCs together and signing in to sync settings exist only in private test builds. They have never been tried on two real PCs or with a real account.
- **Linux** is not a supported download.

Found something else? Open **Settings, About, Report a problem**, copy the report (it has no chat text, keys or personal folders) and paste it into a [new issue](https://github.com/Destroyer9239/Hybrid_Ai_Model-releases/issues).

## Security

To report a vulnerability privately, see [SECURITY.md](SECURITY.md).

## Other downloads

Every past version is on the [Releases page](https://github.com/Destroyer9239/Hybrid_Ai_Model-releases/releases). Third-party licences are listed in the app under **Settings, About, Open-source notices**.
