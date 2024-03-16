Powered by [Hugo](https://gohugo.io/) & [Congo](https://github.com/jpanther/congo)

## Local Host
```
hugo server
```

## Custom Settings

```
│
│  .hugo_build.lock
│  config.yaml
│  desktop.ini
│  netlify.toml
│  README.md
│  
├─.github
│  └─workflows
│          gh-pages.yml
│          
├─archetypes
│      default.md
│      external.md
│      
├─assets
│  │  site.webmanifest
│  ├─css
│  │  │  main.css
│  │  ├─compiled
│  │  └─schemes: color Scheme
│  ├─icons: all icon.svg files
│  ├─img
│  │      khy.jpg: "Home" Page photo
│  │      logo.png
│  ├─js
│  └─lib
│              
├─config: website configuration
│  └─_default
│          config.toml: (almost need not change after website building completed)
│          languages.en.toml:  author info, date style, language, ...
│          markup.toml: make up (almost need not change)
│          menus.en.toml: main menu (may change a lot)
│          module.toml: hugoversion (need not change)
│          params.toml: theme options(may change a lot), colorScheme, header, footer, ...
│          
├─content: website content
│  │  _index.md: Home
│  ├─about: About
│  └─blog: Blog
│          
├─data
│      
├─i18n: different language style
│      
├─layouts: website layout
│              
├─resources
│  └─_gen
│      ├─assets
│      └─images
│              
├─static: including icon, pic in blog, pdf, ...
│  │  ...
│  ├─blog: pic in Blog
│  ├─file4share: delete in future
│  ├─file: files for sharing
│  └─store: draft store
│              
└─themes: Hugo Theme
```