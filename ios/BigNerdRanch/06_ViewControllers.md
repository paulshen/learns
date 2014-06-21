## View Controllers

* `@property (nonatomic, strong) UIView *view;`
* View Controllers create its view hierarchy by:
  * overriding `- (void)loadView`
  * loading a NIB file

```objc
- (void)loadView
{
  ...
  self.view = awesomeView;
}
```

```objc
@implementation MyAppDelegate
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
  ...
  self.window.rootViewController = myVC;
}
```

#### Interface Builder

```objc
NSBundle *appBundle = [NSBundle mainBundle];
MyViewController *myVC = [[MyViewController alloc] initWithNibName:@"myNib" bundle:appBundle];
self.window.rootViewController = myVC;
```

* set File Owner's `Class` in IB

#### UITabBarController

```objc
UITabBarController *tabBarController = [[UITabBarController alloc] init];
tabBarController.viewControllers = @[vc1, vc2];
self.window.rootViewController = tabBarController;
```

* `UIViewController` have `@property(nonatomic, retain) UITabBarItem *tabBarItem`

* `UILocalNotification`

#### View Controller Init Lifecycle

* `- (id)initWithNibName:(NSString *)nibName bundle:(NSBundle *)nibBundle`
* `- (void)loadView`
* `- (void)viewDidLoad`
* `- (void)viewWillAppear:(BOOL)animated`

#### Key-Value Coding

* `- (id)valueForKey:(NSString *)k;`
* `- (void)setValue:(id)v forKey:(NSString *)k;`
* uses accessor, then look for instance variable
* used by IB outlets
