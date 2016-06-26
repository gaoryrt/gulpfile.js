# gulpfile.js
自用gulpfile
***
##确认文件夹结构如下
```
-DIST
gulpfile.js
-node_modules
package.json
-app
	index.html
	-css
		main.scss
	-img
	-js
		dropdown.js
		scroll.js
```
***
##package.js要有这些
```
"devDependencies": {
    "gulp": "^3.9.1",
    "gulp-clean-css": "^2.0.10",
    "gulp-concat": "^2.6.0",
    "gulp-concat-css": "^2.3.0",
    "gulp-connect": "^4.1.0",
    "gulp-imagemin": "^3.0.1",
    "gulp-merge-link": "^0.1.3",
    "gulp-open": "^2.0.0",
    "gulp-sass": "^2.3.2",
    "gulp-sequence": "^0.4.5",
    "gulp-uglify": "^1.5.4",
    "gulp-uncss": "^1.0.5",
    "gulp-zip": "^3.2.0"
  }
```
## 使用
首先`npm i`

`gulp build`：  
会合并js和css，然后在html中替换原有的对资源的多个请求，然后压缩img文件夹中的图片，复制到DIST文件夹中，最后压缩该文件夹，压缩文件名为执行时间。

`gulp watch`：  
开本地服务器预览app/index.html文件，然后监听scss，js，img(文件夹内容)，html的改变实时更新浏览器。
