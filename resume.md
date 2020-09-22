Dane Van Dyck  
132 West Davis Street  
Decatur, GA 30030  
408-892-4138  
dnvandyck@gmail.com


EXPERIENCE
==========

Axcient
-------

### Lead Software Engineer, 2018

### Senior Software Engineer, 2016 to 2018

### Software Engineer, Fall 2012 to 2016

_technical leadership of Axcient's Fusion platform_ 

Axcient provides disaster recovery as a service in the public cloud. Fusion is
the core of that service, exposing secure RESTful interfaces to replication
clients, end users and user interfaces. Relevant technical domains are
filesystems, virtualization, networking, deduplicated storage and web services.

_leadership_

As a team lead, I provided technical guidance to a distributed team
of seven engineers, and maintained architectural and operational oversight of
the public cloud platform for Axcient's DRaaS offering.

- regular feedback sessions with team members
- documentation policies facilitating onboarding and transfer of information
- test automation policies supporting a regular release cadence
- devops policies supporting continuous integration without SREs
- maintenance of a roadmap with product and engineering leadership
- backlog refinement and prioritization
- escalation and bug scrubs with support and QA

_multi-tenant overlay networking_

Implementation of a multitenant layer three overlay network in the public
cloud, clearing the chief technical barrier to COGS rearchitecture of the
Fusion platform. Design, prototyping and oversight of development.

- overlay networking in the public cloud without broadcast support or
  tunnelling
- support for live additions of overlay (guests) and fabric (hosts)
  participants
- agnostic with respect to the layout of guests on hosts
- overlay network support for egress and ingress traffic
- overlay network support for DNS and DHCP services

<div style="page-break-after: always"></div>

_zero-amplification block storage_

Design and development of a novel block store schema to eliminate read
amplification, enabling use of Fusion block storage as a backing store for
virtual machines.

- block storage index and object formats supporting zero-amplification reads
- a block storage object keyspace supporting unbounded operation throughput
- a performant C++ block storage client interface and Python extension
- block index schema optimization reducing aggregate storage size by 2x

_live migration of block storage_

Design and oversight of the live migration and verification of Fusion block
storage to a new block storage schema.

- migration of petabytes of protected data and tens of billions of block
  indices for hundreds of customers
- throughput approaching five gigabytes per second and hundreds of thousands of
  block indices per second over thousands of concurrent executors

_virtual block device driver_

Presentation of Fusion block storage as a logical block device, providing
storage for file and folder recovery and virtualization usecases. Design,
oversight of development and performance optimization.

- read-write network block device (NBD) backed by remote block storage
- persistent read/write caching and adaptive prefetching
- write barriers supporting consistent storage for e.g. virtual machines

_file and folder recovery_

File and folder browsing and download of restore points through secure RESTful
APIs. Design and co-development.

- RESTful HTTP interface secured by token-based client authorization
- supporting browsing, downloads and streaming archive downloads
- support for various common partition and filesystem types
- NTFS attribute extent identification and prefetching
- pipelined architecture front-loading high-latency I/O

<div style="page-break-after: always"></div>

Riverbed Technology, Software Engineer, Summer 2011 to Fall 2012
----------------------------------------------------------------

_software development for Riverbed's Whitewater Cloud Storage Gateway_

Whitewater was a NAS appliance backed by public object storage. The Whitewater
filesystem was transactional, supporting rollback on failure or unplanned
shutdown. Memory arena management for caching and consistent garbage collection
were primary concepts, as was deduplication. My primary responsibilities were
addressing bugs and performance problems.

_reduction of transaction log replay time in the event of a crash_

- design and development of an transaction log checkpointing scheme
- decoupling log replay time from log rotation frequency

_2x speedup of large file deletions_

- fixed a performance problem in a deployed release
- parallelisation of metadata updates for deleted blocks
- addition of short-circuit evaluation to a widely used task-management
  abstraction
- instrumentation, reporting and analysis of performance statistics

_discovery and correction of bug in cache-eviction mechanism_

- unprompted observation of poor cache eviction performance
- correction of misuse of standard template library (STL) reverse iterator
  usage
- 2x increase in the effectiveness of cache-eviction sweeps

_design to revise an aspect of the core architecture_

- identification and technical description of a product behavior affecting the
  performance of a core usecase
- a design to address the issue comprehensive with respect to both the
  consistency and the scope of proposed change
- sophisticated use of a transaction log to decouple the maintenance of
  persistent reference counts on block storage from the replication data path

<div style="page-break-after: always"></div>

Cirtas Systems, Developer in Test, Winter 2010 to Summer 2011
-------------------------------------------------------------

#### Developer in Test, Winter 2010 to Summer 2011

_performance testing and automation for an early-stage cloud storage startup_

Cirtas's Bluejet Cloud Storage Controller appliance implemented a network block
storage service, exposing iSCSI LUNs backed by public object storage. Relevant
concepts were iSCSI, deduplication and snapshots. I spent most of my time
performance and load testing.

_pseudo-random data generation_

- accurately tunable compression (LZ) and deduplication of generated data
- generation at memory speed from a fixed-size dataset computed at program
  initialization according to parameters
- performant C++ core exposed as a Python interface with `ctypes`

_performance testing_

- recordable/replayable test configurations
- synchronization of load generating processes across hosts
- metrics gathering and reporting

#### Under Contract, Fall to Winter 2009

I prototyped a web interface built using C# and Managed Extensions for C++.

Web Development
---------------

#### Bold Spring Nursery (under contract), Fall to Winter 2009

I designed and implemented an XLS/MySQL import system using Drupal and PHP so
that the website administrator could more easily update product availabilities.

#### JHouse Media (part time), Summer to Winter 2009

I helped a company develop and maintain websites for various clients. The
relevant technologies were the LAMP stack and MySQL.

<div style="page-break-after: always"></div>

Undergraduate Research, GaTech
------------------------------

#### College of Computing, Spring 2008 to Spring 2009

Our research focused on the runtime identification of basic blocks for the
purpose of JIT recompilation and optimization. I researched program
optimization techniques and instrumented bytecode using the C++ STL and the
LLVM Compiler Infrastructure.

_bytecode instrumentation_

* generation and instrumentation of bytecode using the
  [LLVM Compiler Infrastructure](https://github.com/llvm/llvm-project)

#### College of Computing, Spring to Summmer 2009

The subject of this research was embedded device and network security,
including IP routing techniques and OS virtualization. I worked with the
Android operating system using a variety of toolchains and embedded devices.

_cross-compilation and deployment of Android_

* cross-compilation of Android
* mobile device flashing and virtualization

#### Electronic Systems Laboratory, Spring to Summmer 2009

I worked with a red team at a GaTech affiliated laboratory to identify and
describe network security vulnerabilities.

_pen-testing_

* identified and documented actual network vulnerabilities
* configured routing tables and a DNS server under Ubuntu and Red Hat

_documentation_

* utilized and developed documentation for various network/OS security tools
* customized a MediaWiki server installation under Red Hat

<div style="page-break-after: always"></div>

SKILLSET
========

_deduplication, compression and encryption_

* Merkle Trees, fanout and block size, size computation, change propagation
* LZ compression, rolling windows, worst case deflation
* common cipher initialization/update/finalization interfaces,
  initialization vector randomization

_filesystems_

- inodes and dentries, VFS
- NTFS, MFT, resident and non-resident attributes, ntfs-3g, ntfsprogs
- libfuse, low-level fuse
- Logical Volume Manager (LVM)

_transactions_

- transaction logging, log replay
- two-phase commit, transaction rollback

_posix storage_

- durability, fsync, write barrier
- memory mapping, msync, buffer cache, write back

_HTTP_

- RESTful interfaces, long-polling
- connection pooling, websockets, ranged GET
- HTTP status codes, redirection, retryable status codes
- authentication, client certificate checking
- authorization, auth tokens, scope of authorization, macaroons, OAuth2

_databases_

- data structure serialization, protocol buffers, pickling, JSON
- serial consistency, quorum, eventual consistency, Cassandra, CQL
- Log Structured Merge Trees, key ordering/scanning, LevelDB/RocksDB

_networking_

- iptables, connection tracking, masquerading, packet marking, policy based
  routing
- IPv6, SIIT (EAMT)
- bridge interfaces, proxy arp, network namespaces

_programming_

- thread parallelism, data races, deadlocks, mutexes, condition variables
- non-blocking socket I/O, socket timeouts, select
- object oriented programming, data structure immutability, RAII
- C++ 11/14, templates, exception safety, move semantics, threading library,
  atomics
- Python 3, context managers, asyncio, tornado, threading, multiprocessing,
  C/C++ extensions
- CMake, CTest, macros and functions, custom targets/commands

<div style="page-break-after: always"></div>

_platforms_

- systemd, service unit files
- shared libraries, linking, runpath modification, ldconfig
- debian packaging, version ordering

_AWS services_

- S3, multipart uploads, object tagging, object lifecycles, storage classes,
  intelligent tiering, key design
- DynamoDB, write/read capacity utilization, batched writes, provisioned
  capacity, attributes, background repartitioning, key design
- Lambda, SQS triggers, log groups, execution environment

_miscellaneous_

- Etcd v3, MultiOp transactions, prefix-based event watching, leases
- NBDKit, flush semantics
- HAProxy, SSL termination, ACLs, client verification, request timing


EDUCATION
=========

Georgia Institute of Technology
-------------------------------

- Bachelor of Science, Computer Science, _summa cum laude_
  * concentrations: networking and platforms
  * highest ranking member of graduating class, College of Computing
