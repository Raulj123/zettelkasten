Storage is a mechanism that enables a system to retain data, either temporarily or permanently.

Where RAID Fits in the Big Picture
* **RAID is for hardware (drives):** It manages **how data is physically stored** on your hard drives or SSDs. Think of it as a safety or speed mechanism for your storage devices.
# Raid 
RAID (Redundant Array of Independent Disks) is a way of storing the same data on multiple hard disks or solid-state drives (SSDs) to protect data in the case of a drive failure.
* Different RAID levels 
* Not all have the goals of providing redundancy(copies)
# Types 
* RAID 0 
	* Also known as striping, data is split evenly across all the drives in the array.
* RAID 1
	* Also known as mirroring, at least two drives contains the exact copy of a set of data. If a drive fails, others will still work.
* RAID 5
	* Striping with parity. Requires the use of at least 3 drives, striping the data across multiple drives like RAID 0, but also has a parity distributed across the drives.
* RAID 6
	* Striping with double parity. RAID 6 is like RAID 5, but the parity data are written to two drives.
* RAID 10
	* combines striping plus mirroring from RAID 0 and RAID 1. It provides security by mirroring all data on secondary drives while using striping across each set of drives to speed up data transfers.

#### **Volume**

- A fixed amount of storage on a disk.
- A single disk can have multiple volumes, or a volume can span multiple disks.

---

#### **File Storage**

- Stores data as files in a directory structure (easy to navigate).
- Files are accessed using their full path.
- Found on hard drives.
    - **Examples:** Amazon EFS, Google Filestore.

---

#### **Block Storage**

- Splits data into blocks (chunks) with unique IDs.
- Blocks can be stored anywhere, enabling fast retrieval.
- Great for spreading data across multiple environments.
    - **Examples:** Amazon EBS.

---

#### **Object Storage**

- Breaks data into objects stored in a central repository.
- Ideal for large-scale distributed systems.
    - **Examples:** Amazon S3, Azure Blob Storage.

---

#### **NAS (Network Attached Storage)**

- A storage device connected to a network for centralized data access.
- Expandable and provides cloud-like storage on-site.

---

#### **HDFS (Hadoop Distributed File System)**

- Designed for big data storage across many low-cost machines.
- Files are split into blocks and replicated for fault tolerance.