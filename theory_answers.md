# Theory Answers

## Part 1: Git & GitHub

### Q1. Git Terms
- **Repository:** A folder tracked by Git storing all project files and history. Example: `git init my-project`
- **Commit:** A saved snapshot of changes. Example: `git commit -m "Add login page"`
- **Branch:** An independent line of development. Example: `git branch feature-login`
- **Merge:** Combining changes from one branch into another. Example: `git merge feature-login`
- **Clone:** Copying a remote repo locally. Example: `git clone https://github.com/user/repo.git`

### Q2. Key Differences
- **git fetch vs git pull:** fetch downloads changes without applying them; pull does fetch + merge automatically.
- **git merge vs git rebase:** merge creates a merge commit preserving full history; rebase replays commits for a cleaner linear history.
- **Local vs Remote:** local repo lives on your machine; remote is hosted on GitHub for collaboration.

### Q3. .gitignore
The .gitignore file tells Git which files to ignore and not track.
- `node_modules/` — auto-generated npm dependencies
- `.env` — contains secret API keys
- `__pycache__/` — Python bytecode files

---

## Part 2: Networking

### Q1. Networking Terms
- **IP Address:** Unique label for a device on a network. Example: 192.168.1.10
- **Subnet Mask:** Separates network and host portions. Example: 255.255.255.0
- **Default Gateway:** Router IP for traffic outside local network. Example: 192.168.1.1
- **CIDR Notation:** Compact IP + prefix format. Example: 192.168.1.0/24
- **Broadcast Address:** Sends data to all devices on subnet. Example: 192.168.1.255

### Q2. IP Classification
| IP Address   | Class | Public/Private        |
|--------------|-------|-----------------------|
| 10.0.0.1     | A     | Private               |
| 172.16.5.10  | B     | Private               |
| 192.168.1.1  | C     | Private               |
| 8.8.8.8      | A     | Public                |
| 224.0.0.1    | D     | Public (Multicast)    |

### Q3. Key Differences
- **IPv4 vs IPv6:** IPv4 is 32-bit (~4.3B addresses); IPv6 is 128-bit (virtually unlimited).
- **TCP vs UDP:** TCP guarantees delivery (web, email); UDP is faster but no guarantee (streaming, gaming).
- **Static vs Dynamic IP:** Static is manually set and fixed; Dynamic is assigned automatically by DHCP.
