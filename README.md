# CSC3044-Computer-Security

## 1.0 Password

privileged EXEC mode: KLsecure@2026

username: NetAdmin

password: AdminP@ss2026

---

## 2.0 IP Address Table

### 2.1 Router Malaysia

| Interface | Ip Address | Subnet Mask | Explaination                |
| --------- | ---------- | ----------- | --------------------------- |
| Se 0/0/0  | 100.64.0.6 | /30         | Connect with ISP            |
| Gig 0/0   | 10.20.0.1  | /30         | Connect with ASA1 (outside) |

---

### 2.2 ISP Router

| Interface | Ip Address | Subnet mask | explanation           |
| --------- | ---------- | ----------- | --------------------- |
| Se 0/0/0  | 100.64.0.2 | /30         | Connect with SG       |
| Se0/0/1   | 100.64.0.5 | /30         | Connect with Malaysia |

---

### 2.3 Singapore Router

| Interface | ip address | subnet mask | explanation                  |
| --------- | ---------- | ----------- | ---------------------------- |
| Se 0/0/0  | 100.64.0.1 | /30         | Connect with ISP             |
| Gig 0/0   | 10.10.0.1  | /30         | Connect with ASA0  (outside) |

---

### 2.4 Singapore ASA0

| interface | ip address | subnet mask | explanation            |
| --------- | ---------- | ----------- | ---------------------- |
| Gig 1/1   | 10.10.0.2  | /30         | Connect with SG Router |
| Gig 1/2   | 10.10.1.1  | /24         | Connect with Switch 4  |

---

###2.5 Singapore Switch

| interface | ip address | subnet mask | explanation           |
| --------- | ---------- | ----------- | --------------------- |
| Fa 0/2    | -          | -           | Connect with  PC10    |
| Fa 0/3    | -          | -           | Connect with Laptop 0 |
| Fa 0/4    | -          | -           | Connect with PC11     |

---

### 2.6 Singapore End Device

| Device   | Interface | ip address | subnet mask | Default gateway |
| -------- | --------- | ---------- | ----------- | --------------- |
| PC 10    | Fa 0      | 10.10.1.10 | /24         | 10.10.1.1       |
| Laptop 0 | Fa 0      | 10.10.1.12 | /24         | 10.10.1.1       |
| PC 11    | Fa 0      | 10.10.1.11 | /24         | 10.10.1.1       |

---

### 2.7 Malaysia ASA1

| Interface         | ip address | subnet mask | explanation                          |
| ----------------- | ---------- | ----------- | ------------------------------------ |
| Gig 1/1 (outside) | 10.20.0.2  | /30         | Connect with Malaysia Router         |
| Gig 1/2 (inside)  | 10.20.2.1  | /30         | Connect with Multilayer Switch (MLS) |
| Gig 1/3 (dmz)     | 10.20.1.1  | /24         | Connect with Switch 0                |

---

### 2.8 VLAN

| Vlan | name        | interface | ip address | subnet mask | device  |
| ---- | ----------- | --------- | ---------- | ----------- | ------- |
| 10   | SALES       | VLAN 10   | 10.20.10.1 | /24         | PC1,2,3 |
| 20   | ENGINEERING | VLAN 20   | 10.20.20.1 | /24         | PC4,5,6 |
| 30   | FINANCE     | VLAN 30   | 10.20.30.1 | /24         | PC7,8,9 |
| 99   | MANAGEMENT  | VLAN 99   | 10.20.99.1 | /24         | PC0     |

---

### 2.9 DMZ Server

| device | ip address | subnet mask | default gateway |
| ------ | ---------- | ----------- | --------------- |
| Web    | 10.20.1.2  | /24         | 10.20.1.1       |
| Email  | 10.20.1.3  | /24         | 10.20.1.1       |
| FTP    | 10.20.1.1  | /24         | 10.20.1.1       |
| DNS    | 10.20.1.5  | /24         | 10.20.1.1       |

---

### 2.10 Multilayer Switch 0 (MLS)

| interface | ip address | subnet mask | explanation                |
| --------- | ---------- | ----------- | -------------------------- |
| Gig 0/1   | 10.20.2.2  | /30         | Connect with ASA1 (inside) |

