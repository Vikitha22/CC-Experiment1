# Performance Analysis of Type-1 and Type-2 Hypervisors

## Experiment Title

**Performance Analysis of Type-1 and Type-2 Hypervisors: Proxmox VE vs VMware Workstation**

## Objective

To analyze and compare the performance of a Type-1 hypervisor and a Type-2 hypervisor by running identically configured Ubuntu virtual machines and measuring their CPU performance using Sysbench.

## Hypervisors Used

### Type-1 Hypervisor – Proxmox VE

Proxmox VE is a Type-1 hypervisor that runs directly on the physical hardware. It is used to create and manage the Ubuntu virtual machine.

### Type-2 Hypervisor – VMware Workstation

VMware Workstation is a Type-2 hypervisor that runs on top of the host operating system. It is used to create and run the Ubuntu virtual machine.

## Virtual Machine Configuration

The same virtual machine configuration is used for both hypervisors to provide a fair performance comparison.

| Configuration | Value |
|---|---|
| Operating System | Ubuntu |
| CPU | 2 vCPU |
| RAM | 2 GB |
| Disk | 20 GB |
| Network | NAT / vmbr0 |
| Benchmark Tool | Sysbench |
| CPU Benchmark | `sysbench cpu --cpu-max-prime=20000 run` |

## Methodology

The experiment was performed in the following steps:

1. Created an Ubuntu virtual machine using Proxmox VE.
2. Configured the VM with 2 vCPU, 2 GB RAM and 20 GB disk.
3. Verified the CPU and memory configuration using `lscpu` and `free -h`.
4. Installed and executed Sysbench CPU benchmark.
5. Recorded the Sysbench performance results.
6. Created an Ubuntu virtual machine using VMware Workstation with the same configuration.
7. Verified the CPU and memory configuration.
8. Executed the same Sysbench CPU benchmark.
9. Recorded the VMware performance results.
10. Compared the results obtained from both hypervisors.

## Type-1 Hypervisor – Proxmox VE

The following screenshots document the Proxmox VE experiment:

- Proxmox dashboard
- Virtual machine configuration
- Virtual machine running
- Ubuntu console
- System configuration
- Sysbench benchmark result
- Resource monitoring

Screenshots are available in:

`screenshots/type1-proxmox/`

## Type-2 Hypervisor – VMware Workstation

The following screenshots document the VMware Workstation experiment:

- Virtual machine configuration
- Virtual machine running
- System configuration
- Sysbench benchmark result

Screenshots are available in:

`screenshots/type2-vmware/`

## Performance Benchmark

The CPU benchmark was performed using:

```bash
sysbench cpu --cpu-max-prime=20000 run
