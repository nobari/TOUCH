# TOUCH
TOUCH: In-Memory Spatial Join by Hierarchical Data-Oriented Partitioning

Efficient spatial joins are pivotal for many applications and particularly important for geographical information systems or for the simulation sciences where scientists work with spatial models. Past research has primarily focused on disk-based spatial joins; efficient in-memory approaches, however, are important for two reasons: a) main memory has grown so large that many datasets fit in it and b) the in-memory join is a very time-consuming part of all disk-based spatial joins.

In this paper we develop TOUCH, a novel in-memory spatial join algorithm that uses hierarchical data-oriented space partitioning, thereby keeping both its memory footprint and the number of comparisons low. Our results show that TOUCH outperforms known in-memory spatial-join algorithms as well as in-memory implementations of disk-based join approaches. In particular, it has a one order of magnitude advantage over the memory-demanding state of the art in terms of number of comparisons (i.e., pairwise object comparisons), as well as execution time, while it is two orders of magnitude faster when compared to approaches with a similar memory footprint. Furthermore, TOUCH is more scalable than competing approaches as data density grows.

Full description: http://bit.ly/TOUCH-nobari

How to compile/run:

-Prerun: The following libraries to be installed:
-Boost (http://www.boost.org/)
-CUDA (https://developer.nvidia.com/cuda-downloads)
-CMake (http://www.cmake.org/download/)

-Run: make the project via cmake and run as explained below:
-In folder "/build" execute "cmake ../cmake"
-In folder "/build" execute "make"
-In folder "/run" execute "./SpatialJoin -a 5 -J 2 -e $EPSILON$ -i $datasetA$ $datasetB$" for example:
"/SpatialJoin -a 5 -J 2 -e 10 -i ../data/RandomData-10K.bin ../data/RandomData-Normal-500-250-10K.bin"

-Postrun: The result and reports are stored in "/run/SJ.csv" in csv format.
