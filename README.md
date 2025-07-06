# safeguard
Embedded device to scan and detect malware On The Go on industrial appliances, could be used as a safe storage unit equipped with an advanced CDR engine.


---

## Overview

**safeguard** is a secure, Rust-based embedded device that automatically scans industrial and high risk appliances ( in host mode ), sanitizes, signs, and stores files. Designed for air-gapped, high-security military environments, it operates:

on the **hardware** :
a **1.8GHz Quad Cortex-A53** CPU, 4GB of **DDR4** RAM, 32GB of **eMMC** storage & a Variety of IO periphirals.
on the **software** :
- Real-time malware scanning
- Content Disarm & Reconstruction in storage mode
- File integrity signing and encryption
- Dual operating modes: Normal (Scan) and Storage (Sanitize + Certify)
- Secure, minimal runtime ( added security layers with sandboxing )
- Custom board & hardware optimized for this application 
- Secure logging with persistent trail.


---

## Component

| Crate              | Purpose                                      |
|--------------------|----------------------------------------------|
| `scanner`          | Runs ClamAV and YARA       |
| `cdr_engine`       | Disarms & reconstructs PDF and doc files     |
| `certificator`     | Signs and encrypts sanitized content         |
| `builder`          | Updates ClamAV/YARA rules definitions on device    |
| `io`               | Manages USB and file I/O                     |
| `hardware_abstraction_layer` | Controls GPIO, USB mode, and low-level device access |
| `logger`           | Central logging facility                     |
| `normal_mode`      | Binary: Normal scan mode                     |
| `storage_mode`     | Binary: Storage/CDR mode                     |

![Untitled Diagram drawio (1)](https://github.com/user-attachments/assets/824f0e5b-62f3-4ccc-adfb-f79c5af3c48c)

