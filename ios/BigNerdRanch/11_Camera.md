## Camera

* `UIImageView`
* `UIToolbar`
* `UIBarButtonItem` - identifier Camera
* drag from IB to create action/connection: `- (IBAction)takePicture:(id)sender {`
* `UIImagePickerController` with delegates `<UINavigationControllerDelegate, UIImagePickerControllerDelegate>`
* `[self presentViewController:imagePicker animated:YES completion:nil];`

```objc
- (void)imagePickerController:(UIImagePickerController *)picker didFinishPickingMediaWithInfo:(NSDictionary *)info
{
  UIImage *image = info[UIImagePickerControllerOriginalImage];
  ...
}
```

#### NSDictionary

```objc
NSMutableDictionary *dict = [[NSMutableDictionary alloc] init];
dict[@"key"] = value;
```

* `NSUUID` for item keys
* `UITextFieldDelegate`: `- (BOOL)textFieldShouldReturn:(UITextField *)textField`
* `UIView`: `- (BOOL)endEditing:(BOOL)force`

#### Navigating Implementation Files

```objc
#pragma mark - View life cycle
- (void)viewDidLoad {...}
...

#pragma mark - Actions
...

#pragma mark -
#pragma mark Label
```
