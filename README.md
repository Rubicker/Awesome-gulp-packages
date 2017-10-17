# Awesome-gulp-packages

### [gulp-load-plugins](https://www.npmjs.com/package/gulp-load-plugins)

  > Loads gulp plugins from package dependencies and attaches them to an object of your choice.

  再也不需要在开头写一堆 `require` 了 🤘
  
  用法如下：
  
  ```js
  var gulp = require('gulp')
  var $ = require('gulp-load-plugins')()
 
  gulp.task('styles', function() {
    return gulp.src('src/styles/bootstrap.less')
      .pipe($.less({strictMath: true}))
      .pipe($.autoprefixer([
        'Android 2.3',
        'Android >= 4',
        'Chrome >= 20',
        'Firefox >= 24',
        'Explorer >= 8',
        'iOS >= 6',
        'Opera >= 12',
        'Safari >= 6']))
      .pipe($.csscomb())
      .pipe(gulp.dest('./build/css'))
  });
  
  ```
  
 ### [gulp-csscomb](https://www.npmjs.com/package/gulp-csscomb)
  
  > Format CSS coding style
    
  可以自定义规则，方便整理输出的 CSS 文件
