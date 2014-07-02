Math.NET Filtering
==================

Math.NET Filtering is an opensource **geometry library for .Net, Silverlight and Mono**.

Supports Mono and .NET 4.0 and 3.5 on Linux, Mac and Windows, the portable build (PCL) also Windows 8, Silverlight 5, Windows Phone/SL 8, Windows Phone 8.1, and Xamarin Android/iOS.

Math.NET Filtering is covered under the terms of the [MIT/X11](LICENSE.md) license. You may therefore link to it and use it in both opensource and proprietary software projects.

**[Release Notes & Changes](RELEASENOTES.md)**

Installation Instructions
-------------------------

The recommended way to get Math.NET Filtering is to use NuGet. The following packages are provided and maintained in the public [NuGet Gallery](https://nuget.org/profiles/mathnet/):

- **MathNet.Filtering** - core package, including .Net 4, .Net 3.5 and portable/PCL builds.

Supported Platforms:

- .Net 4.0, .Net 3.5 and Mono: Windows, Linux and Mac.
- PCL Portable Profiles 47 and 344: Windows 8, Silverlight 5, Windows Phone/SL 8, Windows Phone 8.1.
- Xamarin: Android, iOS

Building Math.NET Filtering
---------------------------

If you do not want to use the official binaries, or if you like to modify, debug or contribute, you can compile Math.NET Filtering locally either using Visual Studio or manually with the build scripts.

* The Visual Studio solutions should build out of the box, without any preparation steps or package restores.
* Instead of a compatible IDE you can also build the solutions with `msbuild`, or on Mono with `xbuild`.
* The full build including unit tests, docs, NuGet and Zip packages is using [FAKE](http://fsharp.github.io/FAKE/).

### How to build with MSBuild/XBuild

    msbuild MathNet.Filtering.sln            # only build for .Net 4 (main solution)
    msbuild MathNet.Filtering.Net35Only.sln  # only build for .Net 3.5
    msbuild MathNet.Filtering.All.sln        # full build with .Net 4, 3.5 and PCL profiles
    xbuild MathNet.Filtering.sln             # build with Mono, e.g. on Linux or Mac

### How to build with FAKE

    build.cmd    # normal build (.Net 4.0), run unit tests
    ./build.sh   # normal build (.Net 4.0), run unit tests - on Linux or Mac
    ./buildn.sh  # normal build (.Net 4.0), run unit tests - bash on Windows (.Net instead of mono)
    
    build.cmd Build              # normal build (.Net 4.0)
    build.cmd Build incremental  # normal build, incremental (.Net 4.0)
    build.cmd Build all          # full build (.Net 4.0, 3.5, PCL)
    build.cmd Build net35        # compatibility build (.Net 3.5)
    
    build.cmd Test        # normal build (.Net 4.0), run unit tests
    build.cmd Test quick  # normal build (.Net 4.0), run unit tests except long running ones
    build.cmd Test all    # full build (.Net 4.0, 3.5, PCL), run all unit tests
    build.cmd Test net35  # compatibility build (.Net 3.5), run unit testss
    
    build.cmd Clean  # cleanup build artifacts
    build.cmd Docs   # generate documentation
    build.cmd Api    # generate api reference
    
    build.cmd NuGet all     # generate normal NuGet packages (.Net 4.0, 3.5, PCL)
    build.cmd NuGet signed  # generate signed/strong named NuGet packages (.Net 4.0)
    
    build.cmd All          # build, test, docs, api reference (.Net 4.0)
    build.cmd All release  # release build

FAKE itself is not included in the repository but it will download and bootstrap itself automatically when build.cmd is run the first time. Note that this step is *not* required when using Visual Studio or `msbuild` directly.

Quick Links
-----------

* [**Project Website**](http://filtering.mathdotnet.com)
* [Source Code](http://github.com/mathnet/mathnet-filtering)
* [Documentation](http://filtering.mathdotnet.com/docs/)
* [API Reference](http://filtering.mathdotnet.com/api/)
* [Work Items and Bug Tracker](http://github.com/mathnet/mathnet-filtering/issues)

Math.NET on other sites:

* [Twitter @MathDotNet](http://twitter.com/MathDotNet)
* [Google+](https://plus.google.com/112484567926928665204)
* [Ohloh](https://www.ohloh.net/p/mathnet)
* [Stack Overflow](http://stackoverflow.com/questions/tagged/mathdotnet)
