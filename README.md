# Initialize Project
1. to init project as scala, use init command with the option below
```
$ gradle init --type scala-library
```

2. to execute main method, apply "application" plugin and specify the name of main class
```
apply plugin: 'application'
....
mainClassName = 'Main'
```

3. to enable incremental compile, add following descriptions.
```
tasks.withType(ScalaCompile) {
    ScalaCompileOptions.metaClass.daemonServer = true
    ScalaCompileOptions.metaClass.fork = true
    ScalaCompileOptions.metaClass.useAnt = false
    ScalaCompileOptions.metaClass.useCompileDaemon = false
}
```

FYI:
Official https://guides.gradle.org/building-scala-libraries/
Blog     http://etc9.hatenablog.com/entry/2015/05/30/172342
