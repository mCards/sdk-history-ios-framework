# mCards History SDK for iOS

Customer distribution of **HistorySDK 1.1.13**, tested with **CoreSDK 1.4.8**.
The SDK provides card activity history, transaction details, funding-source and metadata APIs,
and the history UI. Requires iOS 14 or later.

## Install with Swift Package Manager

1. Add `https://github.com/mCards/sdk-history-ios-framework` at version **1.1.13** and
   select the `HistorySDK` product.
2. Add `https://github.com/mCards/sdk-cards-ios-framework` at version **1.1.19** and
   select its `CoreSDK` product for the shared models. If the app already uses that
   package's `CardsSDK` product, CoreSDK is already supplied.
3. Remove any separate older CoreSDK/model package reference to avoid duplicate modules.

No Wantsa repository access is required. Applications that do not use card features can
select just the `CoreSDK` product from the Cards package.

```swift
import HistorySDK
import CoreSDK
```

Configure `HistorySdkProvider.shared` with the cardholder access token and an
`HSDKTokenRefreshCallback` before calling history methods. The callback supplies refreshed
`JWTs`; AuthSDK can be used as the token provider.

[SDK documentation](https://mcards.readme.io/docs/mcards-sdk-overview)

## Release provenance

The XCFramework is copied unchanged from the pinned reference release recorded in
`RELEASE.json`; `.source-revision` records its source commit. Only customer-facing packaging
and documentation are maintained here. After merging the update, tag the merge commit
`1.1.13` to make this version available through Swift Package Manager.
