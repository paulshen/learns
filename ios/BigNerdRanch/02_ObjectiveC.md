## Objective-C

* create objects by sending message `alloc`
* message sending: `[receiver selector:argument ...];`
* destroy object: `obj = nil;`
* message sent to `nil` is ignored

* `NSString`, `NSArray`, and mutable variants
* fast enumeration: `for (NSString *item in items) { ... }`
* format strings: `NSLog(@"%d, %f, %c", 1, 2.5, 'A');`

```objc
@interface MyClass : SuperClass
{
  NSString *_instanceVars;
  int _moreInstanceVars;
}

@end
```

* `[item foo]` equivalent to `item.foo`
* `[item setFoo:bar]` equivalent to `item.foo = bar`
* convention to use dot notation for accessor methods

* initializers and designated initializers
* initializers return type is `(instancetype)`
* `id` same as `void *`
* sending messages to `super` skips `self` when looking for method
* class methods use `+` instead of `-`

* ObjC arrays can only contain objects, no primitives or `nil`
* use `NSNumber`, `NSValue`, `NSData`, and `NSNull`
* exceptions and unrecognized selectors
* `#import` vs `@import` - optimizations for `@import` but only available for Apple modules
