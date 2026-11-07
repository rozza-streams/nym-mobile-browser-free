# NYM Browser iOS starter

A small native iPhone browser using Apple's WebKit. It opens the NYM game hub and includes address/search, back, forward, home, refresh, page progress and page title controls. Its **NYM status** sheet reads visible resource and activity-timer text from the current game page. WebKit uses its normal persistent website store, so a login may remain between launches.

## Free build

This repository is public so its manually started GitHub Actions build can use GitHub's free hosted macOS runners. The workflow creates an **unsigned** IPA artifact that is available for seven days. It does not sign or install the app.

1. Open **Actions** and choose **Build unsigned iOS app**.
2. Select **Run workflow** and wait for the build to finish.
3. Download `NYMMobileBrowser-unsigned-ipa` from the run's Artifacts section.

## iPhone install limits

An unsigned IPA cannot be installed directly. iOS requires signing and provisioning even for private sideloading. A free Apple account signing route requires Apple account authentication and the app normally needs refreshing every seven days. This build workflow does not collect Apple credentials. App Store review is not required for personal sideloading.

## Scope

- The status sheet is read-only. It does not submit game actions, change settings, handle verification, or bypass game checks.
- It does **not** include or run the NYM Optimiser Chrome extension. Chrome extensions cannot be transferred directly into this iPhone app; their functionality would need a separate iOS implementation.
- It does not require a paid model, API key or cloud service.
- It does not bypass game checks or complete verification.
- iOS may suspend apps in the background, so continuous background timers/actions are not promised.
- The project still needs a successful macOS build and an iPhone install test before it can be called verified.
