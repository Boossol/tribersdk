# Triber iOS SDK

## Installation:

### Add the SDK to your Podfile:
```ruby
target 'my_target' do
  pod 'tribersdk'
end
```


### Setup the SDK in your AppDelegate's `application:didFinishLaunchingWithOptions` method:
```ruby
[TriberSDK insertDelegateForApplication:application];
[TriberSDK setAppKey:@"your_triber_sdk_token"];
```

#### Optional: Setup the theme
```ruby
TriberSDKTheme* theme = [[TriberSDKTheme alloc] init];
theme.textColor = [UIColor blackColor];
[TriberSDK setTheme:theme];
```
See below for a list of theme options


### Show the SDK's meeting points view
```ruby
[TriberSDK showMeetingPoints:navigationController];
```
with :
- navigationController : Navigation controller that will contain TriberSDK's view stack


#### Theme options:

##### Titles and item titles font/color:
UIFont* titlesFont;
UIColor* titlesColor;

##### Text block font/color
UIFont* textFont;
UIColor* textColor;

##### Compass view arrow color
UIColor* compassArrowColor;

##### Compass view distance text color
UIColor* distanceTextColor;

##### Background image
NSString* backgroundImage;

##### Meeting points list header
UIColor* meetingPointsHeaderColor;
UIColor* meetingPointsHeaderTextColor;

##### Meeting points list items
UIColor* meetingPointItemBackgroundColor;
UIColor* meetingPointItemTitleColor;
UIColor* meetingPointItemSubtitleColor;

##### Welcome screen
NSString* welcomeScreenLogo;
TriberLogoColor welcomeScreenTriberLogoColor;

##### "Powered by Triber" header
UIColor* poweredByTriberTextColor;
UIColor* poweredByTriberBackgroundColor;
TriberLogoColor poweredByTriberLogoColor;

## Happy Tribin' ! :)
