# Unit Testing with C# and nunit framework

## What?

Sample repo for testing code coverage using nunit and opencover. 

Source code based in [the dotnet samples repo](https://github.com/dotnet/samples/tree/main/core/getting-started/unit-testing-using-nunit)

A nice how-to can be found in the [learn Microsoft web site](https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-csharp-with-nunit)

## How?

```
$ dotnet sonarscanner begin /k:"unit-testing-using-nunit" /d:sonar.token="xxxx" /d:sonar.cs.opencover.reportsPaths="**/**/coverage.opencover.xml" /d:sonar.host.url="https://lurodrig-sonarqube.ngrok.io" /d:sonar.scanner.scanAll="false" /d:sonar.verbose="true"

$ dotnet build --no-incremental

$ dotnet test --collect:"XPlat Code Coverage" -- DataCollectionRunSettings.DataCollectors.DataCollector.Configuration.Format=opencover

$ dotnet sonarscanner end /d:sonar.token="xxxxx"
```
