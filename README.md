

# MWLayoutHelpers

This is a small category on UIView that adds a few methods to aid in manual frame layout.

There are already a million libraries like this out there; I can't make a strong argument why mine's inherently better than any other.

## Installation
If you're using CocoaPods, adds this to your Podfile:
`pod "MWLayoutHelpers", git: "https://github.com/lazerwalker/MWLayoutHelpers.git", tag: "1.0.0"` and run `pod install`.

Then, in your code, import the header file where appopriate: `#import <MWLayoutHelpers/UIView+MWLayoutHelpers.h>`.

If you're not using CocoaPods, just add `UIView+MWLayoutHelpers.h/m` to your project and use as normal.


## Usage
In general, there are two types of methods in here:

**Shorthand accessors**: Lets you avoid deeply introspecting into child properties. For example, to get the width of a view, instead of using `someview.frame.size.width` or `CGRectGetWidth(someView)` you can just use `someView.width`.

**Shorthand setters**: Lets you avoid creating throwaway instance variables to muck around with setting inner properties of a view's frame. If you just want to move a view while keeping its size, instead of doing this:

```obj-c
CGRect frame = someView.frame;
frame.origin = CGPointMake(0, 0);
someView.frame = frame;
```

You can just call `[someView moveToPoint: CGPointMake(0, 0)];`.

For full usage, check out the `UIView+MWLayoutHelpers.h` header file.


## Contact
Mike Walker

* https://github.com/lazerwalker
* [@lazerwalker](https://twitter.com/lazerwalker)
* mike@lazerwalker.com

## License
[MIT License](https://github.com/lazerwalker/MWLayoutHelpers/blob/master/LICENSE).