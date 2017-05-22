# 自定义 Spinner

自定义继承TextView,效果类似 spinner
在[nice-spinner](https://github.com/arcadefire/nice-spinner)的基础上增加了设置 layout 的构造方法，感谢作者

## 例子
![image](/gifs/nice-spinner.gif )  

## 使用

- Step 1. 把 JitPack repository 添加到build.gradle文件中 repositories的末尾:
```
repositories {
    maven { url "https://jitpack.io" }
}
```
- Step 2. 在你的app build.gradle 的 dependencies 中添加依赖
```
dependencies {
	compile 'com.github.wenchaosong:customSpinner:1.0.0'
}
```
xml

	<view.customspinner.NiceSpinner
        android:id="@+id/nice_spinner"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="请选择"
        android:lines="1"/>

代码

	NiceSpinner niceSpinner = (NiceSpinner) findViewById(R.id.nice_spinner);
        List<String> dataset = new LinkedList<>(Arrays.asList("One", "Two", "Three", "Four", "Five"));
        niceSpinner.attachDataSource(R.layout.child, dataset);
    