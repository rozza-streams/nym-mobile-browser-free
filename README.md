# NYM Browser iOS starter

A small native iPhone browser shell using Apple's WebKit. It opens the NYM game hub and includes address/search, back, forward, home, refresh, page progress and page title controls. WebKit uses its normal persistent website store, so a login may remain between launches.

## Free build

This repository is public so its manually started GitHub Actions build can use GitHub's free hosted macOS runners. The workflow creates an **unsigned** IPA artifact that is available for seven days. It does not sign or install the app.

1. Open **Actions** and choose **Build unsigned iOS app**.
2. Select **Run workflow** and wait for the build to finish.
3. Download `NYMMobileBrowser-unsigned-ipa` from the run's Artifacts section.

## iPhone install limits

An unsigned IPA cannot be installed directly. iOS requires signing and provisioning even for private sideloading. A free Apple account signing route requires Apple account authentication and the app normally needs refreshing every seven days. This build workflow does not collect Apple credentials. App Store review is not required for personal sideloading.

## Scope

- This is only a browser shell. It does **not** include or run the NYM Optimiser Chrome extension.
- It does not require a paid model, API key or cloud service.
- It does not bypass game checks or complete verification.
- iOS may suspend apps in the background, so continuous background timers/actions are not promised.
- The project still needs a successful macOS build and an iPhone install test before it can be called verified.
