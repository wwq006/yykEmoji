# yykEmoji
andorid表情

<img src="./images/1.png">

使用方法：
在Andorid Studio中右击你的项目—>Open Module Settings.

点击左上角的➕号，并在弹出来的页面中选择import gradle Project, 选择我们的library,并可以命名为你需要的module名字，例如”:emoji”（注意冒号）

自动回到了刚刚有➕号的页面，看到左边一栏中的“Modules”一栏中多了我们刚刚导入并命名的Module，把你的app的Compile Sdk Version 和 Build Tools Version 分别设置为
API 21: Android 5.0(Lollipop) 和 21.1.0 (与emoji这个module一样) 点击OK.

该Library引用了如下库，如果你的app也引用了如下库，请把它们的版本号改成一样（同时注意你的targetSdkVersion），否则会报错。

<img src="./images/2.png">

(确保你app里的setting.gradle中含有该Module，之后在app中的build.gradle中的dependencies中加入compile project(‘:emoji’)(emoji换成你之前命名的module名字))之后就可以reBuild一下项目啦，如果遇到EmojiUtil类在Build时报错，在报错的时候导入一下包就好了。
