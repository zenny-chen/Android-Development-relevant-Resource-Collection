# Android-Development-relevant-Resource-Collection
我收藏的Android开发技术文集

<br />

- [Google中国开发者网站](https://developers.google.cn/china/)
- [小天才开放平台文档](https://developer.okii.com/docs/develop/00-model.html)
- [Understanding Android API levels](https://docs.microsoft.com/en-us/xamarin/android/app-fundamentals/android-api-levels)
- [使用 Kotlin 开发 Android 应用](https://developer.android.google.cn/kotlin)
- [Kotlin programming language](https://kotlinlang.org/)
- Android Studio指定源文件所关联的语法高亮——点击菜单栏的File；选择File Properties -> Associate with File Type...。里面可以自己找一个当前文件格式。
- [Android NDK使用指南](https://developer.android.google.cn/ndk/guides)
- [Android NDK示例代码](https://github.com/googlesamples/android-ndk/tree/android-mk)
- [Android Studio自带NDK的CMake](https://developer.android.google.cn/ndk/guides/cmake)
- [Android NDK ABI管理](https://developer.android.google.cn/ndk/guides/abis)
- [Android NDK 常见编译问题整理](http://www.liuxiao.org/2016/08/android-ndk-常见编译问题整理/)
- [Android NDK编译选项设置](http://www.aichengxu.com/android/11032333.htm)
- [\[原创\]编写Android.mk中的LOCAL_SRC_FILES的终极技巧](http://blog.ready4go.com/blog/2013/05/20/write-local-src-files-in-android-dot-mk-ultimate-skills/)
- [NDK开发之<cpu-features.h模块功能>](https://www.cnblogs.com/alanfang/p/8944542.html)
- [如何在Android Studio中导入JNI生成的.so库](https://www.cnblogs.com/zenny-chen/p/4040401.html)
- [Gradle骚操作合集](https://www.toutiao.com/a6792129885650289163/)
- [针对Android环境交叉编译GLib](http://zwyuan.github.io/2016/07/17/cross-compile-glib-for-android/)
- [Bringing Armv8.2 Instructions to Android Runtime](https://community.arm.com/developer/tools-software/oss-platforms/b/android-blog/posts/bringing-armv8-2-instructions-to-android-runtime)
- [Runtime detection of CPU features on an ARMv8-A CPU](https://community.arm.com/developer/tools-software/oss-platforms/b/android-blog/posts/runtime-detection-of-cpu-features-on-an-armv8-a-cpu)
- [How do I set the jvm target for android studio using gradle and kotlin?](https://stackoverflow.com/questions/54972087/how-do-i-set-the-jvm-target-for-android-studio-using-gradle-and-kotlin)
- [Android中判断当前API的版本号](https://blog.csdn.net/wangsf1112/article/details/51545101)
- [StructStat](https://developer.android.google.cn/reference/android/system/StructStat)（对应于Linux C语言中的：
```c
#include <sys/stat.h>

struct stat;
```
）
- [用了adb这么久，看了这篇才明白](https://www.toutiao.com/i6760561662891131403/)
- [掌握 Android 系统架构，看这一篇就够了！](https://www.toutiao.com/a6678854584921752078/)
- [安卓手机如何打开开发者模式进行usb调试](https://jingyan.baidu.com/album/14bd256e477577bb6d2612cc.html)
- [Android中关于LogCat的打印](https://zhidao.baidu.com/question/279075586.html)
- [Android性能优化](http://hukai.me/android-performance-patterns/)
- [Android apk反编译工具](http://blog.csdn.net/yanzi1225627/article/details/48215549)
- [Android应用优化实践](http://www.csdn.net/article/2015-11-05/2826130-speed-up-your-app)
- [Android 利用layoutParams代码动态布局空间位置](https://blog.csdn.net/a15838319826/article/details/70808933)
- [Android获取屏幕宽高的三种方式](https://blog.csdn.net/lebulangzhen/article/details/120037671)
- 获取当前屏幕的物理像素宽高：
```kotlin
    private fun getWidthHeight(): Pair<Int, Int> {
        if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.R) {
            val displayMetrics = mMainActivity?.resources?.displayMetrics
            val pixelRatio = displayMetrics?.density ?: 0.0f

            val windowMetrics = mMainActivity?.windowManager?.currentWindowMetrics ?: return Pair(0, 0)
            return Pair(windowMetrics.bounds.width(), windowMetrics.bounds.height())
        }
        else {
            val dm = DisplayMetrics()
            mMainActivity?.windowManager?.defaultDisplay?.getRealMetrics(dm)
            return Pair(dm.widthPixels, dm.heightPixels)
        }
    }
```
- 获取不包含状态栏的屏幕宽高：
```kotlin
        val dm = DisplayMetrics()
        val size = Point(0, 0)
        windowManager.defaultDisplay.getSize(size)
```
- 获取当前屏幕密度（density, dp）：
```kotlin
resources.displayMetrics.density
```
- [Android（国际化）多语言的实现和切换](https://blog.csdn.net/MakerCloud/article/details/83146600)
- [Android判断当前是否在主线程](https://www.cnblogs.com/genggeng/p/7524948.html)
- [Android中切换到主线程执行的方法](https://blog.csdn.net/lebulangzhen/article/details/108519311)
- [Android Intent 传递自定义对象](https://blog.csdn.net/LucasXu01/article/details/83786866)
- [再见！onActivityResult！你好，Activity Results API](https://www.toutiao.com/i6890511484770910728/)
- [onAttachedToWindow()在整个Activity生命周期的位置及使用](https://blog.csdn.net/guxiao1201/article/details/41517871)
- [android获取设备唯一标识完美解决方案](https://blog.csdn.net/aa1733519509/article/details/50053553)
- [android 6.0及以上动态权限的获取](https://blog.csdn.net/ygz111111/article/details/80281966)
- [安卓Q | 用户画像等功能受影响，Device ID禁用适配指南](https://msd.misuland.com/pd/3127746505234974860)
- [Android Q（10.0）上IMEI获取不到；Android Q（10.0）上OAID替代IMEI；OAID获取方式](https://blog.csdn.net/Kern_/article/details/107530583)
- [扒一扒安卓渲染原理](https://blog.csdn.net/qq_34696203/article/details/105815654)
- [Android App开发基础篇—数据存储(SP和文件)](https://blog.csdn.net/lyklykkk/article/details/56277569)
- [Android OpenGL ES绘制位图字体](http://blog.csdn.net/jackone12347/article/details/7710990)
- [Android粒子爆炸效果](http://blog.csdn.net/crazy__chen/article/details/50149619)
- [Google Mobile Ads SDK for Android](https://developers.google.com/admob/android/quick-start)
- [常用的android弹出对话框](https://www.cnblogs.com/liudeyun/p/android_1.html)
- [Android开发——ListView的运用](https://blog.csdn.net/cnicfhnui/article/details/51356741)
- [Android – Sectioned Headers in ListViews](https://w2davids.wordpress.com/android-sectioned-headers-in-listviews/)
- 取消Android Button字母自动全部大写：在XML布局中添加：`android:textAllCaps="false"`；或是在Kotlin代码中修改 **`isAllCaps`** 属性。另外还可以在style.xml文件中加入：`<item name="android:textAllCaps">false</item>`。加上这个配置后，就不需要为每个所创建的按钮都去配置一下了。
- [TextView设置部分文字大小、加粗、倾斜、颜色、背景、分行显示。](https://blog.csdn.net/joshua_love/article/details/53389338)
- [Android 应用开发（41）---EditText(输入框)详解](https://blog.csdn.net/zhangbijun1230/article/details/82284953)
- [Android -- Autosizing TextView 自动调整文字大小](https://blog.csdn.net/qq_24382363/article/details/99318544)
- Android中取消视图焦点并关闭软键盘：
```kotlin
// 清除焦点
view.clearFocus()
// 关闭输入法
(getSystemService(INPUT_METHOD_SERVICE) as InputMethodManager).hideSoftInputFromWindow(
    window.peekDecorView()?.windowToken, InputMethodManager.RESULT_UNCHANGED_SHOWN)
```
- [Android之点击空白处关闭软键盘](https://www.jianshu.com/p/8f4cfeee2caa)
- [android如何给整个视图view圆角显示](https://blog.csdn.net/hesong1120/article/details/52005895)
- [Android ViewPager实现图片标题轮播和点击事件](https://www.cnblogs.com/luhuan/p/8047098.html)
- [Android快速开发-选项卡](https://blog.csdn.net/yissan/article/details/72867722)
- [为ActionBar添加ActionBar按钮](https://segmentfault.com/a/1190000002497313)
- [在android中资源文件夹中添加一个新的图片资源](https://blog.csdn.net/ccf19881030/article/details/8957959)
- [Canvas之drawBitmap方法](https://www.jianshu.com/p/83074cef31bc)
- [Android——new Canvas(Bitmap)中对canvas和bitmap的理解](https://blog.csdn.net/xg1057415595/article/details/82885448)
- [Android Java代码中设置style属性--创建ProgressBar对象](https://blog.csdn.net/u012971339/article/details/46742243)
- [Android ProgressBar 圆形进度条颜色的设置](https://blog.csdn.net/shenggaofei/article/details/81010005)
- [Android-Java和JavaScript相互调用](https://segmentfault.com/a/1190000004895840)
- [Unity和android之间的通信（adt方式）](https://www.cnblogs.com/weiqiangwaideshijie/p/7715861.html)
- [Unity3D 调用 Android jar 包制作方法](https://blog.csdn.net/elyxiao/article/details/50781813)
- [Unity3D判断当前所在平台](https://www.cnblogs.com/wugang/p/3708569.html)
- 在Unity3D中生成定制的Gradle文件：点击File -> Build Settings... -> 选择Android平台，然后点击左下角的Player Settings，最后在右侧找到Publish Settings中可找到“Custom Gradle Template”，勾选上它就能生成`mainTemplate.gradle`，编辑它即可。
- [用MediaPlayer+TextureView封装一个完美实现全屏、小窗口的视频播放器](https://www.jianshu.com/p/420f7b14d6f6)
- [Android 简单定制一个视频播放器](https://blog.csdn.net/new_one_object/article/details/54839232)
- [Android manifest里Activity配置中android:configChanges属性的使用](https://blog.csdn.net/lkk790470143/article/details/79345971)
- [activity的横屏和竖屏设置](https://www.cnblogs.com/zhongyinghe/p/5289704.html)（android:screenOrientation属性：`landscape`是横向，`portrait`是纵向）
- [android-如何获得当前正在运行的activity的相关信息](https://blog.csdn.net/centralperk/article/details/7269326)
- [你必须弄懂的Intent Filter匹配规则](https://blog.csdn.net/mynameishuangshuai/article/details/51673273)
- [Android 上使用 iconfont 的一种便捷方案](https://www.cnblogs.com/dongweiq/p/5730212.html)
- [android 使用浏览器打开指定页面](https://blog.csdn.net/bzlj2912009596/article/details/80673555)
- [Android 8: Cleartext HTTP traffic not permitted](https://stackoverflow.com/questions/45940861/android-8-cleartext-http-traffic-not-permitted)（Android 8之后使用HTTP做网络通信的设置）
- [Android WebView 无法加载Https](https://www.jianshu.com/p/a7020518c111)
- [Android-工作遭遇-URLConnection原生请求http和https忽略证书](https://blog.csdn.net/ci250454344/article/details/82871965)
- [android 获取时间戳](https://www.jianshu.com/p/43dbc2e01376)
- Android 获取设备开机时间:
```java
 public static String getSystemStartupTime() {
        long time = System.currentTimeMillis() - SystemClock.elapsedRealtime();
        SimpleDateFormat format = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        Date d1 = new Date(time);
        return format.format(d1);
    }
```
- [Unity3D关于动态请求权限](https://docs.unity3d.com/Manual/android-manifest.html)
- [关于Calling View methods on another thread than the UI thread的错误](https://blog.csdn.net/lx448593jp/article/details/51971467)
- [Android反射机制实现与原理](https://www.cnblogs.com/wumingchen/p/5781844.html)
- [Android如何监听蓝牙耳机的按键事件](https://blog.csdn.net/kangear/article/details/40430673)
- [Android URL Scheme的学习和使用](https://www.jianshu.com/p/051eb1ad6328)
- [三种方式让 Android WebView 支持文件下载](https://blog.csdn.net/suyimin2010/article/details/82915942)
- [Android解析JSON，你真的需要三方库？](https://www.jianshu.com/p/fd82d3903e0b)
- [Android zip文件压缩与解压](https://blog.csdn.net/shuaizhigen/article/details/88671079)
- [Android蓝牙开发（一）之打开蓝牙和设备搜索](https://blog.csdn.net/huangliniqng/article/details/82185983)
- [Android蓝牙串口通信](https://www.jianshu.com/p/68fda037c336)
- [Android适配安卓6.0蓝牙通讯实现过程](https://www.jb51.net/article/93769.htm)
- [Android 低功耗蓝牙的多设备连接与数据接收，简单实现](https://blog.csdn.net/geanwen/article/details/73648721)
- [android6.0手机蓝牙与ble蓝牙模块通信](https://blog.csdn.net/y_15751004297/article/details/76559836)（发送数据部分搜索`sendDataThread`这个方法实现；接收数据部分搜索`mGattUpdateReceiver`中的`displayData`部分）
- [BLE中常用的UUID](https://blog.csdn.net/Smile_Qian/article/details/82084232)
- [使用Android Studio打包生成Jar包的方法(亲测可用)](https://blog.csdn.net/xiayiye5/article/details/79639044)（前半部分值得参考，后面用makeJar的部分在新版的Android Studio中不需要。我们先将当前工程设置为release模式，然后构建项目工程，最后直接在`app/build/intermediates/packaged-classes/release/`目录下就能找到`classes.jar`文件，也就是我们最终生成的jar包。）
- [Android Studio中添加jar包的方法](https://blog.csdn.net/yushuangping/article/details/81873630)（直接看方法三。另外对于最新版本的Android Studio，如果添加的是aar包，那么不需要选中包然后再右键选择Add As Library，因为aar包默认会加入到项目中。）
- [建立V7包库（Library）项目以供其他项目引](https://www.cnblogs.com/tonny-li/p/5048863.html)
- 让Android Studio支持`android.support.design.widget.TabLayout`类：在build.gradle(Module: app)中的**dependencies**语句块中添加`implementation 'com.android.support:design:28.0.0'`。
- [Android Support v4、v7、v13和AndroidX的区别及应用场景](https://blog.csdn.net/csdn_aiyang/article/details/80859771)
- [AndroidStudio_安卓原生开发_v4v7升级到androidx方法](https://www.toutiao.com/i7040706218612097573/)
- [新版Android Studio升级后将repositories的设置挪到了setting.gradle](http://events.jianshu.io/p/ee7c9889301a)
- [Android App Bundle (Android新的应用发布格式)](https://blog.csdn.net/weixin_37730482/article/details/83501586)
- 适用于Android X支持库的常用类：`androidx.constraintlayout.widget.ConstraintLayout`，`androidx.appcompat.app.AppCompatActivity`，`androidx.appcompat.app.AlertDialog`，`androidx.annotation.NonNull`，`androidx.annotation.Nullable`，`androidx.core.content.ContextCompat`，`androidx.core.app.ActivityCompat`。
- [2020 年Android入门教程之 RelativeLayout布局 004](https://zhuanlan.zhihu.com/p/150600297)
- [kotlin 构造函数、init、companion object用谁？](https://www.jianshu.com/p/e8c4ac3c8d87)
- [Kotlin之Lambda表达式](https://www.jianshu.com/p/5880bebe4661)（Kotlin中，lambda **类型** 的形参声明中也可以带有参数名，比如：
```kotlin
    /**
     * @param completion 这里completion的函数类型中就含有success这个形参名 
     */
    fun doAction(completion: (success: Boolean) -> Unit) {
        completion(true)
    }

        // 简略调用doAction
        doAction { Log.i(null, "Result: $it") }
        // 详细调用doAction
        doAction({ success: Boolean ->
            Log.i(null, "Result: $success")
        })
```
）
- Kotlin中创建匿名对象的方式：
```kotlin
private interface MyTestInterface {
    fun foo1()
    fun foo2(a: Int): Int
}

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        
        val testObj = object: MyTestInterface {
            override fun foo1() {
                Log.i(null, "Hello, world!!\n")
            }

            override fun foo2(a: Int): Int {
                return a + 1
            }
        }

        testObj.foo1()
        val data = testObj.foo2(10)
        Log.i(null, "data = $data")
    }
}
```
- [Android 底层的进程间同步机制](https://www.toutiao.com/i6906734816255934980/)
- [Android API广告反作弊需求 Native层获取 bootMark奔溃解析](https://blog.csdn.net/hanshengjian/article/details/120483858)
- [修改源码实现全局(无需root)注入躲开注入检测](https://bbs.pediy.com/thread-214589.htm)
- [Android利用ptrace实现Hook API](https://blog.csdn.net/u013234805/article/details/24796515)
- [怎么让 Android 程序一直后台运行，像 QQ 一样不被杀死？](https://blog.csdn.net/gf771115/article/details/77457053)
- [为什么后台应用切换，图标上有个锁一样的标志？！！](http://bbs.blackshark.com/forum.php?mod=viewthread&tid=103764)
- Android Studio上要剖析GPU性能，得使用[Android GPU Inspector](https://gpuinspector.dev/)。官方介绍文档：[GPU Debugger](http://tools.android.com/tech-docs/gpu-profiler)
- [分析 Android 耗电原理后，飞书是这样做耗电治理的](https://www.toutiao.com/article/7096085243337130527/)
- Android Studio中用自带的NDK写C语言获得不同架构平台下的语法高亮：点击左侧边缘处的“Build Variants”，然后选择“Active ABI”，如果选用 **`arm64-v8a`**，则ARM64架构宏下的代码能正常显示高亮；如果选择 **`x86_64`**，则x64宏下的代码会正常显示语法高亮。
- macOS下adb工具所在路径：`~/Library/Android/sdk/platform-tools/adb`
- Windows 10下`adb.exe`所在路径：`%USERPROFILE%/AppData/Local/Android/Sdk/platform-tools`

<br />

## Android异步消息处理

```kotlin
import android.os.Handler
import android.os.Looper

        Handler(Looper.getMainLooper()).post {
            // TODO: Implement your code...
            if (someCondition) return@post

            // Do other things...
        }
```

<br />

## Android Studio中用gradle(Module:app)指定ABI filter：

```gradle
    versionCode 1
    versionName "1.0"

    externalNativeBuild {
            cmake {
                // 对于ARMv7架构使用NEON技术，并且对于32位的ARM执行模式使用ARM指令集而不是默认的Thumb指令集
                arguments "-DANDROID_ARM_NEON=ON", "-DANDROID_ARM_MODE=arm"
 
                // C语言使用GNU17标准
                cFlags "-std=gnu17", "-Os"
            }
            ndk {
                // Specifies the ABI configurations of your native
                // libraries Gradle should build and package with your APK.
                abiFilters 'x86_64', 'armeabi-v7a', 'arm64-v8a'
            }
    }
```

<br />

## Android Studio中使用gradle(Module:app)指定的NDK版本与CMake版本：

```gradle
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
    kotlinOptions {
        jvmTarget = '1.8'
    }

    externalNativeBuild {
        cmake {
            path file('src/main/cpp/CMakeLists.txt')
            version '3.18.1'
        }
    }
    ndkVersion '22.1.7171670'

    buildFeatures {
        viewBinding true
    }
```

其中，以上代码指定了使用CMake 3.18.1版本，以及使用22.1.7171670版本的NDK。

<br />

如果用NDK编译C艹代码，那么需要在`Application.mk`中添加`APP_STL := gnustl_static`，否则大部分C艹标准库都无法找到。而如果要用当前LLVM的runtime的STL库的话，可以使用：`APP_STL := c++_static`。

<br />

## Android手机使用技巧

- 进入开发者模式：一般Android手机通过进入设置，然后点击“系统”或“关于”，再进入后**多次**点击系统版本号即可进入开发者模式。
- 截屏：Motorola Edge S是通过 **`电源键 + 音量键-`** 来截屏；诺基亚则可直接在下拉菜单栏里找到截屏按钮。
- Android手机常用App：**`谷歌拼音输入法`**，**`Google日语输入法`**，**`个人所得税（国家税务总局发布）`**，**`Fa米家`**，**`网络管家`**，**`国家反诈中心`**

