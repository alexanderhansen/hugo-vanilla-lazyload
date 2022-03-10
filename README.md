# Add awesome image libraries to your hugo project

Currently the folllowing libraries are integrated:

- [vanilla-lazyload](https://github.com/verlok/vanilla-lazyload)
- [lightense](https://github.com/sparanoid/lightense-images)


## Add as a module to your hugo installation by adding:

```
[module]
  [[module.imports]]
    path = "github.com/alexanderhansen/hugo-awesome-images"
```

### Include the libraries you want to use in your script loading e.g. ```<head>```

```
  {{ $lazyload := resources.Get "js/lazyload.min.js" }}
  <script src="{{ $lazyload.Permalink }}"></script>
  
  {{ $lightense := resources.Get "js/lightense.min.js" }}
  <script src="{{ $lightense.Permalink }}"></script>
```

### Put the library partials right before your closing ```<body>``` tag.

```
{{- partial "lazyScript.html" . -}}
{{- partial "lightenseScript.html" . -}}
```

### Use the shortcode ```imgLazy``` anywhere in your content any just use it as hugo's build in ```figure``` shortcode.

```
{{< imgLazy src="..." alt="..." >}}
```

## Local Development

After cloning run ```npm install && npm run dist```

And add to your hugo config:

``` 
[module]
  replacements = "github.com/alexanderhansen/hugo-awesome-images -> /your/working/copy/hugo-awesome-images"
  [[module.imports]]
    path = "github.com/alexanderhansen/hugo-awesome-images"

```