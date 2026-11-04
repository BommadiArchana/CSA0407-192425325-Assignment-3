# Q6 – Disk Management

## Objective
To understand disk-management mechanisms and evaluate suitable storage configurations for a hospital records server.

## Requirements Covered
- Explain low-level formatting, partitioning and logical formatting.
- Explain the boot block and boot process.
- Explain bad-block handling.
- Decide the size and location of swap space.
- Compare RAID 0, RAID 1, RAID 5 and RAID 10.
- Select a suitable RAID level for the hospital records server.
- Compare a separate swap disk with a swap file.
- View Linux partitions using `lsblk` and `fdisk -l`.
- Display system partitions and swap space.
- Calculate the usable capacity of six 4 TB disks.
- Calculate RAID 1 and RAID 5 data-loss probabilities.
- Measure SSD and HDD read speeds.
- Evaluate RAID 6 as an alternative.

## Program File
- `raid_calculation.c` – Calculates usable storage capacity for RAID 0, RAID 1, RAID 5 and RAID 10.

## Compilation and Execution
```bash
gcc -std=c11 -Wall -Wextra raid_calculation.c -o raid_calculation
./raid_calculation
```

## Linux Commands
```bash
lsblk
sudo fdisk -l
swapon --show
free -h
```

## Experimental Investigation
The usable storage capacity of six disks, each with 4 TB, is calculated for different RAID configurations.

Linux commands are used to inspect disk partitions and swap space. Disk read speeds are measured using available SSD and HDD devices.

## Conclusion
Disk management is important for reliable storage, data protection and efficient access. RAID 5 and RAID 10 provide different combinations of storage capacity, performance and fault tolerance. The final configuration should be selected based on the hospital server's reliability and storage requirements.
