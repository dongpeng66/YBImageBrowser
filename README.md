# YBImageBrowser
iOS图片浏览器（功能强大，性能优越）==   image browser for iOS (powerful, superior performance)

<img src="https://github.com/indulgeIn/YBImageBrowser/blob/master/OtherDocuments/YBImageBrowserShowGif.gif">



# 中文说明




## 安装

### 使用 cocoapods

**pod 'YBImageBrowser', '~> 1.0.4'**    

注意：请不要使用 1.0.4 之前的版本；若搜索不到库，可使用`rm ~/Library/Caches/CocoaPods/search_index.json`移除本地索引然后再执行安装，或者更新一下 cocoapods 版本。

### 手动导入

直接将该 Demo 的 `YBImageBrowser` 文件夹拖入你的工程中，并在你的 Podfile 里面添加：
<pre><code>pod 'SDWebImage', '~> 4.3.3'
pod 'FLAnimatedImage', '~> 1.0.12'
</code></pre>



## 用法

最简易的方式：
<pre><code>//创建数据源
YBImageBrowserModel *model0 = [YBImageBrowserModel new];
[model0 setImageWithFileName:obj fileType:@"jpeg"];
model0.sourceImageView = ...
YBImageBrowserModel *model0 = [YBImageBrowserModel new];
YBImageBrowserModel *model1 = ...
//创建图片浏览器
YBImageBrowser *browser = [YBImageBrowser new];
browser.dataArray = @[model0, model1, ...];
browser.currentIndex = indexPath.row;
[browser show];
</code></pre>


