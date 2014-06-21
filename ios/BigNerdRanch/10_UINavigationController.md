## UINavigationController

* `[[UINavigationController alloc] initWithRootViewController:vc];`
* create `UIViewController` using template with XIB
* control drag to create `IBOutlet` properties
* drag `UITextField` to File Owner to set `delegate`

#### `UINavigationController`

* `- (void)pushViewController:(UIViewController *)viewController animated:(BOOL)animated`

```objc
@interface UIViewController (UINavigationControllerItem)

@property(nonatomic,readonly,retain) UINavigationItem *navigationItem; // Created on-demand so that a view controller may customize its navigation appearance.
@property(nonatomic) BOOL hidesBottomBarWhenPushed; // If YES, then when this view controller is pushed into a controller hierarchy with a bottom bar (like a tab bar), the bottom bar will slide out. Default is NO.
@property(nonatomic,readonly,retain) UINavigationController *navigationController; // If this view controller has been pushed onto a navigation controller, return it.

@end
```

* `UIBarButtonItem`
* `UINavigationItem *navItem = self.navigationItem;`
* `navItem.(left|right)BarButtonItem = [UIBarButtonItem ...];`
