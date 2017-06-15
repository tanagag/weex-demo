# Hacker News App


https://github.com/weexteam/weex-hackernews

以下是个人整理的启动步骤

npm run build  打包js (不带--watch)

npm run dev  打包js(带--watch)建议使用，刷新可以看到效果，因为页面引用的是打包后的js

npm run copy:android 自动复制打包的js到android 也可以手动复制到android-studio中运行虚拟机并且打包成apk

npm run serve 即可运行

综合简介步骤
1, npm run dev
2, npm run serve



[中文版说明文档](./README.zh.md)

A mobile app for [Hacker News](https://news.ycombinator.com/), which is powered by Weex and Vue.

## Preview

Use [Weex Playground App](https://weex.apache.org/playground.html) to scan the QR code below.

![QR Code](./qrcode.jpg)

> The content of this QR code is `http://whatever.cn?_wx_tpl=https://raw.githubusercontent.com/weexteam/weex-hackernews/master/ios/assets/index.js` , please make sure your phone can assess GitHub.

## Compile

Install the dependencies:

```
npm install
```

Compile the source code:

+ `npm run build` # Compile the source code for web platform and native platform.
+ `npm run dev` # Watch mode for `npm run build`.

Copy the bundle file:

+ `npm run copy:android` # Copy generated bundle file to the assets of Android project.
+ `npm run copy:ios` # Copy generated bundle file to the assets of iOS project.
+ `npm run copy` # Run both `copy:andriod` and `copy:ios`.

More npm scripts will be find in the `package.json`.

### Start Web Service

```
npm run serve
```

The server is listening on 1337. Visit http://127.0.0.1:1337/index.html can preview the app on browser.

### Run The Android Project

First you should install [Android Studio](https://developer.android.com/studio/index.html) and Android SDK.

Assuming you have configured the Android development environment properly, just use Android Studio to open the project in the `android` folder, and run the app as other normal Android projects.

### Run The iOS Project

First you should [setup the iOS develop environment](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppStoreDistributionTutorial/Setup/Setup.html) and install the [CocoaPods](https://guides.cocoapods.org/using/getting-started.html).

Enter the `ios` path, use CocoaPods to install dependencies:

```
pod install
```

Open the project in the `ios` folder by Xcode, you could run the app on the simulator.

> NOTE: If you want to run the app on real device, you also need to setup your own signing configuration.
