# Run Hadoop 2.7 inside docker container in Multi-Node Cluster mode

## Install Docker CE on Ubuntu

Follow the instructions from [Get Docker CE for Ubuntu](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/) page.


## Manage Docker as a non-root user

Follow the instructions from [Post-installation steps for Linux](https://docs.docker.com/engine/installation/linux/linux-postinstall/#manage-docker-as-a-non-root-user) page.


## How to Run
- Go to your terminal.
- Clone this repository and go inside it
	```
	git clone https://github.com/mjaglan/docker-hadoop-distributed-mode.git
	cd docker-hadoop-distributed-mode
	```
- Run the following script
	```
	. ./restart-all.sh
	```

## After Starting Hadoop System

The [hadoop-services.sh](scripts/hadoop-services.sh) is running following commands after starting Hadoop Multi-Node Cluster -

- Java Virtual Machine Process Status Tool (jps)
	```
   <pid>   <process name>
	142    org.apache.hadoop.hdfs.server.namenode.NameNode
	428    org.apache.hadoop.hdfs.server.namenode.SecondaryNameNode
	579    org.apache.hadoop.yarn.server.resourcemanager.ResourceManager
	```

- Basic Hadoop filesystem information and statistics
	```
	Configured Capacity: 37912903680 (35.31 GB)
	Present Capacity: 11530969088 (10.74 GB)
	DFS Remaining: 11530944512 (10.74 GB)
	DFS Used: 24576 (24 KB)
	DFS Used%: 0.00%
	Under replicated blocks: 0
	Blocks with corrupt replicas: 0
	Missing blocks: 0
	Missing blocks (with replication factor 1): 0
	
	-------------------------------------------------
	Live datanodes (3):
	
	...
	```
 
- Hadoop Terasort Benchmark Test

- (Optional) Hadoop NNBENCH Test

- (Optional) Hadoop MRBENCH Test

## Tools
```
Docker version 17.06.0-ce
Ubuntu Trusty 14.04 Host OS
Eclipse IDE for Java EE Developers Oxygen (4.7.0)
Eclipse Docker Tooling 3.1.0
```
