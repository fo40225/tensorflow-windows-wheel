# tensorflow-windows-wheel

This repo contains all you need that work with tensorflow on windows.

- Python 3.8 support

- 64 bit Windows support

- Legacy & low-end CPU (without AVX) support
    - If your CPU didn't support AVX instructions, you will get `ImportError: DLL load failed: A dynamic link library (DLL) initialization routine failed.` (Win 10) or `ImportError: DLL load failed with error code -1073741795` (Win 7) when using tensorflow official release 1.6.0 and up (`pip install tensorflow`)
    - You can use `pip install <filename.whl>` which file download from sse2 folder instead of using official AVX binary.

| Path | Compiler | CUDA/cuDNN | SIMD | Notes |
|-|-|-|-|-|
| 1.15.4+nv20.12\py38\CPU+GPU\cuda111cudnn8sse2 | VS2019 16.8 | 11.1.1_456.81/8.0.5.39 | x86_64 | Python 3.8/Compute 3.5 |
| 1.15.4+nv20.12\py38\CPU+GPU\cuda111cudnn8avx2 | VS2019 16.8 | 11.1.1_456.81/8.0.5.39 | AVX2 | Python 3.8/Compute 3.5,5.0,5.2,6.1,7.0,7.5,8.6 |
| 2.4.0\py38\CPU+GPU\cuda111cudnn8sse2 | VS2019 16.8 | 11.1.1_456.81/8.0.5.39 | x86_64 | Python 3.8/compute_35 |
| 2.4.0\py38\CPU+GPU\cuda111cudnn8avx2 | VS2019 16.8 | 11.1.1_456.81/8.0.5.39 | AVX2 | Python 3.8/compute_35,sm_50,sm_52,sm_61,sm_70,sm_75,compute_86 |
| 2.3.0\py38\CPU+GPU\cuda110cudnn8sse2 | VS2019 16.6 | 11.0.2_451.48/8.0.2.39 | x86_64 | Python 3.8/compute_35 |
| 2.3.0\py38\CPU+GPU\cuda110cudnn8avx2 | VS2019 16.6 | 11.0.2_451.48/8.0.2.39 | AVX2 | Python 3.8/compute_35,sm_50,sm_52,sm_61,sm_70,compute_75 |
| 2.2.0\py37\CPU+GPU\cuda102cudnn76sse2 | VS2019 16.5 | 10.2.89_441.22/7.6.5.32 | x86_64 | Python 3.7/Compute 3.0 |
| 2.2.0\py37\CPU+GPU\cuda102cudnn76avx2 | VS2019 16.5 | 10.2.89_441.22/7.6.5.32 | AVX2 | Python 3.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 2.1.0\py37\CPU+GPU\cuda102cudnn76sse2 | VS2019 16.4 | 10.2.89_441.22/7.6.5.32 | x86_64 | Python 3.7/Compute 3.0 |
| 2.1.0\py37\CPU+GPU\cuda102cudnn76avx2 | VS2019 16.4 | 10.2.89_441.22/7.6.5.32 | AVX2 | Python 3.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 2.0.0\py37\CPU\sse2 | VS2019 16.3 | No | x86_64 | Python 3.7 |
| 2.0.0\py37\CPU\avx2 | VS2019 16.3 | No | AVX2 | Python 3.7 |
| 2.0.0\py37\GPU\cuda101cudnn76sse2 | VS2019 16.3 | 10.1.243_426.00/7.6.4.38 | x86_64 | Python 3.7/Compute 3.0 |
| 2.0.0\py37\GPU\cuda101cudnn76avx2 | VS2019 16.3 | 10.1.243_426.00/7.6.4.38 | AVX2 | Python 3.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 1.15.0\py37\CPU+GPU\cuda101cudnn76sse2 | VS2019 16.3 | 10.1.243_426.00/7.6.4.38 | x86_64 | Python 3.7/Compute 3.0 |
| 1.15.0\py37\CPU+GPU\cuda101cudnn76avx2 | VS2019 16.3 | 10.1.243_426.00/7.6.4.38 | AVX2 | Python 3.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 1.14.0\py37\CPU\sse2 | VS2019 16.1 | No | x86_64 | Python 3.7 |
| 1.14.0\py37\CPU\avx2 | VS2019 16.1 | No | AVX2 | Python 3.7 |
| 1.14.0\py37\GPU\cuda101cudnn76sse2 | VS2019 16.1 | 10.1.168_425.25/7.6.0.64 | x86_64 | Python 3.7/Compute 3.0 |
| 1.14.0\py37\GPU\cuda101cudnn76avx2 | VS2019 16.1 | 10.1.168_425.25/7.6.0.64 | AVX2 | Python 3.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 1.13.1\py37\CPU\sse2 | VS2017 15.9 | No | x86_64 | Python 3.7 |
| 1.13.1\py37\CPU\avx2 | VS2017 15.9 | No | AVX2 | Python 3.7 |
| 1.13.1\py37\GPU\cuda101cudnn75sse2 | VS2017 15.9 | 10.1.105_418.96/7.5.0.56 | x86_64 | Python 3.7/Compute 3.0 |
| 1.13.1\py37\GPU\cuda101cudnn75avx2 | VS2017 15.9 | 10.1.105_418.96/7.5.0.56 | AVX2 | Python 3.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 1.12.0\py36\CPU\sse2 | VS2017 15.8 | No | x86_64 | Python 3.6 |
| 1.12.0\py36\CPU\avx2 | VS2017 15.8 | No | AVX2 | Python 3.6 |
| 1.12.0\py36\GPU\cuda100cudnn73sse2 | VS2017 15.8 | 10.0.130_411.31/7.3.1.20 | x86_64 | Python 3.6/Compute 3.0 |
| 1.12.0\py36\GPU\cuda100cudnn73avx2 | VS2017 15.8 | 10.0.130_411.31/7.3.1.20 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 1.12.0\py37\CPU\sse2 | VS2017 15.8 | No | x86_64 | Python 3.7 |
| 1.12.0\py37\CPU\avx2 | VS2017 15.8 | No | AVX2 | Python 3.7 |
| 1.12.0\py37\GPU\cuda100cudnn73sse2 | VS2017 15.8 | 10.0.130_411.31/7.3.1.20 | x86_64 | Python 3.7/Compute 3.0 |
| 1.12.0\py37\GPU\cuda100cudnn73avx2 | VS2017 15.8 | 10.0.130_411.31/7.3.1.20 | AVX2 | Python 3.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 1.11.0\py36\CPU\sse2 | VS2017 15.8 | No | x86_64 | Python 3.6 |
| 1.11.0\py36\CPU\avx2 | VS2017 15.8 | No | AVX2 | Python 3.6 |
| 1.11.0\py36\GPU\cuda100cudnn73sse2 | VS2017 15.8 | 10.0.130_411.31/7.3.0.29 | x86_64 | Python 3.6/Compute 3.0 |
| 1.11.0\py36\GPU\cuda100cudnn73avx2 | VS2017 15.8 | 10.0.130_411.31/7.3.0.29 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 1.11.0\py37\CPU\sse2 | VS2017 15.8 | No | x86_64 | Python 3.7 |
| 1.11.0\py37\CPU\avx2 | VS2017 15.8 | No | AVX2 | Python 3.7 |
| 1.11.0\py37\GPU\cuda100cudnn73sse2 | VS2017 15.8 | 10.0.130_411.31/7.3.0.29 | x86_64 | Python 3.7/Compute 3.0 |
| 1.11.0\py37\GPU\cuda100cudnn73avx2 | VS2017 15.8 | 10.0.130_411.31/7.3.0.29 | AVX2 | Python 3.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 1.10.0\py36\CPU\sse2 | VS2017 15.8 | No | x86_64 | Python 3.6 |
| 1.10.0\py36\CPU\avx2 | VS2017 15.8 | No | AVX2 | Python 3.6 |
| 1.10.0\py36\GPU\cuda92cudnn72sse2 | VS2017 15.8 | 9.2.148.1/7.2.1.38 | x86_64 | Python 3.6/Compute 3.0 |
| 1.10.0\py36\GPU\cuda92cudnn72avx2 | VS2017 15.8 | 9.2.148.1/7.2.1.38 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.10.0\py27\CPU\sse2 | VS2017 15.8 | No | x86_64 | Python 2.7 |
| 1.10.0\py27\CPU\avx2 | VS2017 15.8 | No | AVX2 | Python 2.7 |
| 1.10.0\py27\GPU\cuda92cudnn72sse2 | VS2017 15.8 | 9.2.148.1/7.2.1.38 | x86_64 | Python 2.7/Compute 3.0 |
| 1.10.0\py27\GPU\cuda92cudnn72avx2 | VS2017 15.8 | 9.2.148.1/7.2.1.38 | AVX2 | Python 2.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.9.0\py36\CPU\sse2 | VS2017 15.7 | No | x86_64 | Python 3.6 |
| 1.9.0\py36\CPU\avx2 | VS2017 15.7 | No | AVX2 | Python 3.6 |
| 1.9.0\py36\GPU\cuda92cudnn71sse2 | VS2017 15.7 | 9.2.148/7.1.4 | x86_64 | Python 3.6/Compute 3.0 |
| 1.9.0\py36\GPU\cuda92cudnn71avx2 | VS2017 15.7 | 9.2.148/7.1.4 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.9.0\py27\CPU\sse2 | VS2017 15.7 | No | x86_64 | Python 2.7 |
| 1.9.0\py27\CPU\avx2 | VS2017 15.7 | No | AVX2 | Python 2.7 |
| 1.9.0\py27\GPU\cuda92cudnn71sse2 | VS2017 15.7 | 9.2.148/7.1.4 | x86_64 | Python 2.7/Compute 3.0 |
| 1.9.0\py27\GPU\cuda92cudnn71avx2 | VS2017 15.7 | 9.2.148/7.1.4 | AVX2 | Python 2.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.8.0\py36\CPU\sse2 | VS2017 15.4 | No | x86_64 | Python 3.6 |
| 1.8.0\py36\CPU\avx2 | VS2017 15.4 | No | AVX2 | Python 3.6 |
| 1.8.0\py36\GPU\cuda91cudnn71sse2 | VS2017 15.4 | 9.1.85.3/7.1.3 | x86_64 | Python 3.6/Compute 3.0 |
| 1.8.0\py36\GPU\cuda91cudnn71avx2 | VS2017 15.4 | 9.1.85.3/7.1.3 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.8.0\py27\CPU\sse2 | VS2017 15.4 | No | x86_64 | Python 2.7 |
| 1.8.0\py27\CPU\avx2 | VS2017 15.4 | No | AVX2 | Python 2.7 |
| 1.8.0\py27\GPU\cuda91cudnn71sse2 | VS2017 15.4 | 9.1.85.3/7.1.3 | x86_64 | Python 2.7/Compute 3.0 |
| 1.8.0\py27\GPU\cuda91cudnn71avx2 | VS2017 15.4 | 9.1.85.3/7.1.3 | AVX2 | Python 2.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.7.0\py36\CPU\sse2 | VS2017 15.4 | No | x86_64 | Python 3.6 |
| 1.7.0\py36\CPU\avx2 | VS2017 15.4 | No | AVX2 | Python 3.6 |
| 1.7.0\py36\GPU\cuda91cudnn71sse2 | VS2017 15.4 | 9.1.85.3/7.1.2 | x86_64 | Python 3.6/Compute 3.0 |
| 1.7.0\py36\GPU\cuda91cudnn71avx2 | VS2017 15.4 | 9.1.85.3/7.1.2 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.7.0\py27\CPU\sse2 | VS2017 15.4 | No | x86_64 | Python 2.7 |
| 1.7.0\py27\CPU\avx2 | VS2017 15.4 | No | AVX2 | Python 2.7 |
| 1.7.0\py27\GPU\cuda91cudnn71sse2 | VS2017 15.4 | 9.1.85.3/7.1.2 | x86_64 | Python 2.7/Compute 3.0 |
| 1.7.0\py27\GPU\cuda91cudnn71avx2 | VS2017 15.4 | 9.1.85.3/7.1.2 | AVX2 | Python 2.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.6.0\py36\CPU\sse2 | VS2017 15.4 | No | x86_64 | Python 3.6 |
| 1.6.0\py36\CPU\avx2 | VS2017 15.4 | No | AVX2 | Python 3.6 |
| 1.6.0\py36\GPU\cuda91cudnn71sse2 | VS2017 15.4 | 9.1.85.3/7.1.1 | x86_64 | Python 3.6/Compute 3.0 |
| 1.6.0\py36\GPU\cuda91cudnn71avx2 | VS2017 15.4 | 9.1.85.3/7.1.1 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.6.0\py27\CPU\sse2 | VS2017 15.4 | No | x86_64 | Python 2.7 |
| 1.6.0\py27\CPU\avx2 | VS2017 15.4 | No | AVX2 | Python 2.7 |
| 1.6.0\py27\GPU\cuda91cudnn71sse2 | VS2017 15.4 | 9.1.85.2/7.1.1 | x86_64 | Python 2.7/Compute 3.0 |
| 1.6.0\py27\GPU\cuda91cudnn71avx2 | VS2017 15.4 | 9.1.85.2/7.1.1 | AVX2 | Python 2.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.5.0\py36\CPU\avx | VS2017 15.4 | No | AVX | Python 3.6 |
| 1.5.0\py36\CPU\avx2 | VS2017 15.4 | No | AVX2 | Python 3.6 |
| 1.5.0\py36\GPU\cuda91cudnn7avx2 | VS2017 15.4 | 9.1.85/7.0.5 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.5.0\py27\CPU\sse2 | VS2017 15.4 | No | x86_64 | Python 2.7 |
| 1.5.0\py27\CPU\avx | VS2017 15.4 | No | AVX | Python 2.7 |
| 1.5.0\py27\CPU\avx2 | VS2017 15.4 | No | AVX2 | Python 2.7 |
| 1.5.0\py27\GPU\cuda91cudnn7sse2 | VS2017 15.4 | 9.1.85/7.0.5 | x86_64 | Python 2.7/Compute 3.0 |
| 1.5.0\py27\GPU\cuda91cudnn7avx2 | VS2017 15.4 | 9.1.85/7.0.5 | AVX2 | Python 2.7/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.4.0\py36\CPU\avx | VS2017 15.4 | No | AVX | Python 3.6 |
| 1.4.0\py36\CPU\avx2 | VS2017 15.4 | No | AVX2 | Python 3.6 |
| 1.4.0\py36\GPU\cuda91cudnn7avx2 | VS2017 15.4 | 9.1.85/7.0.5 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0 |
| 1.3.0\py36\CPU\avx | VS2015 Update 3 | No | AVX | Python 3.6 |
| 1.3.0\py36\CPU\avx2 | VS2015 Update 3 | No | AVX2 | Python 3.6 |
| 1.3.0\py36\GPU\cuda8cudnn6avx2 | VS2015 Update 3 | 8.0.61.2/6.0.21 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1 |
| 1.2.1\py36\CPU\avx | VS2015 Update 3 | No | AVX | Python 3.6 |
| 1.2.1\py36\CPU\avx2 | VS2015 Update 3 | No | AVX2 | Python 3.6 |
| 1.2.1\py36\GPU\cuda8cudnn6avx2 | VS2015 Update 3 | 8.0.61.2/6.0.21 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1 |
| 1.1.0\py36\CPU\avx | VS2015 Update 3 | No | AVX | Python 3.6 |
| 1.1.0\py36\CPU\avx2 | VS2015 Update 3 | No | AVX2 | Python 3.6 |
| 1.1.0\py36\GPU\cuda8cudnn6avx2 | VS2015 Update 3 | 8.0.61.2/6.0.21 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1 |
| 1.0.0\py36\CPU\sse2 | VS2015 Update 3 | No | x86_64 | Python 3.6 |
| 1.0.0\py36\CPU\avx | VS2015 Update 3 | No | AVX | Python 3.6 |
| 1.0.0\py36\CPU\avx2 | VS2015 Update 3 | No | AVX2 | Python 3.6 |
| 1.0.0\py36\GPU\cuda8cudnn51sse2 | VS2015 Update 3 | 8.0.61.2/5.1.10 | x86_64 | Python 3.6/Compute 3.0 |
| 1.0.0\py36\GPU\cuda8cudnn51avx2 | VS2015 Update 3 | 8.0.61.2/5.1.10 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1 |
| 0.12.0\py35\CPU\avx | VS2015 Update 3 | No | AVX | Python 3.5 |
| 0.12.0\py35\CPU\avx2 | VS2015 Update 3 | No | AVX2 | Python 3.5 |
| 0.12.0\py35\GPU\cuda8cudnn51avx2 | VS2015 Update 3 | 8.0.61.2/5.1.10 | AVX2 | Python 3.5/Compute 3.0,3.5,5.0,5.2,6.1 |
