# BLINDSPOT 

artifact implementing:

1. Static analysis + constraint extraction 
2. Trace analysis 
3. Incident template generation 
4. vPLC-style deterministic execution
5. Recovery classification 

## Build
```bash
dotnet restore BLINDSPOT.sln
dotnet build BLINDSPOT.sln -c Release
dotnet test BLINDSPOT.sln -c Release
```

## Run
```bash
dotnet run --project src/BLINDSPOT.Cli -- --out artifacts/run1
```


## .NET Dependencies

### Required SDK
- **.NET SDK 8.0** (or newer 8.x)

Check installed version:
```bash
dotnet --version
