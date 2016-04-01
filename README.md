# MBBViewController
父子控制器框架
.h文件中 导入继承框架
#import "ViewController.h"

@interface NewsViewController : ViewController

@end

.m中 
 (void)viewDidLoad {
//    NSLog(@"%s",__func__);
    
    [super viewDidLoad];
    
    // 3.添加子控制器
    [self setupAllChildViewController];
}

#pragma mark -添加子控制器
- (void)setupAllChildViewController
{
    // 头条
    TopLineViewController *topLineVc = [[TopLineViewController alloc] init];
    // 保存对应按钮的标题
    topLineVc.title = @"头条";
    [self addChildViewController:topLineVc];
    
    // 热点
    HotViewController *hotVc = [[HotViewController alloc] init];
    hotVc.title = @"热点";
    [self addChildViewController:hotVc];
    
    // 视频
    VideoViewController *videoVc = [[VideoViewController alloc] init];
    videoVc.title = @"视频";
    [self addChildViewController:videoVc];
    
    // 社会
    ScoietyViewController *scoietyVc = [[ScoietyViewController alloc] init];
    scoietyVc.title = @"社会";
    [self addChildViewController:scoietyVc];
    
    // 订阅
    ReaderViewController *readerVc = [[ReaderViewController alloc] init];
    readerVc.title = @"订阅";
    [self addChildViewController:readerVc];
    
    // 科技
    ScienceViewController *scienceVc = [[ScienceViewController alloc] init];
    scienceVc.title = @"科技";
    [self addChildViewController:scienceVc];
    
}
