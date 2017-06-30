# YJBannerViewOC

`YJBannerView` YJAutoScrollBanner. Objective-C版 无限循环Banner、文字轮播器。

## Adding YJBannerView to your project (添加 YJBannerView 到你的项目)

### CocoaPods

[CocoaPods](http://cocoapods.org) is the recommended way to add `YJBannerView` to your project.

1. Add a pod entry for `YJBannerView` to your Podfile </br>
```bash
    pod 'YJBannerView'
```
2. Install the pod(s) by running </br>
```bash
    pod install
```
3. Include `YJBannerView` wherever you need it with </br>
```bash
    #import "YJBannerView.h"
```

### Carthage

1. Add YJBannerView to your Cartfile. </br>
```bash
    github "YJManager/YJBannerViewOC"
```
2. Run 
```bash
    carthage update
```
3. Follow the rest of the [standard Carthage installation instructions](https://github.com/Carthage/Carthage#adding-frameworks-to-an-application) to add YJBannerView to your project.

### 使用举例

代码及效果如下:

```objc
- (YJBannerView *)secondBannerView{
if (!_secondBannerView) {
    _secondBannerView = [YJBannerView bannerViewWithFrame:CGRectMake(0, CGRectGetMaxY(self.defaultBannerView.frame) + midMargin, kSCREEN_WIDTH, 160) dataSource:self delegate:self placeholderImage:[UIImage imageNamed:@"placeholder"]];
    _secondBannerView.pageControlStyle = YJBannerViewPageControlSystem;   // PageControl 系统样式
    _secondBannerView.pageControlAliment = YJBannerViewPageControlAlimentRight;  // 位置居中
    _secondBannerView.autoDuration = 2.0f;    // 时间间隔
    _secondBannerView.bannerViewScrollDirection = YJBannerViewDirectionTop; // 向上滚动
    _secondBannerView.pageControlHighlightImage = [UIImage imageNamed:@"pageControlCurrentDot"];
    _secondBannerView.pageControlNormalImage = [UIImage imageNamed:@"pageControlDot"];
    _secondBannerView.titleAlignment = NSTextAlignmentLeft;
    }
    return _secondBannerView;
}
```

### 效果如下所示
<img src="https://github.com/YJManager/YJBannerViewOC/blob/master/YJBannerViewDemo/Resources/Effect.gif" width="300" height="533" />

## License

This code is distributed under the terms and conditions of the [MIT license](LICENSE).

## Change-log

A brief summary of each MBProgressHUD release can be found in the [CHANGELOG](CHANGELOG.mdown). 
