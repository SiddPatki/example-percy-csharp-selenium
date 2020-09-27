# example-percy-csharp-selenium
This example app is an HTTP server that serves a fork of the [TodoMVC](https://github.com/tastejs/todomvc)
[Vanilla-ES6](https://github.com/tastejs/todomvc/tree/master/examples/vanilla-es6)
(forked at commit
[c78ae12a1834a11da6236c64a0c0fb06b20b7c51](https://github.com/tastejs/todomvc/tree/c78ae12a1834a11da6236c64a0c0fb06b20b7c51)).

The project requires .NET Core 3.1 or higher.

The Selenium tests use ChromeDriver, which you need to install separately for your system.

On Mac OS, you can use Homebrew:
```bash
$ brew tap homebrew/cask && brew cask install chromedriver
```

On Windows, you can use Chocolatey:

```bash
$ choco install chromedriver
```

For other systems (or installation alternatives), see:
https://github.com/SeleniumHQ/selenium/wiki/ChromeDriver

## Building and running the app

To compile and build a .dll file containing our app:
```bash
$ dotnet build
```

To run the tests and create the build on Percy:
```bash
$ PERCY_TOKEN=<YOUR_PROJECT_TOKEN> percy exec -- dotnet example-percy-csharp-selenium/bin/Debug/*/example-percy-csharp-selenium.dll
```