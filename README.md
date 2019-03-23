# ShowIt

> 一直没有舒服的截图标记软件。自己又喜欢漂亮的矢量标记，shutter好像不更新了，上游库要是完蛋，那也就没了。hotshots是矢量的，只是qt5界面太丑。点阵的那种截图标记软件，偶尔用用，不值得在意。gtk3以来，按道理是全部支持矢量截图了的，居然那个矢量截图软件都没在源里面了。

`KISSSSIK` = `Keep It Simple Strong Sexy Small Singular Independent Kind`

> 我乱写的。不过`好看`和`奇特`，是要有的。为什么要截图再标记，先在屏幕标记好，排好了位置，系统自带的截图去搞就好了。就算是录视频，暂停下，放几个矢量标记上去，接着录制，也会蛮舒服的。
![演示](shot.png)
![演示](shot1.png)

>也有蛮多年了，咋除开valadoc.org，就没啥地方有相关资料呢。搞得要去看其他语言的例子。

## 软件结构
###安装都省了
1. 下载单一`tar.gz`。解压就可以跑。（要是我采用MDWiki发布）
1. 或者，直接`git clone xxxx`。（github.com没看到显示README.md时，支持自定义css的）

源码在其他仓库。非商业用途授权吧。GPL3??????

###`▶ showit`
32k大小。很小的主界面。鼠标1键可拖放，2键显示文字，3键退出。

* 接受nautilus或者其他文件管理器的文件拖放。拖一个显示一个，拖一堆显示一堆。![演示](showit.png)
* 鼠标选中任何地方的文字 -- (暂时采用`X selection` PRIMARY)
* **中键**点击主界面，相当于平时的粘贴操作，在屏幕上显示之前鼠标选中的文字。
* `TODO`滚轮切换字体。cairo中文字体获取宽度不对，记得以前是用pango搞定的；系统也没啥中文字体，不好如何处理，还要想想。
* `TODO`Alt滚轮切换8种预定颜色

###`▶ showsvgpngtxt`
35k大小。负责在屏幕显示各种元素的（主要就是svg/png/text）。纯cli，当然可以终端下带参数单独运行。

* 鼠标拖放
* 滚轮缩放。`TODO`要切换渲染位置，目前放大后，不是原始矢量放大。小问题。
* Shift滚轮旋转
* `TODO` Alt滚轮切换8种预定颜色

使用节点手柄调节svg大小和角度，那是Inkscape的功能，我可不愿意作一个小克隆出来，所以只是实现了简单缩放。**%2dK**的执行文件是我的最爱。

###`*.svg`
纯手工绘制。大家喜欢什么就自己画什么。原配的SVG文件采用CC3.0授权。？？？
