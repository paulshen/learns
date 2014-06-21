## View and the View Hierarchy

* views draw itself to its layer, instance of `CALayer`
* designated initializer: `- (id)initWithFrame: (CGrect) aRect`
* `CGRect CGRectMake(CGFloat x, CGFloat y, CGFloat width, CGFloat height)`
* a view's `frame` is size and position relative to `superview`
* views have `subviews`, add via `- (void)addSubview:(UIView *)view`
* views have `superview` pointer. `- (void)removeFromSuperview`

#### Drawing

* `- (void)drawRect:(CGRect)rect`
* `bounds` used to lay out drawing within the boundaries of the view's layer
* `frame` used to layo out view relative to view hierarchy

* `UIBezierPath`
* `UIImage` - `drawInRect`

#### Core Graphics

* 2D drawing API written in C

```objc
CGContextRef currentContext = UIGraphicsGetCurrentContext();
CGContextSaveGState(currentContext);
CGContextSetShadow(currentContext, CGSizeMake(4,7), 3);
// draw stuff with shadow
CGContextRestoreGStart(currentContext);
```

* if you create a Core Graphics object with function that has `Create` or `Copy` in it, need to matching `Release`
* `CGContextDrawLinearGradient`
