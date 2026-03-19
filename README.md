# Finalflash
Windows PowerShell setup script for quickly applying post-build system tweaks, performance settings, and optional debloat actions on a fresh PC.

# Windows Post-Build Setup Script

A PowerShell-based post-build setup script for freshly installed Windows systems.

This project automates a small set of useful Windows configuration changes after building or setting up a PC.  
It is designed to be simple, interactive, and easy to extend without requiring a graphical user interface.

The script currently focuses on a few performance-related and quality-of-life settings, optional prompts for selected features, and the ability to launch an external debloater at the end.

---

## Overview

After a fresh Windows installation, many users manually change the same settings over and over again.  
This script helps reduce that repetitive work by applying predefined system changes through PowerShell.

The current implementation includes:

- Enabling **Hardware-Accelerated GPU Scheduling**
- Disabling **Variable Refresh Rate**
- Disabling **Game Mode**
- Setting **Balanced Power Mode** if an **X3D CPU** is installed
- Disabling **mouse acceleration**
- Disabling **optional diagnostic data**
- Restricting **Delivery Optimization**
- Optional prompt to enable **System Protection**
- Optional prompt to enable **Clipboard History**
- Optional prompt to open **Do Not Disturb / Notifications settings**
- Optional prompt to launch the **Raphire Debloater**

The script is intentionally interactive for selected settings so the user can decide case by case during execution.

---

## Goals

This project aims to provide:

- A quick post-build configuration workflow
- A lightweight PowerShell-based solution without a GUI
- A simple foundation that can be expanded over time
- A more user-friendly setup experience through prompts and automatic elevation

---

## Features

### Automatic elevation
The script automatically checks whether it is running with administrator privileges.  
If not, it relaunches itself as Administrator.

### Interactive prompts
Some settings are not forced automatically and instead ask the user for confirmation, for example:

- X3D CPU power plan handling
- System Protection
- Clipboard History
- Do Not Disturb configuration
- Debloater launch

### Small simulated wait times
A small random delay between steps makes execution feel less abrupt and improves readability while the script runs.

### Clean terminal output
The script prints structured status messages to show what is happening during execution.

---

## Included settings

### Applied automatically

These settings are applied without additional confirmation:

- Hardware-Accelerated GPU Scheduling = **On**
- Variable Refresh Rate = **Off**
- Game Mode = **Off**
- Mouse acceleration = **Off**
- Optional diagnostic data = **Reduced / Required only**
- Delivery Optimization = **HTTP only / peer-to-peer disabled**

### Applied conditionally

These settings depend on user input:

- Power plan = **Balanced** if the user confirms an X3D CPU is installed
- System Protection = optional
- Clipboard History = optional
- Do Not Disturb = optional manual configuration prompt
- Debloater launch = optional

---

## Project structure
