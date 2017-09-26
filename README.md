# MFSDK


# Introduction


1. ![Setp 1](/relative/path/to/img.jpg?raw=true "Optional Title")
2. ![Setp 2](/relative/path/to/img.jpg?raw=true "Optional Title")
3. ![Setp 3](/relative/path/to/img.jpg?raw=true "Optional Title")

4. Add below code in didFinishLaunchingWithOptions method

```
func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.

        MFSettings.sharedInstance.setMerchantWithMerchantCode(merchantCode: "23456790", 
                                                              merchantName: "MerchantName", 
                                                              merchantUserName: "MerchantUserName",
                                                              merchantPassword: "MerchantPassword",
                                                              merchantReferenceID: "MerchantReferenceID",
                                                              merchantReturnURL: "merchantReturnURL",
                                                              merchantMerchantErrorUrl: "merchantMerchantErrorUrl", 
                                                              udf1: "", 
                                                              udf2: "",
                                                              udf3: "", 
                                                              udf4: "", 
                                                              udf5: "", 
                                                              isTestMode: true)
        return true
    }
```



# Requirements

- Xcode 8 and iOS SDK 11
- iOS 8.0+ target deployment
- armv7, armv7s, and arm64 devices, and the simulator (not armv6)
- iPhone and iPad of all sizes and resolutions
 
