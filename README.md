# tensorflow-windows-wheel

This repo contains all you need that work with tensorflow on windows.

- Python 2.7 and 3.6 support

- 64 bit and 32 bit Windows support

- Legacy & low-end CPU (without AVX) support
    - If your CPU didn't support AVX instructions, you will get `ImportError: DLL load failed: A dynamic link library (DLL) initialization routine failed.` (Win 10) or `ImportError: DLL load failed with error code -1073741795` (Win 7) when using tensorflow official release 1.6.0 and up (`pip install tensorflow`)
    - You can use `pip install [filename].whl` which file download from sse2 folder instead of using official AVX binary.

- Legacy GPU (compute capability 3.0 up) support
    - Because this repo's binary only contain PTX code, it need to do a Just-In-Time compile to SASS to target your graphic card by your driver. It will take time for compiling when execute tensorflow first time.

- Tensorflow C++ library prebuilt binary for Windows
    - For ANSI C user, you can download official Tensorflow C API binary https://storage.googleapis.com/tensorflow/libtensorflow/libtensorflow-cpu-windows-x86_64-1.11.0.zip

| Path | Compiler | CUDA/cuDNN | SIMD | Notes |
|-|-|-|-|-|
| 1.12.0\py36\CPU\sse2 | VS2017 15.8 | No | x86_64 | Python 3.6 |
| 1.12.0\py36\CPU\avx2 | VS2017 15.8 | No | AVX2 | Python 3.6 |
| 1.12.0\py36\GPU\cuda100cudnn73sse2 | VS2017 15.8 | 10.0.130_411.31/7.3.1.20 | x86_64 | Python 3.6/Compute 3.0 |
| 1.12.0\py36\GPU\cuda100cudnn73avx2 | VS2017 15.8 | 10.0.130_411.31/7.3.1.20 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
| 1.11.0\py36\CPU\sse2 | VS2017 15.8 | No | x86_64 | Python 3.6 |
| 1.11.0\py36\CPU\avx2 | VS2017 15.8 | No | AVX2 | Python 3.6 |
| 1.11.0\py36\GPU\cuda100cudnn73sse2 | VS2017 15.8 | 10.0.130_411.31/7.3.0.29 | x86_64 | Python 3.6/Compute 3.0 |
| 1.11.0\py36\GPU\cuda100cudnn73avx2 | VS2017 15.8 | 10.0.130_411.31/7.3.0.29 | AVX2 | Python 3.6/Compute 3.0,3.5,5.0,5.2,6.1,7.0,7.5 |
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
