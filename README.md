<div align="center">
  <h1>Mercury Desktop</h1>
  <p><strong>Analyze and visualize Android apps over time.</strong></p>

  <p>
    <a href="https://github.com/elkenson/mercury-desktop-releases/releases"><img alt="Latest release" src="https://img.shields.io/github/v/release/elkenson/mercury-desktop-releases?include_prereleases&style=flat-square&label=release&color=2563eb"></a>
    <img alt="Platform: macOS (Apple Silicon)" src="https://img.shields.io/badge/platform-macOS%20(Apple%20Silicon)-111827?style=flat-square&logo=apple&logoColor=white">
    <img alt="Status: beta" src="https://img.shields.io/badge/status-beta-f59e0b?style=flat-square">
  </p>

  <p>
    <a href="https://github.com/elkenson/mercury-desktop-releases/releases/download/v0.1.0-beta.1/Mercury.Desktop-0.1.0-beta-arm64.dmg"><img alt="Download for macOS" src="https://img.shields.io/badge/Download_for_macOS-Apple_Silicon-2563eb?style=for-the-badge&logo=apple&logoColor=white"></a>
    <a href="https://elkenson.com"><img alt="Website" src="https://img.shields.io/badge/Website-elkenson.com-111827?style=for-the-badge"></a>
    <a href="https://github.com/elkenson"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-elkenson-111827?style=for-the-badge&logo=github"></a>
  </p>

  <p>
    <a href="#macos-installation">Install</a> ·
    <a href="#how-mercury-works">How it works</a> ·
    <a href="#features">Features</a> ·
    <a href="#disclaimer">Disclaimer</a>
  </p>
</div>

<br>

<p align="center">
  <img src="./mercury.png" alt="Screenshot of Mercury Desktop" width="900">
</p>

Mercury is a desktop app for analyzing and auditing Android packages over time. Pull versions from public repositories (or drop in APK samples you already have), then see a variety of features and how that picture changes release to release with chronological visualizations.

Mercury is built for people who need to audit apps continuously, find new evidence, and get a clear view of an APK's footprint without digging through every version by hand. It's also meant for people from other disciplines who can complement their work with technical evidence, brought together in one installable package, without needing to learn cybersecurity tools day to day.

## macOS installation

Everything required is already bundled into the installable `.dmg`.

| Platform | Status |
| --- | --- |
| macOS (Apple Silicon) | **Beta** · [Download `.dmg`](https://github.com/elkenson/mercury-desktop-releases/releases/download/v0.1.0-beta.1/Mercury.Desktop-0.1.0-beta-arm64.dmg) |
| Windows | Coming soon |
| Linux | Coming soon |

1. Download the `.dmg` from [**Releases**](https://github.com/elkenson/mercury-desktop-releases/releases) (not the source code `.zip` files).
2. Open the DMG and drag **Mercury Desktop** into **Applications**.
3. If macOS blocks it ("App is damaged and can't be opened"), open a Terminal window and paste this command:

   ```bash
   xattr -cr "/Applications/Mercury Desktop.app" && open "/Applications/Mercury Desktop.app"
   ```

> [!NOTE]
> The builds are not code-signed yet, so a Gatekeeper prompt is expected.

## How Mercury works

1. **Search** for an app (or enter a package name you already know).
2. **Choose** versions available from a repository listing, or add your own APK samples to Mercury.
3. **Analyze** — Mercury scans for a variety of technical traits and indicators.
4. **Explore** the graph, features, and churn tabs, or try the compare panel when you have more than one package.
5. **Export** if you need something you can share or keep.

> [!IMPORTANT]
> Mercury does **not** ship or redistribute APKs. You resolve and download packages yourself (or analyze local samples you already have). Store terms, local law, the samples you choose to analyze (and any associated risks), and how you use this software are your responsibility.

## Features

### Follow an app across versions
Pick an app, select the versions you care about, and see its history unfold. Traits appear in a chronological heatmap. You can look at connectivity, permissions, SDKs, and native libraries all in the same way, and cross-reference traits with companies and operators.

### Match against hints
Mercury ships a tentative list of complementary data and hints for domains, companies, SDKs, and native libs. Hints are labeled when something matches, so the raw technical signals are easier to understand. This data is a work in progress and is still being verified, so treat matches as leads, not facts, until you've confirmed them.

### Highlight countries
Color heatmaps by curated country hints on matched entities (operator / HQ). When Mercury has a match, technical indicators are colored by country, and country flags and entity labels show on the interactive visualization.

### Compare apps side by side
Load two or more packages and see what's shared versus what's unique between them. Useful when you're checking related apps, rebrands, geotwins, or "same company, different skin" situations. Overlap, outliers, and network graphs help you see the relationships quickly.

### Find what's actually in the package
Browse strings and classes, check signing certificates, and run through a checklist of known frameworks, packers, SDKs, and native libs. Good for answering a range of questions without opening a dozen tools.

> [!TIP]
> Unpacking isn't supported in Mercury. If you have a packed or otherwise hard sample, reach out to our team through [our website](https://elkenson.com). We can help perform bespoke analysis in these cases, including memory forensics and dynamic analysis.

### Work across app frameworks
Coverage of Mercury is expanding beyond plain Java/Kotlin apps. Flutter apps are supported too. Other frameworks (React Native, Capacitor, and similar) are flagged when Mercury recognizes them, and deeper parsing support for them will grow over time.

### Spot churn between releases
See small changes in what was added or removed from one version to the next. When a new domain, permission, or library appears or disappears, it's easy to spot in the granular churn view.

### Export your findings
Save interactive HTML graphs and offline views so you can share and save your findings. You can also copy the current chart as plain text, formatted for pasting straight into an AI chat.

## Disclaimer

> [!CAUTION]
> Catalog labels (domains, companies, SDKs, permissions, native libs) are a tentative list of attribution hints and are still undergoing verification. Treat them as a starting point for investigation, not established facts. Always double-check before publishing or sharing results.

Mercury is provided **as-is** for research and education. It is not a store and not legal advice. The authors make **no warranty** of any kind and are **not liable** for damages, data loss, misuse, terms-of-service violations, illegal use, or anything else that comes from running or relying on this tool. You alone are responsible for what you analyze and how you use the results. Use at your own risk.
