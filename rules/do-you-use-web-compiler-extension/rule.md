---
type: rule
title: Do you use Web Compiler extension?
uri: do-you-use-web-compiler-extension
created: 2018-06-19T01:38:21.0000000Z
authors:
- id: 76
  title: Eden Liang

---

 You can use Visual Studio's Web Compiler extension to create a bundle.css and test if CSS was compiled successfully. 
 
More information and download at [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.WebCompiler).
 ![web-compiler-find-error.png](web-compiler-find-error.png) Figure: Web Compiler can find missing curly braces Unfortunately different kinds of errors, like are not caught.  ![web-compiler-didnt-find-error.png](web-compiler-didnt-find-error.png) Figure: Curly braces in the wrong place, but still compiled successfully 

In addition, Gulp is wrongly successful too:
![gulp-didnt-find-error.png](gulp-didnt-find-error.png) Figure: Gulp couldn't find the curly braces error​

