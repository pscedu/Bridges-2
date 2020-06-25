# Bridges-2
This repo contains software developed to support the Bridges-2 platform at the [Pittsburgh Supercomputing Center](https://psc.edu) ([PSC](https://psc.edu)).
Bridges-2 converges high-performance computing (HPC), artificial intelligence (AI), and Big Data, expanding and extending concepts proven in [Bridges](https://psc.edu/resources/computing/bridges) and [Bridges-AI](https://psc.edu/bridges-ai-early-user-guide) to provide transformative capability for rapidly-evolving, computationally-intensive and data-intensive research, creating opportunities for collaboration and convergence research.
It emphasizes ease of access for nontraditional uses of HPC and researcher productivity by providing a extremely flexible user and software environment and interactivity, a variety of compute nodes that are optimized for different kinds of jobs and different aspects of workflows, and high-performance, unified access to all data through a parallel filesystem that's equally accessible from all compute nodes.
The Bridges-2 architecture is extensible for interoperation with complementary data-intensive projects, campus resources, and clouds.

Bridges-2 is led by [Nick Nystrom](mailto:nystrom@psc.edu) (PI/PD), Paola Buitrago (Co-PI and Director of AI & Data Science), Sergiu Sanielevici (Co-PI and Director of User Support), and Robin Scibek (Co-PI and Director of Broader Impacts). Bridges-2 is supported by [National Science Foundation award number 1928147](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1928147).

## The Bridges-2 Platform

PSC’s Bridges-2 platform will address the needs of rapidly evolving research by combining high-performance computing (HPC), high-performance artificial intelligence (HPAI), and high-performance data analytics (HPDA) with a user environment that prioritizes researcher productivity and ease of use.

Hardware highlights of Bridges-2 include HPC nodes with 128 cores and 256 to 512GB of RAM, scalable AI with 8 NVIDIA Tesla V100-32GB SXM2 GPUs per accelerated node and dual-rail HDR-200 InfiniBand between GPU nodes, a high-bandwidth, tiered data management system to support data-driven discovery and community data, and dedicated database and web servers to support persistent databases and domain-specific portals (science gateways).

User environment highlights include interactive access to all node types for development and data analytics; Anaconda support and optimized containers for TensorFlow, PyTorch, and other popular frameworks; and support for high-productivity languages such as Jupyter notebooks, Python, R, and MATLAB including browser-based (OnDemand) use of Jupyter, Python, and RStudio. A large collection of applications, libraries, and tools will make it often unnecessary for users to install software, and when users would like to install other applications, they can do so independently or with PSC assistance. Novices and experts alike can access compute resources ranging from 1 to 64,512 cores, up to 192 V100-32GB GPUs, and up to 4TB of shared memory.

Bridges-2 will support community datasets and associated tools, or Big Data as a Service (BDaaS), recognizing that democratizing access to data opens the door to unbiased participation in research. Similarly, Bridges-2 is available to support courses at the graduate, undergraduate, and even high school levels. It is also well-suited to interfacing to other data-intensive projects, instruments, and infrastructure.

Bridges-2 will contain three types of nodes: Regular Memory (RM), Extreme Memory (EM), and GPU (Graphics Processing Unit; GPU). These are described in turn below.

Regular Memory (RM) nodes will provide extremely powerful general-purpose computing, machine learning and data analytics, AI inferencing, and pre- and post-processing. Each of Bridges-2’s 504 RM nodes will each consist of two AMD 7742 “Rome” CPUs (64 cores, 2.25-3.4 GHz, 3.48 Tf/s peak), 256-512 GB of RAM, 3.84 TB NVMe SSD, and one HDR-200 InfiniBand adaptor. 488 Bridges-2 RM nodes have 256 GB RAM, and 16 have 512 GB RAM for more memory-intensive applications. Bridges-2 will be HPE Apollo 2000 Gen11 servers.

Extreme Memory (EM) nodes will provide 4TB of shared memory for genome sequence assembly, graph analytics, statistics, and other applications that need a large amount of memory and for which distributed-memory implementations are not available. Each of Bridges-2’s 4 EM nodes will consist of four Intel Xeon Platinum 8260M CPUs, 4 TB of DDR4-2933 RAM, 7.68 TB NVMe SSD, and one HDR-200 InfiniBand adaptor. Bridges-2 will be HPE ProLiant DL385 Gen10+ servers.

GPU (GPU) nodes will be optimized for scalable artificial intelligence (AI). Each of Bridges-2’s 24 GPU nodes will contain 8 NVIDIA Tesla V100-32GB SXM2 GPUs, providing 40,960 CUDA cores and 5,120 tensor cores. In addition, each GPU node will contain two Intel Xeon Gold 6248 CPUs, 512 GB of DDR4-2933 RAM, 7.68 TB NVMe SSD, and two HDR-200 adaptors. Their 400 Gbps connection will enhance scalability of deep learning training across up to 192 GPUs. The GPU nodes can also be used for other applications that make effective use of the V100 GPUs’ tensor cores. Bridges-2 GPU nodes will be HPE Apollo 6500 Gen10 servers.

The Bridges-2 Ocean data management system will provide a unified, high-performance filesystem for active project data, archive, and resilience. Ocean will consist of two tiers – disk and tape – transparently managed by HPE DMF (Data Management Framework) as a single, highly usable namespace, and a third all-flash tier will accelerate AI and genomics. Ocean’s disk subsystem, for active project data, is a high-performance, internally resilient Lustre parallel filesystem with 15 PB of usable capacity, configured to deliver up to 129 GB/s and 142 GB/s of read and write bandwidth, respectively. Its flash tier will provide 9M IOps and an additional 100 GB/s. The disk and flash tiers will be implemented as HPE ClusterStor E1000 systems. Ocean’s tape subsystem, for archive and additional resilience, is a high-performance tape library with 7.2 PB of uncompressed capacity (estimated 8.6 PB compressed, with compression done transparently in hardware with no performance overhead), configured to deliver 50TB/hour. The tape subsystem will an HPE StoreEver MSL6480 tape library, using LTO-8 Type M cartridges. (The tape library is modular and can be expanded, if necessary, for specific projects.)

Bridges-2, including both its compute nodes and its Ocean data management system, is internally interconnected by HDR-200 InfiniBand in a fat tree Clos topology. Bridges-2 RM and EM nodes each have one HDR-200 link (200 Gbps), and Bridges-2 GPU nodes each have two HDR-200 links (400 Gbps) to support acceleration of deep learning training across multiple GPU nodes.

Bridges-2 will be federated with Neocortex, an innovative system also at PSC that will provide revolutionary deep learning capability that accelerates training orders of magnitude. This will complement the GPU-enabled scalable AI available on Bridges-2 and provide transformative AI capability for data analysis and to augment simulation and modeling.


