# Gulp Build Boilerplate

Use this boilerplate to build your web app with Gulp.

**What can it do**
* Generate site's files, compile HTML pages with [Panini](https://www.npmjs.com/package/panini);
* Compile, minify, autoprefix SCSS;
* Concatenate, uglify JavaScript and include js-files with [Rigger](https://www.npmjs.com/package/rigger) include engine;
* Optimizes images;
* Moves your static files into your `dist` folder;
* Creates compressed and uncompressed versions of your CSS & JavaScript files;
* Watches for changes in the files and automatically reload updates.

## Usage
1. Navigate to your project directory;
2. Install dependencies by running `npm install`;
3. Once it done installing, run `gulp` and you're ready to go!

## List of tasks
### `gulp html`
Compiles HTML pages using HTML partials `src/tpl/partials` and layouts `src/tpl/layouts`.

### `gulp css`
Compiles SCSS to CSS, [applies](https://www.npmjs.com/package/gulp-autoprefixer) prefixes, [beautifies](https://www.npmjs.com/package/gulp-cssbeautify) CSS for uncompressed version, [minifies](https://www.npmjs.com/package/gulp-cssnano) for compressed version, and [removes](https://www.npmjs.com/package/gulp-strip-css-comments) any comments in CSS.

### `gulp js`
[Concatenates](https://www.npmjs.com/package/rigger) JavaScript files, [uglify (minify)](https://www.npmjs.com/package/gulp-uglify) a production ready JavaScript.

### `gulp images`
[Optimizes](https://www.npmjs.com/package/gulp-imagemin) all type of images.

### `gulp clean`
[Deletes](https://www.npmjs.com/package/del) existing `dist` directory and its contents.

### `gulp build`
Clean `dist` folder and runs `html`, `css`, `js`, `images` tasks in parallel.

### `gulp watch`
Watches for any files in `src` folder to change, then runs the corresponding task. [Starts](https://www.npmjs.com/package/browser-sync) the server. 

### `gulp` or `gulp default`
Alias to run `watch` task.