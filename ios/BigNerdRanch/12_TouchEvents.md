## Touch Events and UIResponder

```objc
@interface UIResponder
- (void)touchesBegan:(NSSet *)touches withEvent:(UIEvent *)event;
- (void)touchesMoved:(NSSet *)touches withEvent:(UIEvent *)event;
- (void)touchesEnded:(NSSet *)touches withEvent:(UIEvent *)event;
- (void)touchesCancelled:(NSSet *)touches withEvent:(UIEvent *)event;
@end
```

* `UIBezierPath`
* `CGPoint location = [t locationInView:self];`

#### Responder Chain

* every `UIResponder` has pointer `nextResponder`
* view's `nextResponder` is its view controller if it has one, otherwise its `superview`
* view controller's `nextResponder` is its view's `superview`
* top-most superview is `window`
* window's `nextResponder` is `UIApplication` instance

* `UIControl`
  * `- (void)addTarget:(id)target action:(SEL)action forControlEvents:(UIControlEvents)controlEvents`
  * `- (void)sendActionsForControlEvents:(UIControlEvents)controlEvents`
