# TOUCH
TOUCH: In-Memory Spatial Join by Hierarchical Data-Oriented Partitioning
##Abstract
Efficient spatial joins are pivotal for many applications and particularly important for geographical information systems or for the simulation sciences where scientists work with spatial models. Past research has primarily focused on disk-based spatial joins; efficient in-memory approaches, however, are important for two reasons: a) main memory has grown so large that many datasets fit in it and b) the in-memory join is a very time-consuming part of all disk-based spatial joins.

In this paper we develop TOUCH, a novel in-memory spatial join algorithm that uses hierarchical data-oriented space partitioning, thereby keeping both its memory footprint and the number of comparisons low. Our results show that TOUCH outperforms known in-memory spatial-join algorithms as well as in-memory implementations of disk-based join approaches. In particular, it has a one order of magnitude advantage over the memory-demanding state of the art in terms of number of comparisons (i.e., pairwise object comparisons), as well as execution time, while it is two orders of magnitude faster when compared to approaches with a similar memory footprint. Furthermore, TOUCH is more scalable than competing approaches as data density grows.

##Running Instructions
How to compile/run:

###Prerun:
The following libraries to be installed:
1. Boost (http://www.boost.org/)
2. CUDA (https://developer.nvidia.com/cuda-downloads)
3. CMake (http://www.cmake.org/download/)

###Run:
Make the project via cmake and run as explained below:

1. In folder "/build" execute "cmake ../cmake"

2. In folder "/build" execute "make"

3. In folder "/run" execute "./SpatialJoin -a 5 -J 2 -e $EPSILON$ -i $datasetA$ $datasetB$".
For example: "/SpatialJoin -a 5 -J 2 -e 10 -i ../data/RandomData-10K.bin ../data/RandomData-Normal-500-250-10K.bin"

###Postrun:
The result and reports are stored in "/run/SJ.csv" in csv format.

## Please cite the paper:
[Sadegh Nobari](http://bit.ly/NOB-GS), Farhan Tauheed, Thomas Heinis, Panagiotis Karras, Stéphane Bressan, Anastasia Ailamaki,
["TOUCH: in-memory spatial join by hierarchical data-oriented partitioning"](http://bit.ly/TOUCH-nobari),
Proceedings of the ACM SIGMOD International Conference on Management of Data, SIGMOD 2013, New York, NY, USA, June 22-27, 2013: 701-712

### BibTeX record

 @inproceedings{Nobari:2013,
  author    = {Sadegh Nobari and
               Farhan Tauheed and
               Thomas Heinis and
               Panagiotis Karras and
               St{\'{e}}phane Bressan and
               Anastasia Ailamaki},
  title     = {{TOUCH:} in-memory spatial join by hierarchical data-oriented partitioning},
  booktitle = {Proceedings of the {ACM} {SIGMOD} International Conference on Management
               of Data, {SIGMOD} 2013, New York, NY, USA, June 22-27, 2013},
  pages     = {701--712},
  year      = {2013},
  url       = {http://doi.acm.org/10.1145/2463676.2463700},
  doi       = {10.1145/2463676.2463700}
}
 
## Furthur reading
[Full paper](http://bit.ly/TOUCH-nobari)

## Email
s @ s q n c o . c o m 
