# TESTING

```json
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "devserver": "live-server",
    "start": "npm-run-all --parallel devserver watch:sass",
    "watch:sass": "sass ./sass/main.scss ./css/style.css -w",
    "compile:sass": "sass ./sass/main.scss ./css/style.comp.css",
    "concat:css": "concat -o ./css/style.concat.css ./css/icon.css ./css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' ./css/style.concat.css -o ./css/style.prefixed.css",
    "compress:css": "sass ./css/style.prefixed.css ./css/style.css --style=compressed",
    "build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
  },

```

[Next: Warping](./11-warping.md)
