caleydo-doc
===========

User documentation for (Caleydo)[http://caleydo.org], accessible via: http://help.caleydo.org. 

Syntax: http://dynalon.github.io/mdwiki/#!quickstart.md

Layout: http://dynalon.github.io/mdwiki/#!layout.md

Major versions are hosted in directories corresponding to the version, such as 3.0 and 3.1. 

In case of a version update of mdwiki, download the release and replace the index.html with mdwiki.html. To keep google analytics working, paste the following code right before </head> into the html file:

```
<script>
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

  ga('create', 'UA-45998043-1', 'caleydo.org');
  ga('send', 'pageview');

</script>
```

To get favicons add this to the html header:

```
 <link rel="shortcut icon" type="image/x-icon" href="i/favicon.ico"/>
 <link rel="apple-touch-icon" href="i/favicon.png"/>
```


To edit the menu edit navigation.md. 
