# Problem report

As it is right now, the import will fail, since webpack has no way of identifying what the import statement contains. Which means it won't bundle that package.

If you replace x with its content in the import, in other words ```import("@material-ui/core/Dialog")``` it will work

My suggestion is having an option in webpack's configuration file to include an array of packages, like this ```["@material-ui/core/Dialog", ...]```. The packages specified in this array will be bundled regardless of whether they're required in the source code or not.
