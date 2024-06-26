## IBD Benchmark project source code

List of file:

```Program.cs```         Program entrance, load configurations, check inputs, then run program.

```GroupCaller.cs```     Group calling module, organized to call core functions to run a full set of test.

```BinCalculator.cs```   Core calculation module, detailed calculation methords could be found here.

```Loader.cs```          Loading unit, parsers could be modified here for differet formats.

```Utl.cs```             Supporting utility module.

```siteCoverage.cs```    IBD distribution module.

## Compiling

### windows:

Download code files, compile with Microsoft Visual Studio, use Release version for better performance.

### Linux and macOS:

Precompiled versions for ubuntu 18, ubuntu 22 and windows 10 are already uploaded to directory ```/IBD_Benchmark_ExperiencePackage/```. 

However if none of those version work, you can compile the source code. As following:

Download the code files, use mono compiler ```mcs -out:IBD_BM *.cs```.

If you have not installed mono compiler, please follow the guide in https://www.mono-project.com/ to install.

## Execution
### windows
```./IBD_BM``` or ```./IBD_BM config.txt```

You may also execute the program by double clicking the IBD_BM.exe if ```Config.txt``` exists in the same directory.

### linux
```./IBD_BM``` or ```./IBD_BM config.txt```

### macOS
```mono IBD_BM``` or ```mono IBD_BM config.txt```

Note, input file paths and most configurations could be modified in ```Config.txt```, it may not be necessary to modify in the code.


## Input
This program takes a configuration file path as input, if the path is not given, it will try to read ```Config.txt``` in the same directory.

After successfully located the configuration file, the program will load all paths and other configurations, and start generate results.

Detial configurations and example could be found in ```/IBD_Benchmark_ExperiencePackage/Config.txt```

## Output
The result could be found in ```[reported_Path].IBD_BM_Result.txt```.

```[reported_Path]``` is the IBD detection tool's result path, refers to ```reported_Path``` in the configuration file.
