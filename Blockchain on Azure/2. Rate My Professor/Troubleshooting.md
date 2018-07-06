# Troubleshooting #
This page contains tips to solve issues that you may encounter along the way.


## Excercise 4 step 3 ##

### Issue: ###
Running `npm install` fails

The error contains a message that looks like this:  
***The imported project “C:\Microsoft.Cpp.Default.props” was not found***

### Fix: ###
The Windows build tools that are called during this installation are configured to use a specific Visual Studio version to compile. If you have a different version, you may get errors.

The solution is to map the build tools to your Visual Studio version.  

Try to run:  
`node-gyp configure --msvs_version=2015`  
And then run:   
`npm install`

