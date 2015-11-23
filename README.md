# tracecompass-rcptt-test
Blackbox UI test using RCPTT for Trace Compass

## How to run ?

You can run this project either via the RCP Testing Tool or via maven.

### Local maven run
By default maven will look for the RCP under ./rcp/trace-compass .

This can be overridden by providing a -DauthPath="/path/to/rcp/"

```
mvn package -DautPath="/tmp/rcp/trace-compass/"
```

By default maven will lokk for Data in ./Data .
This can be overridden by providing a -DdataPath="/path/to/data/folder"
```
mvn package -DdataPath="/tmp/data/"
```

Both argument can be combined.
```
mvn package -DautPath="/tmp/rcp/trace-compass/" -DdataPath="/tmp/data"
```

Maven will take care of all necessary dependencies and run the pre-selected test
suites.

Results will be located under ./target.

### Via RCPTT

Add an AUT (Application Under Test) [More detail here](https://www.eclipse.org/rcptt/documentation/userguide/getstarted/).

If you are not using the default path make sure to pass the correct arguments to
the AUT in the run configurations.

![](http://i.imgur.com/XH02fa9.png)
