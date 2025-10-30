# Experiment - 6

---

## Aim
To understand and demonstrate the usage of Sleuth Kit in analyzing digital evidence for forensic investigation purposes.

---

## Description
The Sleuth Kit (TSK) is a powerful open-source digital forensics toolkit that enables investigators to analyze disk images and recover files. This experiment focuses on using various Sleuth Kit commands and tools to examine digital evidence, recover deleted files, and analyze file system artifacts.

---

## Tools Used
1. The Sleuth Kit (TSK)
2. Command Line Interface
3. Disk Image (for analysis)
4. AutopsyⓇ (GUI frontend for Sleuth Kit)

---

## Procedure

### 1. Installation and Setup
1. Download and install The Sleuth Kit from the official website.
2. Verify the installation by running basic commands.
3. Prepare a disk image for analysis.

### 2. File System Metadata Analysis
1. Use `fsstat` to display the partition layout:

```bash
fsstat -o 0 TestImage.dd
```
<p align="center">
<img width="600" alt="image" src="https://github.com/user-attachments/assets/7932b64e-8f81-454a-a850-59a9d66ce704" />
</p>

### 3. List Files and Directories:
List all files and directories in the disk image:
      
```bash
fls -o 0 TestImage.dd
```

## Observation:
Shows all allocated files. Note the inode numbers for files you want to recover. For example:
r/r 4: testfile.txt
<p align="center">
<img width="600" alt="image" src="https://github.com/user-attachments/assets/7932b64e-8f81-454a-a850-59a9d66ce704" />
</p>

### 4.Recover a File
Extract a file using its inode number:
```bash
icat -o 0 TestImage.dd 4 > recovered_file.txt
```

## Observation:
The file testfile.txt is successfully recovered. You can check its content:
type 
### recovered_file.txt

<p align="center">
<img width="600" alt="image" src="https://github.com/user-attachments/assets/7932b64e-8f81-454a-a850-59a9d66ce704" />
</p>

### 5. Analyze File Metadata:
Use this command to display the metadata of a file:
```bash
istat -o 0 TestImage.dd 4
```
<p align="center">
<img width="600" alt="image" src="https://github.com/user-attachments/assets/7932b64e-8f81-454a-a850-59a9d66ce704" />
</p>

---

# Rubrics

| Criteria | Mark Allotted | Mark Awarded |
|---|---:|---:|
| 1. GitHub Activity & Submission Regularity | 3 | |
| 2. Application of Forensic Tools & Practical Execution | 3 | |
| 3. Documentation & Reporting | 2 | |
| 4. Engagement, Problem-Solving & Team Collaboration | 2 | |
| *Total* | *10* | |

---

## Results

- Successfully identified partition structure.
- Retrieved file system metadata.
- Recovered both active and deleted files.
- Verified timestamps and file attributes.
- Created a timeline of file system activities.
