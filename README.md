  # ColorSortingConveyor_TwinCAT3
<img width="474" height="284" alt="image" src="https://github.com/user-attachments/assets/763e576f-023a-4ce6-96c3-f019c70ab29a" />

**Automated industrial color-based sorting conveyor** implemented in **Beckhoff TwinCAT 3**.

This project demonstrates a complete PLC-based automation solution for detecting colored objects on a conveyor belt and sorting them into designated bins using pneumatic actuators or diverters. Built with Beckhoff's TwinCAT 3 engineering environment, it showcases modern industrial control practices including structured PLC programming, real-time control, and integration-ready architecture.

![Project Overview](https://via.placeholder.com/800x400/0066cc/ffffff?text=Color+Sorting+Conveyor+System)  
*(Add a real screenshot or GIF of the running system here – highly recommended)*

## ✨ Features

- **Real-time color detection** and classification (RGB/HSV-based or sensor-driven)
- **Conveyor belt control** with variable speed and positioning
- **Automated sorting logic** using pneumatic cylinders or servo diverters
- **Object tracking** along the conveyor
- **Fault handling** and safety interlocks
- **Modular, object-oriented PLC code** (IEC 61131-3 + TwinCAT OOP extensions)
- **Ready for HMI integration** (TwinCAT HMI or third-party SCADA)
- **Simulation-friendly** structure for testing without physical hardware

## 🏗️ Project Structure
ColorSortingConveyor_TwinCAT3/
├── ColorSortingConveyor/              # Main TwinCAT 3 project
│   ├── ColorSortingConveyor.tsproj    # TwinCAT project file
│   ├── MAIN/                          # Primary PLC code
│   ├── _Boot/                         # Boot and initialization
│   └── ... (POUs, Function Blocks, Tasks, etc.)
├── Color detection projects.sln       # Visual Studio solution (color detection component)
└── README.md

### Key Components
- **PLC Logic**: Main task handling conveyor control, sensor reading, color classification, and actuator commands
- **Color Detection Module**: Integrated or separate vision/sensor logic (supports extension with TwinCAT Vision or external camera)
- **State Machine**: Clean implementation for different operating modes (Idle, Running, Fault, Manual, etc.)

## 🚀 Getting Started

### Prerequisites
- **Beckhoff TwinCAT 3** (XAE) installed (version 4024.0 or higher recommended)
- TwinCAT 3 runtime on target PC or virtual machine
- Beckhoff hardware (optional for simulation): EK1100, ELxxxx I/O terminals, color sensor, conveyor drive, pneumatic valves
- Visual Studio 2019/2022 with TwinCAT extensions

### Installation & Deployment
1. Clone the repository:
   ```bash
   git clone https://github.com/AlvinNgo-dev/ColorSortingConveyor_TwinCAT3.git
2. Open Color detection projects.sln or directly open ColorSortingConveyor/ColorSortingConveyor.tsproj in TwinCAT Engineering (XAE).
3. Activate the configuration and download to the target.
4. Start the PLC task and monitor variables via the online view.
Configuration
Adjust I/O mapping in the TwinCAT System Manager according to your hardware.
Tune color detection thresholds in the dedicated function blocks.
Modify conveyor speed and timing parameters in the main program.

📊 System Analysis & Performance
Sorting Performance (Typical Values)
<img width="342" height="146" alt="image" src="https://github.com/user-attachments/assets/bed09fbf-47d0-459b-a9ed-f1f243b453fa" />

State Diagram (High-level)
textIdle → Start → Running (Conveyor ON + Sensor Scan)
          ↓
   Object Detected → Color Classified → Actuator Triggered
          ↓
   Sorting Completed → Continue / Fault Handling

🛠️ Technologies Used

Beckhoff TwinCAT 3 (PLC, Motion, Safety optional)

Made with ❤️ for automation engineering
Alvin Ngo – Industrial Automation & TwinCAT Developer
IEC 61131-3 + TwinCAT OOP & .NET integration
Visual Studio solution for auxiliary color processing
Potential extensions: TwinCAT Vision, MATLAB/Simulink integration, OPC UA

