
# Introduction


# Prerequisites
You will need a [My Fatoorah](https://myfatoorah.com) account.

# iOS 9+ Specific
One of the changes in iOS9 is a default setting that requires apps to make network connections only over SSL, this is known as App Transport Security. MFSDK is facilitating the transition to support this change for each of our demand partners in order to ensure they are compliant. In the meantime, developers who want to release apps that support iOS9, will need to disable ATS in order to ensure MFSDK continues to work as expected, and in iOS10 and later only disable ATS for Media and Web content. To do so, developers should add the following to their plist:

```
<key>NSAppTransportSecurity</key>
<dict>
    <key>NSAllowsArbitraryLoads</key>
    <true/>
    <key>NSAllowsArbitraryLoadsForMedia</key>
    <true/>
    <key>NSAllowsArbitraryLoadsInWebContent</key>
    <true/>
</dict>
```
Developers can also edit the plist directly by adding NSAppTransportSecurity key of dictionary type with the parameters: NSAllowsArbitraryLoads, NSAllowsArbitraryLoadsForMedia and NSAllowsArbitraryLoadsInWebContent set to true.

# Usage
1. Add MFSDK in your projects
    ![Screenshot](https://s9.postimg.org/n92phj9tr/DSC_0155.jpg)
    ![Screenshot](https://s9.postimg.org/n92phj9tr/DSC_0155.jpg)
    ![Screenshot](https://s9.postimg.org/n92phj9tr/DSC_0155.jpg)

2. Add below code in didFinishLaunchingWithOptions method



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
 
