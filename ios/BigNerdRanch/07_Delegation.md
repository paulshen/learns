## Delegation and Text Input

* `UITextField`
* `UIResponder` superclass of `UIView`, `UIViewController`, `UIApplication`
* `UITextInputTraits`

#### Delegation

```objc
@protocol UITextFieldDelegate <NSObject>

@optional

- (BOOL)textFieldShouldBeginEditing:(UITextField *)textField;
- (void)textFieldDidBeginEditing:(UITextField *)textField;
- (BOOL)textFieldShouldEndEditing:(UITextField *)textField;
- (void)textFieldDidEndEditing:(UITextField *)textField;

- (BOOL)textField:(UITextField *)textField shouldChangeCharactersInRange:(NSRange)range replacementString:(NSString *)string;

- (BOOL)textFieldShouldClear:(UITextField *)textField;
- (BOOL)textFieldShouldReturn:(UITextField *)textField;

@end
```

```objc
SEL clearSelector = @selector(textFieldShouldClear:);
if ([self.delegate respondsToSelector:clearSelector]) {
  if ([self.delegate textFieldShouldClear:self]) {
    self.text = @"";
  }
}
```

```objc
@interface MyViewController() <UITextFieldDelegate>
@end
```

* `delegate` pointer is usually weak
* `UIInterpolatingMotionEffect`
* Debugger - setting breakpoints
* `main()` and `UIApplication`
* `UIScrollViewDelegate`
