# DelayClickListener
[![](https://jitpack.io/v/xuanu/DelayClickListener.svg)](https://jitpack.io/#xuanu/DelayClickListener)
点击事件，两次之间不可用

> 实现方法：[android 自定义组件事件点击，防止按钮重复点击](https://juejin.im/entry/577cd7b88ac2470061c21917)

### 实现原理：
> 重写View的OnClickListener方法，在指定的间隔时间内，拦截点击事件。

### 使用方式
```
OnClickFastListener();//默认间隔900ms
OnClickFastListener(long);//指定间隔
***
tempView.setOnClickListener(new OnClickFastListener() {
      @Override
      public void onFastClick(View v) {
         System.out.println(System.currentTimeMillis());
         }
     });
```
### 添加依赖
Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}Copy
Step 2. Add the dependency

	dependencies {
	        compile 'com.github.xuanu:DelayClickListener:1.0'
	}
