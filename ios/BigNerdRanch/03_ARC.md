## Managing Memory with ARC

#### How objects lose owners

* A variable that points to the object is changed to point to another object.
* A variable that points to the object is set to nil.
* The owner of the object is itself destroyed.
* An object in a collection, like an array, is removed from that collection.

* child should not own parent - retain cycle
* `__weak ClassName *_var;`

#### Properties

```objc
@property (attributes) ClassName *var;
```

* Multi-threading: `nonatomic`, `atomic`
* Read-write: `readwrite`, `readonly`
* Memory management: `strong`, `weak`, `copy`, `unsafe_unretained`

* in implementation, `@synthesize var = _var;` same as `@synthesize var;`
* need `@synthesize` if you want instance variable and custom implement all accessors

* `@autoreleasepool`
