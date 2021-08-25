# Example Directory Structure - NOT Example Project!

This repository features the expected directory structure of an OpenEndpoints application.
OpenEndpoints is an open source platform for building everything around XSL transformation.
Visit https://openendpoints.io for more information.

## This is NOT a working example application

Note that this is **not** a working example application. The focus is only on describing expected syntax of files. Example projects can be found here: https://doc.openendpoints.io/configuration/example-applications

## Expected xml sometimes less strict than xsd
The software is a little less strict than what is written in the xsd: Don't be surprised if you find working examples where the order of elements is slightly different from what is described in the xsd.

## Additional files silently ignored

Any additional files which are present in the application directory, but not required by the software, are silently ignored. In many of our example applications we have an additional **project directory** - which contains project related ressources, but is ignored by the software.

The same is **sometimes** true for additional attributes added to the xml. Usually this doesn't make sense, but when using the <application-introspection> data source it can be practical to give an <endpoint-folder> additional attributes, for example. If in doubt, simply try out whether the software silently ignores such an additional feature.