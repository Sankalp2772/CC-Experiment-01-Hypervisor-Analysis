# Hypervisor Performance Analysis

## Type-1 vs Type-2 Hypervisor Performance Analysis

### Experiment

Performance Analysis of Type-1 and Type-2 Hypervisors

### Hypervisors Used

- Type-1: Proxmox VE
- Type-2: VMware Workstation

### Guest Operating System

Ubuntu

---

## 1. Objective

To analyze and compare the CPU performance of a virtual machine running on a Type-1 hypervisor (Proxmox VE) and a Type-2 hypervisor (VMware Workstation) using the Sysbench CPU benchmark.

---

## 2. Experimental Configuration

To ensure a fair comparison, identical virtual machine resource configurations were used for both hypervisors.

| Resource | Type-1: Proxmox VE | Type-2: VMware Workstation |
|---|---|---|
| Hypervisor Type | Type-1 | Type-2 |
| Guest Operating System | Ubuntu | Ubuntu |
| CPU | 2 vCPU | 2 vCPU |
| Memory | 2 GB | 2 GB |
| Disk | 20 GB | 20 GB |
| Benchmark Tool | Sysbench | Sysbench |

The lab requires identical VM configurations for the Type-1 and Type-2 environments so that the performance results can be compared under the same resource allocation.

---

## 3. Benchmark Method

The CPU performance was measured using Sysbench with the following command:

```bash
sysbench cpu --cpu-max-prime=20000 run
