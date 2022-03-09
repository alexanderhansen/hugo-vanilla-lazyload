# Use vanulla-lazyload in your hugo project


Add as a module to your hugo installation by adding:

```
[module]
  [[module.imports]]
    path = "github.com/alexanderhansen/hugo-vanilla-lazyload"
```

If you want to make adjustments to the module, clone the repository first.

After cloning run ```npm install && npm run dist```

And add to your hugo config:

``` 
[module]
  replacements = "github.com/alexanderhansen/hugo-vanilla-lazyload => /your/working/copy/hugo_vanilla_lazyload"
  [[module.imports]]
    path = "github.com/alexanderhansen/hugo-vanilla-lazyload"

```