# Subnetting Solutions

## Exercise 1: 192.168.10.0/24 → 4 Equal Subnets
Borrowed 2 bits → /26, Block size = 64

| Subnet | Network Address  | First Usable   | Last Usable    | Broadcast      | Mask              | CIDR |
|--------|-----------------|----------------|----------------|----------------|-------------------|------|
| 1      | 192.168.10.0    | 192.168.10.1   | 192.168.10.62  | 192.168.10.63  | 255.255.255.192   | /26  |
| 2      | 192.168.10.64   | 192.168.10.65  | 192.168.10.126 | 192.168.10.127 | 255.255.255.192   | /26  |
| 3      | 192.168.10.128  | 192.168.10.129 | 192.168.10.190 | 192.168.10.191 | 255.255.255.192   | /26  |
| 4      | 192.168.10.192  | 192.168.10.193 | 192.168.10.254 | 192.168.10.255 | 255.255.255.192   | /26  |

## Exercise 2: 172.16.0.0/16 VLSM

### Engineering (200 hosts) → /24
- Network: 172.16.0.0 | Broadcast: 172.16.0.255
- Range: 172.16.0.1 – 172.16.0.254 | Wasted: 54

### HR (50 hosts) → /26
- Network: 172.16.1.0 | Broadcast: 172.16.1.63
- Range: 172.16.1.1 – 172.16.1.62 | Wasted: 12

### Sales (25 hosts) → /27
- Network: 172.16.1.64 | Broadcast: 172.16.1.95
- Range: 172.16.1.65 – 172.16.1.94 | Wasted: 5

### Management (10 hosts) → /28
- Network: 172.16.1.96 | Broadcast: 172.16.1.111
- Range: 172.16.1.97 – 172.16.1.110 | Wasted: 4

## Exercise 3: Troubleshooting
- Computer subnet: 192.168.1.128/26
- Valid host range: 192.168.1.129 – 192.168.1.190
- Gateway 192.168.1.1 is in a DIFFERENT subnet → no communication
- Fix: Change IP to 192.168.1.50 with mask 255.255.255.192
