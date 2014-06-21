## Views: Redrawing and UIScrollView

* `-(void)touchesBegan:(NSSet *)touches withEvent:(UIEvent *)event`
* run loop listens and responds to events, then rerenders dirty views
* `[self setNeedsDisplay];`

#### Class Extensions

```objc
@interface ClassName ()
@end
```

#### UIScrollView

* `[[UIScrollView alloc] initWithFrame:rect]`;
* `scrollView.contentSize = ...;`
* `scrollView.pagingEnabled = YES;`
