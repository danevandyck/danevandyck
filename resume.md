Dane Van Dyck  
132 West Davis Street  
Decatur, GA 30030  
408-892-4138  
dnvandyck@gmail.com


EXPERIENCE
==========

Axcient
-------

### Software Engineer, Fall 2012 to 2016

### Senior Software Engineer, 2016 to 2018

### Lead Software Engineer, 2018

_technical leadership of Axcient's Storage and Recovery Cloud_

Axcient provides end-to-end Disaster Recovery as a Service, beginning with the
replication of protected devices and extending to file and folder recovery,
restore point export and business continuity. The Storage and Recovery Cloud is
the core of that service, exposing secure ReSTful interfaces to replication
clients, end users and the UI. I have either contributed to or led the
development teams responsible for building it. Core concepts are filesystems,
virtualization, networking, deduplicated storage and web services.

_leadership_

- technical guidance of a distributed team of five developers (plus 1 QA and 1
  SRE) with mixed experience
- technical oversight of Axcient's Storage and Recovery Cloud
- thorough and continual code reviews
- daily backlog refinement and prioritization
- organization of weekly bug scrubs with support and QA
- creation, maintenance and socialization of a multi-quarter roadmap with
  product and engineering leadership
- "automate everything" approach to regression testing supporting regular and
  frequent minor releases
- "document everything" approach to development supporting rapid onboarding

_virtual private guest networks_

- virtual IPv4 guest networks embedded within an IPv6 host network
- securely separated overlapping virtual IPv4 address spaces supporting
  guest-internet and guest-guest traffic
- DNS and DHCP services for virtual IPv4 network guests
- IPSec VPN access to virtual IPv4 guest networks

_distributed workqueue_

- proposal, design and implementation of a distributed, asynchronous
  workqueue
- consistent task ownership across many workers without large-scale
  consensus
- modular task definitions and generic ReSTful client APIs
- scalable "pull" architecture, long-polling workers
- reassignment of stale tasks through a configurable TTL

_zero-amplification block storage_

- design and implementation of block storage index and object storage formats
  supporting zero-amplification reads of content-addressable blocks
- design and implementation of a block storage object keyspace supporting
  unbounded read operation throughput
- design and implementation of concurrent, performant C++ block
  storage client interface and corresponding Python extension
- optimization of block index schema reducing aggregate storage size by
  approximately forty percent

_live migration of block storage_

- live migration to new block storage index and object storage formats of
  petabytes of protected data for hundreds of customers
- throughput approaching five gigabytes per second and hundreds of thousands of
  block indices per second over thousands of concurrent nodes

_virtual block device driver_

- read-write network block device (NBD) backed by remote block storage
- persistent read/write caching and adaptive prefetching
- explicit prefetching of particular extents through socket commands
- write barriers supporting consistent storage for e.g. virtual machines
- multiple connections supporting virtual machine migration

_file and folder recovery_

- ReSTful HTTP interface supporting browsing, downloads and streaming archive
  downloads at throughputs approaching one hundred megabits
- partition and filesystem detection supporting common flavors
- prefetching of special files/attributes supporting performant access to
  filesystem roots
- file data and directory index extent identification and prefetching
  supporting performant browsing and file download
- pipelined prefetch/traversal/read stages front-loading I/O for archive
  downloads

_build infrastructure_

- design and implementation of packaging infrastructure
  * per-target dependency maps generated at configuration time
  * per-target installation scripts generated at configuration time
  * transitive installation of package component dependencies to package
  * runpath modification of packaged shared libraries and binaries
  * generation and installation of soname symlinks in packages
- addition of custom targets supporting complex artifact types
  * protobuf libraries, Python extensions, pypi package archives
- derivation of artifact versions from VCS tags

_disk image export_

- rapid synthesis of protected disk images from block storage for download
  and physical export
- single stream throughput approaching one GB per second to a single S3 object
- orchestration infrastructure supporting concurrent export of many disk images


Riverbed Technology, Software Engineer, Summer 2011 to Fall 2012
----------------------------------------------------------------

_software development for Riverbed's Whitewater Cloud Storage Gateway_

Whitewater was a NAS appliance backed by public object storage intending to
replace tape as a backup software target. The Whitewater filesystem was
transactional, supporting rollback on failure or unplanned shutdown. Memory
arena management for caching and consistent garbage collection were primary
concepts, as was deduplication. Most of my time was spent fixing bugs and
addressing performance problems.

_reduction of transaction log replay time in the event of a crash_

- design and implementation of an transaction log checkpointing scheme
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


Cirtas Systems, Developer in Test, Winter 2010 to Summer 2011
-------------------------------------------------------------

#### Developer in Test, Winter 2010 to Summer 2011

_performance testing and automation for an early-stage cloud storage startup_

Cirtas's Bluejet Cloud Storage Controller appliance implemented a network block
storage service, exposing iSCSI LUNs backed by public object storage and
APIs and UI to manage them. Relevant concepts were iSCSI, LBAs, deduplication
and snapshots. My work focused on performance testing, including data
generation and metrics collection.

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
- two-phase commit, transaction abort

_posix storage_

- durability, fsync, msync, buffer cache, write back, write barrier
- shared memory, memory mapping, copy on write

_HTTP_

- ReSTful interfaces, long polling
- connection pooling, websockets, ranged GET
- HTTP status codes, redirection, retryable status codes
- authentication, client certificate checking
- authorization, authorization tokens, scope of authorization,
  token time-to-live, macaroons, JSON Web Tokens, OAuth2

_databases_

- data structure serialization, protocol buffers, pickling, JSON
- serial consistency, quorum, eventual consistency, Cassandra, CQL
- Log Structured Merge Trees, key ordering/scanning, LevelDB/RocksDB

_networking_

- iptables, connection tracking, masquerading, packet marking, policy based
  routing, destination NAT
- IPv6, SIIT (EAMT)
- bridge interfaces, proxy arp, tun/tap, network namespaces

_programming_

- thread parallelism, data races, deadlocks, mutexes, condition variables
- non-blocking socket I/O, socket timeouts, `select`
- object oriented programming, data structure immutability, RAII
- C++ 11/14, templates, exception safety, move semantics, rule of three/five,
  threading library, atomics
- Python 3, context managers, iteration interface, `asyncio`, `tornado`,
  threading, concurrent futures, multiprocessing, requests, logging,
  C/C++ extensions
- CMake, CTest, macros and functions, custom targets/commands,
  installation mechanics

_platforms_

- systemd, service unit files
- shared libraries, linking, runpath modification, ld library path, ldconfig
- debian packaging, control files, changelog, version ordering

_AWS services_

- S3, ranged GETs, multipart uploads, object tagging, object lifecycles,
  storage classes, intelligent tiering
- DynamoDB, write/read capacity utilization, batched writes, provisioned
  capacity, attributes, background repartitioning, key design
- Lambda, SQS triggers, log groups, execution environment

_miscellaneous_

- Etcd v3, MultiOp transactions, prefix-based event watching,
  leases/keep-alives
- NBDKit, flush semantics
- HAProxy, SSL termination, ACLs, client verification, request timing


EDUCATION
=========

Georgia Institute of Technology
-------------------------------

- Bachelor of Science, Computer Science, _summa cum laude_
  * concentrations: networking and platforms
  * highest ranking member of graduating class, College of Computing


REFERENCES
==========

Axcient
-------

- Kevin Hoffman, CTO
- Justin Moore, Founder and CEO
- Anuradha Krishnan, VP of Engineering
- Aaron Brown, Lead Developer

Riverbed Technology
-------------------

- Greg Taleck / Richard Hefner, Engineering Managers
- Vivasvat Keswani, Director of Engineering
- Ka-Hing Cheung / Zoheb Shivani / Salil Gokhale, Members of Technical Staff

Cirtas Systems
--------------

- Dan Decasper, President of Engineering
- Allen Samuels, Chief Architect
- Shiva Ankam / Olaf Manzcak / Sandeep Ranade, Engineers
