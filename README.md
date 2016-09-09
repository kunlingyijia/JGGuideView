# JGGuideView
##App启动后的引导页
###图片展示：

![Mou icon](https://github.com/mengzhihun6/JGGuideView/blob/master/Snip20160909_3.png)

###使用：

- 在AppDelegate中导入 **#import "JGGuideView.h"**
- 在下列方法中调用

```objc
	- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {

   [self createGuideView];
    
   return YES;
}

```

	//创建引导页
	- (void)createGuideView {
    
    	NSArray* guideImages = @[@"guide-1",@"guide-2",@"guide-3",@"guide-4"];
    	JGGuideView* guide = [[JGGuideView alloc]initWithFrame:CGRectMake(0, 0, kDeviceWidth, kDeviceHight)];
    	guide.guideImages = guideImages;
    	[self.window.rootViewController.view addSubview:guide];
    	[UIView animateWithDuration:0.5 animations:^{
        guide.frame = CGRectMake(0, 0, kDeviceWidth, kDeviceHight);
    }]; 
	}
	