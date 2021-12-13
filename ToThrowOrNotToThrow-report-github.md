``` ini

BenchmarkDotNet=v0.13.1, OS=Windows 10.0.19043.1348 (21H1/May2021Update)
Intel Core i7-9850H CPU 2.60GHz, 1 CPU, 12 logical and 6 physical cores
  [Host]     : .NET Framework 4.8 (4.8.4420.0), X86 LegacyJIT  [AttachedDebugger]
  DefaultJob : .NET Framework 4.8 (4.8.4420.0), X86 LegacyJIT


```
|             Method |       Mean |   Error |  StdDev |       Gen 0 |     Gen 1 | Allocated |
|------------------- |-----------:|--------:|--------:|------------:|----------:|----------:|
|   Default_AllValid |   617.9 ms | 4.62 ms | 4.32 ms | 107000.0000 | 1000.0000 |    539 MB |
|   NoThrow_AllValid |   627.0 ms | 4.35 ms | 3.86 ms | 105000.0000 | 1000.0000 |    530 MB |
| Default_AllInvalid | 1,170.0 ms | 5.50 ms | 5.15 ms |  86000.0000 |         - |    430 MB |
| NoThrow_AllInvalid |   452.7 ms | 2.98 ms | 2.79 ms |  80000.0000 |         - |    400 MB |
|  Default_HalfValid |   941.6 ms | 5.89 ms | 5.51 ms |  96000.0000 | 1000.0000 |    484 MB |
|  NoThrow_HalfValid |   543.8 ms | 3.45 ms | 3.06 ms |  93000.0000 |         - |    466 MB |
