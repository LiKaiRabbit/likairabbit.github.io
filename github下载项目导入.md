**以前走过的坑全是血和泪啊。**

如果你的电脑联网一句话就可以搞定。

如果没有，那就把源码下载下来，一点一点听我讲（没有老师的苦逼的我以前有网也是这么干的，~>_<~）。**。

先来两张主角的照片：
![这里写图片描述](http://img.blog.csdn.net/20170228103416534?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)                 ![这里写图片描述](http://img.blog.csdn.net/20170228103632546?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


## 一、利用网络添加以依赖库##
   一般在项目的介绍里都会有下面那个compile 。
![这里写图片描述](http://img.blog.csdn.net/20170228160841317?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

添加到app的build.gradle的dependcies里面即可。

![这里写图片描述](http://img.blog.csdn.net/20170228160155307?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

然后右上角会出现是sync now 点击即可自动完成。

![这里写图片描述](http://img.blog.csdn.net/20170228160424218?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

## 二、github项目下载下来导入自己工程目录中##
    github下载下来的工程目录是这样的，我们只需要它的红色箭头文件夹。
    这个工程就叫做viewpagerindicator。
![这里写图片描述](http://img.blog.csdn.net/20170228104546055?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

      把这个文件夹拷贝到自己工程文件夹目录里。
      
   ![这里写图片描述](http://img.blog.csdn.net/20170228105803998?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

    这是第一步，接下来就是要配置gradle，打开自己的AS。 
![这里写图片描述](http://img.blog.csdn.net/20170228111313316?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

    打开后会看到compileSdkVersion、buildToolsVersion、minSdkVersion、targetSdkVersion不一样，必须修改一致。
![这里写图片描述](http://img.blog.csdn.net/20170228113220514?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

     第二步，打开settings.gradle文件。
  
  ![这里写图片描述](http://img.blog.csdn.net/20170228113642359?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

    在里面添加     ':viewpagerindicator'  。注意：和''，格式不能错。

![这里写图片描述](http://img.blog.csdn.net/20170228113903054?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

    第三步，查看工程依赖，再回到下载的viewpagerindicator文件夹下面，打开build.gradle。
![这里写图片描述](http://img.blog.csdn.net/20170228133353835?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

把它和android studio项目里的第一个build.gradle进行比较
![这里写图片描述](http://img.blog.csdn.net/20170228133816921?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
 
 viewpagerindicator的里依赖gradle在自己的项目里有，不用添加，至于版本没有问题。
 
 ![这里写图片描述](http://img.blog.csdn.net/20170228133921042?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
 
![这里写图片描述](http://img.blog.csdn.net/20170228133936719?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

有这种需要添加依赖仓库的，在下载文件夹里找到build.gradle里的classpath添加上去即可，例如xutils3：

![这里写图片描述](http://img.blog.csdn.net/20170228134608494?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

  第四步，打开File--ProjectStructure
  
  ![这里写图片描述](http://img.blog.csdn.net/20170228135108377?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

app--Dependencles----加号-----Module dependency  然后添加即可。

![这里写图片描述](http://img.blog.csdn.net/20170228135615164?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGlrYWlfcmFiYml0/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

结束，添加完成。
