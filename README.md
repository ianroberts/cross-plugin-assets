# Cross-plugin asset references in Grails

This is a Grails application to demonstrate issue bertramdev/asset-pipeline#330.  It consists of a Grails application and two plugins, where one plugin depends on the other, and the app depends on both:

```
         core plugin
          ^       ^
          |       |
  skin plugin     |
          ^       |
          |       |
       main application
```

The "skin" plugin attempts to refer to CSS assets provided by the "core" plugin, but this does not work as expected, at least not in the versions tested (Grails 6.0, asset-pipeline 4.4.0).
