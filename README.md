# gretl-docs


Approach:

- on-demand
- Parameter: Version (defualt=master/main)
- falls master/main wird gh pages aktualisiert
- immer wird ein package deployed mit branch-(und commit id von gretl) im zip-namen oder so ähnlich.
- 


Dokumentation für [_GRETL_](https://github.com/sogis/gretl).

- https://gretl.app
- https://sogis.github.io/gretl-docs


## Usage

Gradle:

```
javadoc {
    source = sourceSets.main.allJava
    title = null
    destinationDir = file("./doc/")
    
    include 'ch/so/agi/gretl/tasks/**'
    options.doclet = "ch.so.agi.gretl.doclet.GretlDoclet"
    options.docletpath = [file("/Users/stefan/sources/gretl-doclet/build/libs/gretl-doclet.jar")]    
}
```


## Develop

```
quarto preview 
```

```
### DummyTask

{{< include srcdoc/_ch.so.agi.gretl.doclet.test.DummyTask.md >}}
```

