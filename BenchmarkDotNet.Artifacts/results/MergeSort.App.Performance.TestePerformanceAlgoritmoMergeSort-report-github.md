``` ini

BenchmarkDotNet=v0.13.5, OS=Windows 10 (10.0.19045.3570/22H2/2022Update)
Intel Core i7-10510U CPU 1.80GHz, 1 CPU, 8 logical and 4 physical cores
.NET SDK=7.0.400
  [Host]     : .NET 7.0.10 (7.0.1023.36312), X64 RyuJIT AVX2
  DefaultJob : .NET 7.0.10 (7.0.1023.36312), X64 RyuJIT AVX2


```
|                     Method |         Array |                Mean |             Error |            StdDev | Rank |      Gen0 |     Gen1 |     Gen2 |  Allocated |
|--------------------------- |-------------- |--------------------:|------------------:|------------------:|-----:|----------:|---------:|---------:|-----------:|
|  **MedirPerformanceMergeSort** | **Int32[100000]** |     **8,232,976.55 ns** |    **162,350.281 ns** |    **316,651.755 ns** |    **8** | **2671.8750** | **234.3750** | **234.3750** | **12031272 B** |
| MedirPerformanceBubbleSort | Int32[100000] | 5,411,927,633.33 ns | 95,923,621.476 ns | 74,890,854.061 ns |   10 |         - |        - |        - |      600 B |
|  **MedirPerformanceMergeSort** |  **Int32[10000]** |       **720,451.90 ns** |     **22,989.513 ns** |     **67,061.487 ns** |    **7** |  **255.8594** |        **-** |        **-** |  **1072017 B** |
| MedirPerformanceBubbleSort |  Int32[10000] |    45,510,431.55 ns |    907,360.686 ns |    931,792.620 ns |    9 |         - |        - |        - |       55 B |
|  **MedirPerformanceMergeSort** |   **Int32[1000]** |        **44,197.05 ns** |        **856.210 ns** |        **800.899 ns** |    **5** |   **22.0337** |        **-** |        **-** |    **92304 B** |
| MedirPerformanceBubbleSort |   Int32[1000] |       465,293.47 ns |      8,132.131 ns |     10,856.161 ns |    6 |         - |        - |        - |          - |
|  **MedirPerformanceMergeSort** |    **Int32[100]** |         **3,510.93 ns** |         **44.416 ns** |         **37.090 ns** |    **3** |    **1.9112** |        **-** |        **-** |     **8000 B** |
| MedirPerformanceBubbleSort |    Int32[100] |         4,841.24 ns |         71.858 ns |         63.700 ns |    4 |         - |        - |        - |          - |
|  **MedirPerformanceMergeSort** |     **Int32[10]** |           **250.56 ns** |          **4.695 ns** |         **10.107 ns** |    **2** |    **0.1488** |        **-** |        **-** |      **624 B** |
| MedirPerformanceBubbleSort |     Int32[10] |            47.86 ns |          0.535 ns |          0.418 ns |    1 |         - |        - |        - |          - |
