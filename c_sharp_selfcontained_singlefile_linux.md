[dotnet cli](https://learn.microsoft.com/en-us/dotnet/core/tools/)

Create app:
```
dotnet new console --framework net7.0
```

Run app:
```
dotnet run
```

Create linux executable:
```
dotnet publish -r linux-x64 --self-contained true --configuration Release -p:PublishSingleFile=true
```
