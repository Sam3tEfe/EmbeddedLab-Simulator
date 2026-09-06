# ⚡ EmbeddedLab Simulator

An open, interactive, and desktop-based simulation platform designed to bridge low-level embedded systems emulation with modern graphical debugging tools.

---

## 🎯 Vision & Objective
Embedded development often faces steep entry barriers: expensive physical debuggers, hardware shortages, and time-consuming flashing cycles. **EmbeddedLab Simulator** leverages the power of industrial emulation engines to provide:
- **Headless Hardware Emulation:** Cycle-accurate Cortex-M execution via Renode.
- **Visual Bus Analysis:** Real-time software-defined I2C, SPI, and UART inspection.
- **Smart Diagnostics:** Context-aware fault localization and register analysis.
- **Frictionless Lab Environment:** Zero hardware setup required for students and firmware engineers.

---

## 🏗️ Architecture Overview
The platform operates on a modular three-tier architecture:

```text
+-------------------------------------------------------------+
|                Graphical User Interface (GUI)               |
|            PyQt6 Desktop Studio & Virtual Canvas            |
+------------------------------+------------------------------+
                               |
                   [Local Socket / JSON IPC]
                               |
+------------------------------v------------------------------+
|                   Bridge & Peripheral Engine                |
|      Python IPC Router - Virtual Sensors (I2C/SPI) Models   |
+------------------------------+------------------------------+
                               |
                      [CLI / Socket Bridge]
                               |
+------------------------------v------------------------------+
|                  Core Emulation Engine                      |
|          Antmicro Renode (Virtual Cortex-M Machine)         |
+-------------------------------------------------------------+
```

---

## 📅 Development Roadmap (Build in Public)

- [ ] **Phase 1: Emulation Core & Socket Bridge**
  - [x] Architecture design & modular repository split
  - [ ] Renode STM32F4 headless environment setup
  - [ ] Bidirectional TCP GPIO event router
- [ ] **Phase 2: Virtual Peripherals & Protocol Inspection**
  - [ ] Software-modeled I2C sensor registers (MPU6050)
  - [ ] Real-time packet parsing & logic analyzer engine
- [ ] **Phase 3: Desktop Studio (PyQt6)**
  - [ ] Dark-themed engineering cockpit
  - [ ] Dynamic hardware pin mapping canvas
  - [ ] Interactive live serial monitor
- [ ] **Phase 4: Intelligent Diagnostics**
  - [ ] Automated HardFault register capture
  - [ ] Context-driven firmware assistance
- [ ] **Phase 5: Packaging & Distribution**
  - [ ] Standalone portable binary distribution

---

## 📝 Engineering DevLogs
Daily progress, architectural decisions, and integration updates are tracked under the [`/devlog`](./devlog) directory.
