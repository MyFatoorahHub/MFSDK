
# Introduction
Those building new integrations should consider using  MyFatoorah, which is the easiest way to accept Knet, credit cards, and many other MyFatoorah payment methods.

The MFSDK makes it easy to add MyFatoorah payments to mobile apps.

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
    ![Screenshot](https://github.com/MyFatoorahHub/MFSDK/blob/master/Setp%201.png)
    ![Screenshot](https://github.com/MyFatoorahHub/MFSDK/blob/master/Setp%202.png)
    ![Screenshot](https://github.com/MyFatoorahHub/MFSDK/blob/master/Setp%203.png)

2. Import framework in AppDelegate
```
import MFSDK
```

3. Add below code in didFinishLaunchingWithOptions method

# Objective C 
```
[MFSettings.sharedInstance setMerchantWithMerchantCodeWithMerchantCode:@"999999"
                                                              merchantName:@"Web Pay"
                                                          merchantUserName:@"testapi@myfatoorah.com"
                                                          merchantPassword:@"E55D0"
                                                       merchantReferenceID:@"201454542102"
                                                         merchantReturnURL:@"https://www.google.co.in"
                                                          merchantErrorUrl:@"https://www.yahoo.com"
                                                                      udf1:@""
                                                                      udf2:@""
                                                                      udf3:@""
                                                                      udf4:@""
                                                                      udf5:@""
                                                                isTestMode:YES];



```

# Swift 3.0
```
func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.

          MFSettings.sharedInstance.setMerchantWithMerchantCode(merchantCode: "999999",
                                                              merchantName: "Web Pay",
                                                              merchantUserName: "testapi@myfatoorah.com",
                                                              merchantPassword: "E55D0",
                                                              merchantReferenceID: "201454542102",
                                                              merchantReturnURL: "https://www.google.co.in",
                                                              merchantErrorUrl: "https://www.yahoo.com",
                                                              udf1: "",
                                                              udf2: "",
                                                              udf3: "",
                                                              udf4: "",
                                                              udf5: "",
                                                              isTestMode: true)
        return true
    }
```

# Test Cards Details
1. KNET Test Cards
    8888880000000001 (any Pin /Expiry) Captured
    8888880000000002 (any Pin /Expiry) Not Captured

2. MasterCard Test Cards
    Card No: 5123456789012346 
    Expiry Date : 05/17
    CVV: 123

    Card No : 5313581000123430
    Expiry Date : 05/17
    CVV: 123

3. Visa Test Cards
    Card No: 4005550000000001 
    Expiry Date : 05/17
    CVV: 123

    Card No : 4557012345678902
    Expiry Date : 05/17
    CVV: 123


# Requirements

- Xcode 8 and iOS SDK 11
- iOS 8.0+ target deployment
- armv7, armv7s, and arm64 devices,
- simulator (not i386 and x86_64)
- iPhone and iPad of all sizes and resolutions
 
