__HPC, Distributed Computing, Cloud computing, Cluster computing, Grid computing, Parallel computing, Hardware arch (ARM, CUDA, GPU, MIPS), Kernels, Compilers (source-to-source compiler, transcompiler/ transpilers)__

+ [ARM-CUDA](#arm-cuda)
+ [COMPILERS](#compilers)
   + [Transpiler](#transpiler)
+ [Computer Performance](#computer-performance)
+ [CONCURRENCY](#concurrency)
+ [DISTRIBUTED-PARALLEL](#distributed-parallel) 
   + [Job Scheduler](#job-scheduler)
+ [GRID](#grid) 
+ [Org-JuliaGPU](#org-juliagpu)
+ [Org-JuliaParallel](#org-juliaparallel)
+ [Org-JuliaLang](#org-julialang)
+ [Publications](#publications)

----

# ARM-CUDA
+ [Build Julia on ARMv7 / Cortex A15 Samsung Chromebooks running Ubuntu Linux under Crouton](https://github.com/JuliaLang/julia/blob/master/README.arm.md).
   + Bug status of the [Julia port to ARM](https://github.com/JuliaLang/julia/issues/3134) and the [Debian build log](https://buildd.debian.org/status/fetch.php?pkg=julia&arch=armhf&ver=0.1.2%2Bdfsg-3&stamp=1368675598).
+ [Instruments.jl](https://github.com/BBN-Q/Instruments.jl) :: A package for controlling laboratory instruments through Julia over TCPIP/GPIB/USB/Serial, wrapped around the NI-VISA library (which needs to be separately installed) similar to PyVISA and has some starts towards making it easier to write custom instrument drivers. 
+ [NIDAQ.jl](https://github.com/JaneliaSciComp/NIDAQ.jl) :: This package provides an interface to NIDAQmx - National Instruments' driver for their data acquisition boards.
+ Sample notebooks for: [GPU Julia](http://nbviewer.ipython.org/7436359), and [GPU Transpose](http://nbviewer.ipython.org/7436439).

----

# COMPILERS
+ [Clang.jl](https://github.com/ihnorton/Clang.jl) :: Julia interface to libclang and C wrapper generator and its fork [CIndex.jl](https://github.com/vtjnash/CIndex.jl) to access the libclang interface of the LLVM Clang compiler.
+ [Eglib.jl](https://github.com/ihnorton/Eglib.jl) :: Clang.jl wrapping example, C code from @kindlmann.
+ [JITTools.jl](https://github.com/loladiro/JITTools.jl) :: Tools for working with in-memory object. 
+ [LLVM.jl](https://github.com/jakebolewski/LLVM.jl) :: A Julia package for LLVM.

### Transpiler
+ [Julia2C](https://github.com/IntelLabs/julia/tree/j2c) :: A source-to-source translator from Julia to C. This initial version converts basic Julia types and expressions into the corresponding C types and statements.

---- 

# Computer Performance
+ [CPUTime.jl](https://github.com/schmrlng/CPUTime.jl) :: Amodule for CPU timing. 
+ [USERTime.jl](https://github.com/christianpeel/USERTime.jl) :: A Julia package for measuring elapsed user time. 

----

# DISTRIBUTED-PARALLEL
**Cloud/ Cluster**
+ [AWS.jl](https://github.com/amitmurthy/AWS.jl) :: supports the EC2 and S3 API's, letting you start and stop EC2 instances dynamically.
+ [ChainedVectors.jl](https://github.com/tanmaykm/ChainedVectors.jl) :: Few utility types over Julia Vector type.
+ [Flume.jl](https://github.com/malmaud/Flume.jl) :: A port of the Google Flume Data-Parallel Pipeline system.
+ [FunHPC.jl](https://bitbucket.org/eschnett/funhpc.jl) :: A high-level API for distributed computing, implemented on top of MPI.
+ [GCloud.jl](https://github.com/spencerlyon2/GCloud.jl) :: Tools for working with Google Compute engine via the cloud CLI.
+ [OCAWS.jl](https://github.com/samoconnor/OCAWS.jl) :: An AWS library.
+ [ParallelGLM.jl](https://github.com/dmbates/ParallelGLM.jl) :: Parallel fitting of GLMs using SharedArrays.
+ [PTools.jl](https://github.com/amitmurthy/PTools.jl) :: A collection of utilities for parallel computing in Julia.
+ [SGEArrays.jl](https://github.com/davidavdav/SGEArrays.jl) :: SGEArray implements a simple iterator in Julia to efficiently handle Sun Grid Engine task arrays.


###### Resources
+ [Parallel Computing](http://docs.julialang.org/en/latest/manual/parallel-computing/)
+ [How to use AWS EC2 machines via addprocs for parallel computing](http://docs.julialang.org/en/latest/stdlib/base/#parallel-computing).
+ [Parallel and Distributed Computing with Julia](http://www.csd.uwo.ca/~moreno/cs2101a_moreno/Parallel_computing_with_Julia.pdf) by Marc Moreno Maza, for CS2101 at the University of Western Ontario, London, Ontario (Canada). Updated October 16, 2014.
+ Julia Ferraioli on using Julia on Google Compute Engine (GCE): 
   + Julia [installation and first steps](http://www.blog.juliaferraioli.com/2013/12/julia-on-google-compute-engine.html).
   + An example of [interfacing with the Cloud Datastore via JSON](http://www.blog.juliaferraioli.com/2014/01/julia-on-google-compute-engine-working.html)

----

# [CONCURRENCY](https://en.wikipedia.org/wiki/Concurrency_%28computer_science%29)

### [Job Scheduler](https://en.wikipedia.org/wiki/Job_scheduler)
+ [ClusterManagers.jl](https://github.com/JuliaLang/ClusterManagers.jl) :: Support for different clustering technologies.
+ [LCJC.jl](https://github.com/amitmurthy/LCJC.jl) :: Loosely Coupled Julia Clusters.
+ [LoraMPI.jl](https://github.com/scidom/LoraMPI.jl) :: MPI Job Manager for Lora Parralel-Centric Runners.
+ [MatlabCluster.jl](https://github.com/simonster/MatlabCluster.jl) :: Julia cluster manager for Matlab Job Scheduler.
+ [Reactive.jl](https://github.com/JuliaLang/Reactive.jl) :: A package for reactive programming in Julia.
+ [SimJulia.jl](https://github.com/BenLauwens/SimJulia.jl) :: A combined continuous time / discrete event process oriented simulation framework written in Julia inspired by the Simula library DISCO and the Python library SimPy.

----

# GRID
+ [IBFS.jl](https://github.com/eurika-kaiser/IBFS.jl) :: Grid simulation solver.

----

# Org-[JuliaGPU](https://github.com/JuliaGPU)
Mailing list : https://groups.google.com/forum/#!forum/julia-gpu
+ [AbstractGPUArray.jl](https://github.com/JuliaGPU/AbstractGPUArray.jl) :: An abstract interface for a GPU array, must be implemented by a back-end like OpenCL or OpenGL.
+ [CLBLAS.jl](https://github.com/JuliaGPU/CLBLAS.jl) :: CLBLAS integration for Julia.
+ [CUBLAS.jl](https://github.com/JuliaGPU/CUBLAS.jl) :: Julia interface to CUBLAS.
+ [CUDA.jl](https://github.com/JuliaGPU/CUDA.jl) :: This package wraps key functions in CUDA Driver API.
+ [CUDArt.jl](https://github.com/JuliaGPU/CUDArt.jl) :: Wrapper for CUDA runtime API.
+ [CUDNN.jl](https://github.com/JuliaGPU/CUDNN.jl) :: Julia wrapper for the NVIDIA cuDNN GPU deep learning library.
+ [julia-CuMatrix](https://github.com/stefan-k/julia-CuMatrix) :: CUDA Matrix library.
+ [julia-kernels](https://github.com/toivoh/julia-kernels) :: A small suite of tools aimed at being able to write kernels in Julia, which could be executed on the CPU, or as GPU kernels. 
+ [OpenCL.jl](https://github.com/JuliaGPU/OpenCL.jl) :: OpenCL 1.2 Julia bindings - a cross platform parallel computation API for programming parallel devices, with implementations from AMD, Nvidia, Intel, and others, similar in scope to PyOpenCL. 
+ [UberSignals.jl](https://github.com/SimonDanisch/UberSignals.jl) :: Concept for a fast event signal system, using JIT and GPU acceleration, loosely inspired by Reactive.jl.

###### Resources
+ Blog post on [Compiling Julia for NVIDIA GPUs](http://blog.maleadt.net/2015/01/15/julia-cuda/)

----

# Org-[JuliaLang](https://github.com/JuliaLang)
+ [Yeppp.jl](https://github.com/JuliaLang/Yeppp.jl) :: A low level, high performance library for vectorized operations, elementwise operation on arrays, supports the x86(-64), ARM and MIPS architectures, and takes advantage of a lot of SIMD extensions (from SSE to AVX2 on x86, NEON on ARM). The New BSD(3-clause BSD)-licensed [source code is hosted on Bitbucket](https://bitbucket.org/MDukhan/yeppp).

----

# Org-[JuliaParallel](https://JuliaParallel.github.io)
+ [Blocks.jl](https://github.com/JuliaParallel/Blocks.jl) :: A framework to represent chunks of entities and parallel methods on them.
+ [ClusterManagers.jl](https://github.com/JuliaParallel/ClusterManagers.jl) :: Support for different clustering technologies.
+ [DistributedArrays.jl](https://github.com/JuliaParallel/DistributedArrays.jl) :: Distributed Arrays in Julia.
+ [Elly.jl](https://github.com/JuliaParallel/Elly.jl) :: Hadoop HDFS and Yarn client.
+ [HDFS.jl](https://github.com/JuliaParallel/HDFS.jl) :: An interface wrapper over the Hadoop HDFS library that wraps the HDFS C library libhdfs and provides APIs similar to Julia Filesystem APIs which can be used for direct access to HDFS files.
+ [hwloc.jl](https://github.com/JuliaParallel/hwloc.jl) :: The Portable Hardware Locality (hwloc) package wraps the hwloc library to provide a portable abstraction (across OS, versions, architectures, ...) of the hierarchical topology of modern architectures, including NUMA memory nodes, sockets, shared caches, cores and simultaneous multithreading. 
+ [MessageUtils.jl](https://github.com/JuliaParallel/MessageUtils.jl) :: A collection of utilities for messaging.
+ [MPI.jl](https://github.com/JuliaParallel/MPI.jl) :: A basic Julia wrapper for the portable message passing system Message Passing Interface (MPI).
   + [JuliaMPIMonteCarlo](https://github.com/mcreel/JuliaMPIMonteCarlo) :: Illustrative examples using Julia and MPI to do Markov Chain Monte Carlo (MCMC) methods.
+ [ScaLAPACK.jl](https://github.com/JuliaParallel/ScaLAPACK.jl) :: Scalable Linear Algebra PACKage.

###### Resources
+ [JuliaCon2015_Workshop](https://github.com/JuliaParallel/JuliaCon2015_Workshop) :: Notebooks from the JuliaCon2015 Workshop.

----

# Publications
+ [Parallel Prefix Polymorphism Permits Parallelization, Presentation & Proof](http://jiahao.github.io/parallel-prefix/) :: A short [paper](https://github.com/jiahao/parallel-prefix) about parallel prefix.

