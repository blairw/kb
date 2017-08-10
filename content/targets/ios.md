---
title: iOS
---

*&larr; back to [Targets](%base_url%/?targets)*

# iOS

For products targeting native installation on iPhones and iPads.

## Swift

Use Swift because it's better than freaking Objective C.

But it's still weird, so here's a nice [unofficial cheatsheet](https://github.com/iwasrobbed/Swift-CheatSheet),
and here's [a more detailed cheatsheet specifically around Optionals](http://dcandi.com/post/optionals_cheat_sheet/) (the weird `?` and `!` things).

### CocoaPods

Super awesome dependency management system. Use this.

Useful libraries:

- SwiftyJSON - for handling JSON responses from a server API without getting hung up (too much) about casting.
- SwiftLocation - for doing geolocation queries without dealing with hardware-level APIs.
- RealmSwift - awesome local object storage, no SQL required.
    - The syntax is bizarre. Use the [official cheatsheet](https://realm.io/docs/swift/latest/#cheatsheet).
    - Use Realm Model Generator to set up your `.swift` files instead of authoring your own and writing funky
      non-standard functions in what is supposed to be data-layer code.

### Code documentation

Apple makes Xcode use a funny variant of Markdown. See NSHipster's [reference document](http://nshipster.com/swift-documentation/).

tl;dr:

```swift
/**
    Lorem ipsum dolor sit amet.

    - parameter foo: Consectetur adipisicing elit.
    - parameter bar: Consectetur adipisicing elit.
    - parameter baz: Consectetur adipisicing elit.

    - returns: Sed do eiusmod tempor.
*/
func foo(bar: String) -> AnyObject { ... }
```