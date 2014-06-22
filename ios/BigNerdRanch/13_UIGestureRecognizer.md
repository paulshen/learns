## UIGestureRecognizer and UIMenuController

[[https://developer.apple.com/library/ios/documentation/uikit/reference/UIGestureRecognizer_Class/Reference/Reference.html]]

```objc
UITapGestureRecognizer *doubleTapRecognizer = [[UITapGestureRecognizer alloc] initWithTarget:self action:@selector(doubleTap:)];
doubleTapRecognizer.numberOfTapsRequired = 2;
[self addGestureRecognizer:doubleTapRecognizer];
```

#### Concrete subclasses

* UITapGestureRecognizer
* UIPinchGestureRecognizer
* UIRotationGestureRecognizer
* UISwipeGestureRecognizer
* UIPanGestureRecognizer
* UIScreenEdgePanGestureRecognizer
* UILongPressGestureRecognizer

* `- (void)requireGestureRecognizerToFail:(UIGestureRecognizer *)otherGestureRecognizer`
* `- (CGPoint)locationInView:(UIView *)view`
* `- (CGPoint)locationOfTouch:(NSUInteger)touchIndex inView:(UIView *)view`
* `@property(nonatomic, readonly) UIGestureRecognizerState state`
* `- (BOOL)gestureRecognizer:(UIGestureRecognizer *)gestureRecognizer shouldRecognizeSimultaneouslyWithGestureRecognizer:(UIGestureRecognizer *)otherGestureRecognizer`

#### `UIMenuController`

* `[self becomeFirstResponder];` for view to respond to menu actions
* `[UIMenuController sharedMenuController];`

* `- (BOOL)canBecomeFirstResponder { return YES; }`
* `@protocol UIResponderStandardEditActions`

#### `UIGestureRecognizer` state

```objc
typedef enum {
   UIGestureRecognizerStatePossible,
   
   UIGestureRecognizerStateBegan,
   UIGestureRecognizerStateChanged,
   UIGestureRecognizerStateEnded,
   UIGestureRecognizerStateCancelled,
   
   UIGestureRecognizerStateFailed,
   
   UIGestureRecognizerStateRecognized = UIGestureRecognizerStateEnded
} UIGestureRecognizerState;
```
