# HMAMessageViewManager

Dead simple notification message banners (appearing from bottom) for iOS. 
Xcode 7 and iOS9 SDK.

* No dependencies
* Rotation support (uses autolayout)
* Error, Warning, Success and Default types
* Customize fonts via UIAppearance
* No legacy code ;)

Message banner hides automatically after seconds defined with kMessageViewDismissInSeconds constant or by user tap.
 
Sample Usage
----
```
#import "HMAMessageViewManager.h"
...
[[HMAMessageViewManager sharedManager] showMessageInController:self
                                                          title:@"Oops!"
                                                      subtitle:@"Did not expected this"
                                                          type:HMAMessageViewTypeWarning];
```


Customization
----
To customize font for message title and subtitle in you app delegate (or any other place setting default appearance):
```
#import "HMAMessageView.h"
...
[[HMAMessageView appearance] setTitleFont:[UIFont boldSystemFontOfSize:10]];
[[HMAMessageView appearance] setSubtitleFont:[UIFont boldSystemFontOfSize:6]];
```