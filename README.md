DotNet_Extensibility
=========

## Intension:
Copy a compiled extension dll to a specific folder. The application to extend will be look inside this directory for specific extension objects and will load them and initialize through several functions. No Recompilation for function extension get necessary.


## How to use:

### How to build an extension
1. Embed tud.mci.tangram.TangramLector.Extension
2. Extension object must be an AbstractSpecializedFunctionProxyBase (tud.mci.tangram.TangramLector.SpecializedFunctionProxies)
3. the constructor must be without parameters

#### ATTENTION: 
Don’t let the compiler add local copies of resources of your extension that will be sent to the extension by the framework. This will lead to problems in checking the wright object types in initialization function.


--	TODO: build a small workflow

Using Project should include the folders into the output directory via xcopy

So add the xcopy as "post build process"

XCOPY "$(SolutionDir)EXT" "$(TargetDir)Extensions" /H /S /Y /C /I /Q /R


### Example

--	TODO: build a small example



## You want to know more?

--	TODO: build help from code doc

For getting a very detailed overview use the [code documentaion section](/Help/index.html) of this project.

