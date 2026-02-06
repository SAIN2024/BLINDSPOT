# BLINDSPOT — End-to-End C#/.NET 8 Reference Implementation



1) Constraint extraction (PLC ST/SCL + operator rules JSON + ESD ST)  
2) Multi-layer constraint model (MCM) graph construction  
3) Trace analysis: slack & coupling statistics  
4) Template generation using a strict JSON schema (mock LLM for reproducibility)  
5) Template validation / instantiation  
6) vPLC execution adapter (mock surrogate simulator)  
7) Recovery outcome classification (recoverable / infeasible / unsafe)  
8) Reporting: JSON + CSV + MCM Graphviz DOT



## Build
```bash
dotnet build BLINDSPOT.sln
```

## Run pipeline
```bash
dotnet run --project src/Blindspot.Cli -- --sampleRoot samples/water --useMockLlm true --outDir out --log info
```

Outputs:
- `out/blindspot_report.json`
- `out/blindspot_report.csv`
- `out/mcm.dot` (render with Graphviz: `dot -Tpng mcm.dot -o mcm.png`)

## Run self-tests
```bash
dotnet run --project src/Blindspot.SelfTest
```
