## Sublime API Completions Package

This package aim at provide a simpler way to build own auto-completion.

**auto-completion** is lightweight, not complex, simpler than **snippets**.

This package also provide several APIs completions such as JavaScript, jQuery API and Bootstrap Classes collect by me.


## Features

手刻的浪漫

#### JavaScript and jQuery

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/JavaScript-and-jQuery/demo1.gif)

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/JavaScript-and-jQuery/static1.jpg)

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/JavaScript-and-jQuery/static2.jpg)

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/JavaScript-and-jQuery/static3.jpg)

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/JavaScript-and-jQuery/static4.jpg)

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/JavaScript-and-jQuery/static5.jpg)

#### Twitter Bootstrap

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/bootstrap-demo/demo1.gif)

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/bootstrap-demo/static1.jpg)

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/bootstrap-demo/static2.jpg)

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/bootstrap-demo/static3.jpg)

#### HTML / HTML5

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/HTML/html-demo1.gif)

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/HTML/static1.jpg)

![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/HTML/static2.jpg)


## Why this package?

* Compared with `*.sublime-snippet` files:

  Simpler to build own API completions.

* Compared with `*.sublime-completions` files:
  
  * **speak in English**:

      It seems like when scope matched would be override completions provide by sublime itself. refer to issue #3.

  * **speak in Chinese**:

      一但 scope 匹配成功之後，雖然自製的 auto-completion 能更順利工作；但是它會覆蓋掉原本 auto-completion，只有在自製的辭彙完全沒匹配，才會顯示原本的 auto-completion，而不是將它們融合。


## Setting

The `sublime-completions` folder is my collection of APIs You might want to enable or disable it.

Your own APIs, place in `/Sublime Text 2/Data/Packages/User/API-completions-${filename}.sublime-settings` is recommend.

```js
{
  "completion_active_list": {
    // As filename `API-completions-${filename}.sublime-settings`.
    "jQuery": false,
    "JavaScript": false,
    "twitter-bootstrap": false
  },
  "completion_active_extend_list": {
    // As filename `API-completions-${filename}.sublime-settings`.
    "myGlossary": true,
    "myAngularJS": true,
    "myjQuery": true,
    "myJavaScript": true,
    "mytwitter-bootstrap": true,
    "HTML": true
  }
}
```

After you enable, disable or added new completions, you might need restart your Sublime Text.


## API References

* jQuery Version: 1.9

  * http://oscarotero.com/jquery/

* JavaScript

  * http://overapi.com/javascript/
  * http://www.w3schools.com/js/

* Twitter Bootstrap Version 2.3.2

  * http://twitter.github.io/bootstrap/index.html

* HTML / HTML5

  * http://devdocs.io/html-html5/

## Installation

* Using **Package control** to install.

  ![](https://raw.github.com/Pleasurazy/Sublime-JavsScript-API-Completions/master/README/UsingPackageControl.jpg)

* Waiting download from **Github**.

* Happy programming.


## Relevant issues

> How to trigger completion hint when every typing?

Open file `Packages/User/Preferences.sublime-settings` or click `Setting - User` from menu. In my case, I just setup the `auto_complete_triggers` property as follow:

```js
  "auto_complete_triggers":
  [
    {
      "characters": "qazwsxedcrfvtgbyhnujmikolpQAZWSXEDCRFVTGBYHNUJMIKOLP",
      "selector": "text, source, meta, string, punctuation, constant"
    }
  ],
```

It will active most of scope triggers and most of characters.