# Understanding the Folder Structure

### Explanation of System Directories

### **Symbolic Links (Less Significant)**
| Directory | Description |
|-----------|-------------|
| `/sbin -> /usr/sbin` | System binaries for administrative commands (linked to `/usr/sbin`). |
| `/bin -> /usr/bin` | Essential user binaries (linked to `/usr/bin`). |
| `/lib -> /usr/lib` | Shared libraries and kernel modules (linked to `/usr/lib`). |

### **Important System Directories**
| Directory | Description |
|-----------|-------------|
| `/boot` | Stores files needed for booting the system (not relevant in containers). |
| `/usr` | Contains most user-installed applications and libraries. |
| `/var` | Stores logs, caches, and temporary files that change frequently. |
| `/etc` | Stores system configuration files. |

### **User & Application-Specific Directories**
| Directory | Description |
|-----------|-------------|
| `/home` | Default location for user home directories. |
| `/opt` | Used for installing optional third-party software. |
| `/srv` | Holds data for services like web servers (rarely used in containers). |
| `/root` | Home directory for the root user. |

### **Temporary & Volatile Directories**
| Directory | Description |
|-----------|-------------|
| `/tmp` | Temporary files (cleared on reboot). |
| `/run` | Holds runtime data for processes. |
| `/proc` | Virtual filesystem for process and system information. |
| `/sys` | Virtual filesystem for hardware and kernel information. |
| `/dev` | Contains device files (e.g., `/dev/null`, `/dev/sda`). |

### **Mount Points**
| Directory | Description |
|-----------|-------------|
| `/mnt` | Temporary mount point for external filesystems. |
| `/media` | Mount point for removable media (USB, CDs). |
| `/data` | Likely your **mounted volume** from Windows (`C:/ubuntu-data`). |

/ (Root): The primary hierarchy breakpoint and the top-level directory of the entire system. All other directories are located under it.

/bin: Contains essential user binaries (executable programs) that are necessary for basic system operation and must be present when the system is mounted in single-user mode (e.g., ls, cp, mv, cat). 

/sbin: Stores essential system binaries and administrative tools (e.g., shutdown, mount, iptables) primarily used by the root user for system maintenance.

/etc: Holds system-wide configuration files and scripts for all applications and services (e.g., /etc/passwd, /etc/hosts). These are generally editable text files.

/dev: A special directory containing device files that represent hardware components and virtual devices (e.g., hard drives: /dev/sda, terminals: /dev/tty).

/proc: A virtual filesystem providing real-time information about running processes and kernel parameters (e.g., /proc/cpuinfo, /proc/meminfo).

/var: Contains variable data files that change frequently, such as system logs (/var/log), mail queues, and caches.

/tmp: A temporary storage directory for files created by applications and users. Its contents are typically cleared upon system reboot.

/usr: A secondary hierarchy that contains the majority of user-level programs, libraries (/usr/lib), documentation, and shared data files.

/home: Contains the personal directories for non-root users. Each user has their own directory here (e.g., /home/username) for their files and user-specific configurations.

/root: The home directory of the root user, separate from the /home directory.

/lib and /lib64: Contain essential shared libraries needed by the binaries in /bin and /sbin.

/opt: Used for installing optional, add-on, or third-party software packages that are not part of the default system installation.

/mnt and /media: These directories serve as mount points for temporarily mounting external storage devices or network filesystems (e.g., USB drives, CDs, additional hard disk partitions).

/boot: Stores files required for the booting process, including the Linux kernel and bootloader files (e.g., GRUB configuration)