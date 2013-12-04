# PhoneGap WebView background color plugin for iOS

by [Eddy Verbruggen](http://www.x-services.nl)

* These instructions are for PhoneGap 3.0.0 and up.

## 0. Index

1. [Description](https://github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin#1-description)
2. [Installation](https://github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin#2-installation)
	2. [Automatically (CLI / Plugman)](https://github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin#automatically-cli--plugman)
	2. [Manually](https://github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin#manually)
	2. [PhoneGap Build](https://github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin#phonegap-build)
3. [Usage](https://github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin#3-usage)
4. [Testing](https://github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin#4-testing)
5. [License](https://github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin#5-license)

## 1. Description

This plugin allows you to change the background color of the iOS WebView.

* Tested on iOS 6.1 and 7.0.
* Supports all colors, just pass a valid hex value like #FF0000.
* Compatible with [Cordova Plugman](https://github.com/apache/cordova-plugman).
* Pending official support by [PhoneGap Build](https://build.phonegap.com/plugins).

iOS 7 screenshot - original:

![ScreenShot](https://raw.github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin/master/screenshot-original.png)

iOS 7 screenshot - color changed to #FFFFFF (white):

![ScreenShot](https://raw.github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin/master/screenshot-changed.png)

## 2. Installation

### Automatically (CLI / Plugman)
WebViewColor is compatible with [Cordova Plugman](https://github.com/apache/cordova-plugman), compatible with [PhoneGap 3.0 CLI](http://docs.phonegap.com/en/3.0.0/guide_cli_index.md.html#The%20Command-line%20Interface_add_features), here's how it works with the CLI:

```
$ phonegap local plugin add https://github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin.git
```
or
```
$ cordova plugin add https://github.com/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin.git
```
run this command afterwards:
```
$ cordova prepare
```

WebViewColor.js is brought in automatically. There is no need to change or add anything in your html.

### Manually

1\. Add the following xml to your `config.xml` in the root directory of your `www` folder:
```xml
<feature name="WebViewColor">
	<param name="ios-package" value="WebViewColor" />
</feature>
```

2\. Grab a copy of WebViewColor.js, add it to your project and reference it in `index.html`:
```html
<script type="text/javascript" src="js/WebViewColor.js"></script>
```

3\. Download the source files and copy them to your project.

Copy `WebViewColor.h` and `WebViewColor.h` to `platforms/ios/<ProjectName>/Plugins`

### PhoneGap Build

WebViewColor will soon work with PhoneGap build too! Compatible with PhoneGap 3.0.0 and up.

You can implement the plugin with these simple steps.

1\. Add the following xml to your `config.xml` to always use the latest version of this plugin:
```xml
<gap:plugin name="nl.x-services.plugins.ioswebviewcolor" />
```
or to use this exact version:
```xml
<gap:plugin name="nl.x-services.plugins.ioswebviewcolor" version="1.0" />
```

2\. Nothing.
WebViewColor.js is brought in automatically. There is no need to change or add anything in your html.


## 3. Usage
```html
  <button onclick="window.plugins.webviewcolor.change('#FF0000')">change to #FF0000</button>
  <button onclick="window.plugins.webviewcolor.change('#00FF00', function(){alert('color was changed!')}">change to #00FF00</button>
```


## 4. Testing
The background color change can best be seen by allowing overscroll (rubber banding), so when you swipe up and down, the WebView background is shown.

Another possibility is adding a `<select>` or `<input type="date"`.
When clicked, the background color shines through the native picker UI.


## 5. License

[The MIT License (MIT)](http://www.opensource.org/licenses/mit-license.html)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/EddyVerbruggen/iOSWebViewColor-PhoneGap-Plugin/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

