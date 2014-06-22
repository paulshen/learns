## Auto Layout

* Deployment Info -> Universal for iPhone and iPad
* alignment rectangles and layout attributes
* constraints
* constraints in Interface Builder
* priorities
* debugging layouts
  * ambiguous layout
  * unsatisfiable constraints
  * misplaced views

```objc
@interface UIView (UIConstraintBasedLayoutDebugging)
- (NSArray *)constraintsAffectingLayoutForAxis:(UILayoutConstraintAxis)axis NS_AVAILABLE_IOS(6_0);
- (BOOL)hasAmbiguousLayout NS_AVAILABLE_IOS(6_0);
- (void)exerciseAmbiguityInLayout NS_AVAILABLE_IOS(6_0); 
@end
```

* `(lldb) po [[UIWindow keyWindow] _autolayoutTrace]`
* multiple XIB file: `Name~iphone.xib`, `Name~ipad.xib`
