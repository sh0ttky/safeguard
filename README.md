# safeguard
---
**safeguard** is a secure, Rust-based & ARM architecture SOC embedded device that automatically scans, sanitizes, signs, and stores files. Designed for air-gapped, high-security military environments, it operates:

on the **hardware** :

a **1.8GHz Quad Cortex-A53** CPU, 4GB of **DDR4** RAM, 32GB of **eMMC** storage & a Variety of IO periphirals.

on the **software** :

- Custom **safeguard_linux** embedded distribution.
- Real-time malware scanning.
- Content Disarm & Reconstruction in storage mode.
- File integrity signing and encryption.
- Dual operating modes: Normal (Scan) and Storage (Sanitize + Certify).
- Secure, minimal runtime.
- Added security layer with sandboxing.
- Secure logging with persistent trail.




## Component
---

![Untitled Diagram drawio (2)](https://github.com/user-attachments/assets/30916f99-5e35-4b5d-878d-fc68e0e515d4)



| Component              | Purpose                                      |
|--------------------|----------------------------------------------|
| `HAL: hardware_abstraction_layer` | Controls GPIO, USB mode, and low-level device access |
| `logger`           | Central logging facility across all components                    |
| `io`               | Manages USB and file I/O                     |
| `sandboxer`          | Oversees and manages secured sandboxes    |
| `scanner`          | Runs Signature based AV and YARA       |
| `cdr`       | CDR engine that Disarms & reconstructs storage files     |
| `certificator`     | Signs and encrypts sanitized content         |
| `builder`          | Updates AV/YARA rules definitions on device    |

