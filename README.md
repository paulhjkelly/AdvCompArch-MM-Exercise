# AdvCompArch-MM-Exercise

A simple exercise to explore understanding of cache performance.  Four versions of a simple matrix-matrix multiply, MM1, MM2, MM3 and MM4.  Your job is to compile and run them, and observe their performance.  And then explain what is going on.

To run them:
  make clean
  make x86
  ./MM1.x86
  ./MM2.x86
  ./MM3.x86
  ./MM4.x86

For your amusement, I also provide MM5-blas, which uses the OpenBLAS library to achieve somewhat higher performance.  
The OpenBLAS library automatically uses multiple cores.  To limit it to a single core, use:
  make -f Makefile-blas clean
  make -f Makefile-blas
  setenv OPENBLAS_NUM_THREADS 1
  ./MM5-blas.x86
Please never, ever implement a matrix multiply yourself again - use the libraries.

(a small caveat: MM5 doesn't run fast under Ubuntu (WSL) on Windows - I think because it doesn't detect the CPU variant properly).

Paul H J Kelly
Imperial College London
