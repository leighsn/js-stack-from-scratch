JS Ecosystem Notes
+ Gulp - task runner - "streaming build system" - lets you automate tasks. Make gulpfile.js at root directory that holds the tasks you want to run

```
gulp.task("this task", ["other task", "another task"], function(){
  //stuff that this task will do after other tasks finish
})
```

```
gulp.task('copyHtml', function() {
  // copy any html files in source/ to public/
  gulp.src('source/*.html').pipe(gulp.dest('public'));
})
```

```
gulp.watch('src/**/*.js', ['task'])
//whenever a file matching the path changes, run these tasks
```

+ Running `gulp` will run

```javascript
gulp.task('default', ['dependencyTasks'], function(){
  //task
  })
```
this will run dependencyTasks first
  
+ Babel configuration can be kept in root of package.json object OR stored in .babelrc file at project root
+ Gulp and Babel will create a /lib folder by default to store transpiled JS code
