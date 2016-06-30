# Triber iOS SDK

## Installation:

### Add the SDK to your Podfile:
```ruby
target 'my_target' do
  pod 'tribersdk'
end
```

***

### Setup the SDK in your AppDelegate's `application:WillFinishLaunchingWithOptions:` method:
```objective-c
[TriberSDK insertDelegateForApplication:application];
[TriberSDK setAppKey:@"your_triber_sdk_token"];
```

#### Optional: Setup the theme
```objective-c
TriberSDKTheme* theme = [[TriberSDKTheme alloc] init];
theme.textColor = [UIColor blackColor];
[TriberSDK setTheme:theme];
```
See below for a list of theme options

***

### Add configuration to your project's Info.plist:
```xml
  <key>NSLocationAlwaysUsageDescription</key>
  <string>Triber a besoin de votre position !</string>
```
```xml
  <key>NSAppTransportSecurity</key>
  <dict>
    <key>NSAllowsArbitraryLoads</key>
    <false/>
    <key>NSExceptionDomains</key>
    <dict>
      <key>triberapp.co</key>
      <dict>
        <key>NSIncludesSubdomains</key>
        <true/>
        <key>NSTemporaryExceptionAllowsInsecureHTTPLoads</key>
        <true/>
        <key>NSTemporaryExceptionMinimumTLSVersion</key>
        <string>TLSv1.1</string>
      </dict>
    </dict>
  </dict>
```

### Show the SDK's meeting points view when you need to
```objective-c
[TriberSDK showMeetingPoints:navigationController];
```
with :
- navigationController : Navigation controller that will contain TriberSDK's view stack

***

#### Theme options:

##### Titles and item titles font/color:
```objective-c
UIFont* titlesFont;
UIColor* titlesColor;
```

##### Text block font/color
```objective-c
UIFont* textFont;
UIColor* textColor;
```

##### Compass view arrow color
```objective-c
UIColor* compassArrowColor;
```

##### Compass view distance text color
```objective-c
UIColor* distanceTextColor;
```

##### Background image
```objective-c
NSString* backgroundImage;
```

##### Meeting points list header
```objective-c
UIColor* meetingPointsHeaderColor;
UIColor* meetingPointsHeaderTextColor;
```

##### Meeting points list items
```objective-c
UIColor* meetingPointItemBackgroundColor;
UIColor* meetingPointItemTitleColor;
UIColor* meetingPointItemSubtitleColor;
```

##### Welcome screen
```objective-c
NSString* welcomeScreenLogo;
TriberLogoColor welcomeScreenTriberLogoColor;
```

##### "Powered by Triber" header
```objective-c
UIColor* poweredByTriberTextColor;
UIColor* poweredByTriberBackgroundColor;
TriberLogoColor poweredByTriberLogoColor;
```

## Happy Tribin' ! :)
