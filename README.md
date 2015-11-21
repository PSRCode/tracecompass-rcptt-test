# tracecompass-rcptt-test
Blackbox UI test using RCPTT for Trace Compass

## How to run ?

You can run this project either via the RCP Testing Tool or via maven.

### Local maven run

Either create a symlink to a trace-compass RCP or extract one under
./rcp/trace-compass.

####Symlink creation

Let's say the rcp is located inside /tmp/rcp/trace-compass.

The folder tree of /tmp/rcp:
```
$ tree /tmp/rcp/ -d  -L 2
/tmp/rcp/
└── trace-compass
    ├── configuration
    ├── features
    ├── p2
    ├── plugins
    └── readme
```

The corresponding symlink:
```
ln -s /tmp/rcp/trace-compass ./rcp/trace-compass
```

Run inside the root of this project:
```
mvn package
```

Maven will take care of all necessary dependencies and run the pre-selected test
suites.

Results will be located under ./target.

### CI maven run 
#### Jenkins

Test can be run on a Jenkins instance by using the pom-jenkins.xml.

The local Data should be placed under $WORKSPACE/Data.

The trace-compass rcp (fully extracted) should be placed under
$WORKSPACE/rcp/trace-compass.
