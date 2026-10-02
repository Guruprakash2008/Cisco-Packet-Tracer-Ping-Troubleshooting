# Cisco-Packet-Tracer-Ping-Troubleshooting

## 📌 Project Overview

This project demonstrates how to create a simple network using **Cisco Packet Tracer** and troubleshoot connectivity problems using the **Ping** command.

The network consists of two PCs connected through a Cisco 2960 switch. Different IP configurations are tested to understand why a ping succeeds or fails.

---

## 🎯 Objective

The main objectives of this project are:

* To create a basic network in Cisco Packet Tracer.
* To configure IPv4 addresses on PCs.
* To test network connectivity using the `ping` command.
* To identify common causes of ping failure.
* To troubleshoot IP addressing and subnet-related problems.
* To understand basic network troubleshooting.

---

## 🛠️ Software Used

* **Cisco Packet Tracer**
* IPv4 Networking
* Windows-style Command Prompt in Packet Tracer

---

## 🌐 Network Topology

The network contains:

      PC0 --- SWITCH --- PC1

### Devices Used

| Device                        | Quantity |
| ----------------------------- | -------: |
| PC                            |        2 |
| Cisco 2960 Switch             |        1 |
| Copper Straight-Through Cable |        2 |

---

## 💻 IP Address Configuration

### PC0

```text
IP Address:    172.16.66.1
Subnet Mask:   255.255.255.0
Default Gateway: Not Required
```

### PC1

```text
IP Address:     172.16.66.2
Subnet Mask:   255.255.255.0
Default Gateway: Not Required
```

Both PCs belong to the same network:

172.16.66.0

## 🔌 Network Connection

The devices are connected using **Copper Straight-Through** cables.

PC0 FastEthernet0
        |
        ↓
Switch FastEthernet0/1

PC1 FastEthernet0
        |
        ↓
Switch FastEthernet0/2

The link indicators should become **green** when the connections are working correctly.


## ⚙️ Procedure

### Step 1: Add Devices

Open Cisco Packet Tracer and add:

* Two PCs
* One Cisco 2960 Switch

### Step 2: Connect the Devices

Use **Copper Straight-Through** cables.

Connect:

PC0 → Switch Fa0/1
PC1 → Switch Fa0/2
```

### Step 3: Configure PC0

Go to:

PC0 → Desktop → IP Configuration

Enter:


IP Address: 172.16.66.1
Subnet Mask: 255.255.255.0

### Step 4: Configure PC1

Go to:

PC1 → Desktop → IP Configuratio

Enter:

IP Address: 172.16.66.2
Subnet Mask: 255.255.255.0

### Step 5: Check IP Configuration

Open:

PC0 → Desktop → Command Prompt

Run:

```text
ipconfig
```

Verify the IP address and subnet mask.

### Step 6: Test Connectivity

From PC0, run:

```text
ping 172.16.66.1

```

If the configuration is correct, the ping should receive replies.

Example:

```text
Reply from 172.16.66.1
Reply from 172.16.66.1
Reply from 172.16.66.1
Reply from 172.16.66.1
```

---

## ❌ Testing a Ping Failure

To demonstrate troubleshooting, change PC1's IP address.

Change:

```text
172.16.66.2
```

to:

```text
172.16.56.2
```

Keep the subnet mask:

```text
255.255.255.0
```

Now run from PC0:

```text
ping172.16.66.2 
```

The ping will fail because the PCs are now configured in different IP networks and there is no router connecting those networks.

---

## 🔍 Troubleshooting

When a ping fails, check the following:

### 1. Check the Cable

Make sure the PCs are connected to the switch using the correct cable.

### 2. Check Link Status

The connection indicators should become green.

### 3. Check IP Address

Run:

```text
ipconfig
```

Make sure the IP address is correct.

### 4. Check Subnet Mask

Both PCs should use:

```text
255.255.255.0
```

### 5. Check Network Address

For the working configuration:

```text
PC0 → 172.16.66.1
PC1 → 172.16.66.2
Network → 192.168.10.0/2
```

### 6. Test Again

After correcting the configuration:

```text
ping 172.16.66.2
```

The ping should succeed.

---

## 🧪 Testing Results

| Test                                 | Result       |
| ------------------------------------ | ------------ |
| PC0 IP configuration                 | Correct    |
| PC1 IP configuration                 | Correct    |
| PC0 → PC1 ping with same subnet      | Successful |
| PC0 → PC1 ping with different subnet | Failed     |
| Correcting IP configuration          | Successful |

---

## 📸 Screenshots

The project can include the following screenshots:

---

## 📂 Project Files
<img width="1366" height="727" alt="image" src="https://github.com/user-attachments/assets/5107e9c0-0fb8-4779-9469-f222331b82b9" />

```text

## 📚 Concepts Covered

* IPv4 Addressing
* Subnet Mask
* Network Address
* Basic LAN Configuration
* Cisco Switch
* Ping Command
* Network Connectivity
* IP Troubleshooting
* Cisco Packet Tracer Simulation

---

## ✅ Result

A basic LAN was successfully created using two PCs and a Cisco 2960 switch. Connectivity was tested using the `ping` command. The project also demonstrated how an incorrect IP configuration can cause ping failure and how correcting the configuration restores connectivity.

---

## 👨‍💻 Author

**Guruprakash**

**Course:** B.Tech – Computer Science and Business Systems

---

## ⭐ Project Status

**Completed**
