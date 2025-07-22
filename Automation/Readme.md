# Automation Builder

**Author:** nisanray  
**GitHub:** [https://github.com/nisanray](https://github.com/nisanray)  
**Email:** nisanray@gmail.com

A powerful GUI application for creating and running automation sequences with mouse clicks, keyboard inputs, and more. Build complex automation workflows with an intuitive drag-and-drop interface and execute them with precision timing.

## Overview

Automation Builder is a PyQt6-based desktop application that allows you to create, edit, and execute automation sequences. Whether you need to automate repetitive tasks, create testing scenarios, or build complex workflows, this tool provides a user-friendly interface to accomplish your automation goals.

## Features

### Core Automation Actions
- **Key Press**: Send individual key presses (including special keys like F1, Ctrl, Alt, etc.)
- **Type Text**: Input text strings automatically
- **Mouse Click**: Click at specific coordinates with left/right button support
- **Mouse Move**: Move cursor to precise screen positions
- **Pause**: Add delays between actions
- **Key Down/Up**: Hold and release keys for complex key combinations
- **Hotkey**: Execute keyboard shortcuts (Ctrl+C, Alt+Tab, etc.)
- **Image Click**: Click on images found on screen (future feature)

### Advanced Features
- **Sequence Reversal**: Run automation steps in reverse order
- **Loop Control**: Execute sequences multiple times or infinitely
- **Start Delay**: Add initial delay before sequence execution
- **Custom Step Delays**: Configure individual delays after each step
- **Step Notes**: Add descriptive notes to document your automation
- **Live Coordinates**: Real-time mouse coordinate display overlay
- **Workstation Lock**: Automatically lock computer after sequence completion

### File Management
- **Save/Load**: Store automation sequences as JSON files
- **New/Open**: Create new sequences or load existing ones
- **Step Management**: Edit, duplicate, remove, and reorder steps

## Getting Started

### Interface Layout

The application consists of three main areas:

1. **Sequence Editor (Left Panel)**: Displays your automation steps in order
2. **Tools Panel (Right Panel)**: Buttons to add new steps and manage existing ones
3. **Control Panel (Bottom)**: Execution controls and settings

### Basic Workflow

1. **Create Steps**: Use the "Add Step" buttons to build your automation
2. **Configure Settings**: Set delays, loops, and other execution parameters
3. **Test & Refine**: Use the coordinate overlay and step editing features
4. **Save**: Store your sequence for future use
5. **Execute**: Run your automation with the Start button

## Main Interface Components

### Menu Bar
- **File**: New, Open, Save, Save As operations
- **Help**: Access user guide and about information

### Add Step Buttons
- **+ Key Press**: Add keyboard key presses
- **+ Type Text**: Add text input
- **+ Mouse Click**: Add mouse clicks at coordinates
- **+ Mouse Move**: Add cursor movement
- **+ Pause**: Add time delays
- **+ Key Down/Up**: Add key hold/release actions
- **+ Hotkey**: Add keyboard shortcuts
- **+ Image Click**: Add image-based clicking (advanced)

### Step Management
- **Edit Step**: Modify existing step parameters
- **Duplicate Step**: Copy steps with all settings
- **Remove Step**: Delete unwanted steps
- **Move Up/Down**: Reorder sequence steps

### Execution Controls
- **Start Delay**: Countdown before sequence begins (0-3600 seconds)
- **Run in Reverse**: Execute steps in opposite order
- **Loop Times**: Number of repetitions (0 = infinite)
- **Lock after loop**: Auto-lock workstation after completion
- **Start/Stop**: Begin or abort sequence execution

### Utility Features
- **Details**: View complete sequence summary
- **Coords**: Toggle coordinate overlay for precise positioning
- **Save to DB**: Quick save current sequence

## Key Features Explained

### Coordinate Overlay
The coordinate overlay is a movable window that displays real-time mouse coordinates. This is invaluable for:
- Determining exact click positions
- Planning mouse movement paths
- Positioning elements precisely

**Usage:**
- Click "Coords" to show/hide the overlay
- Left-click and drag to move the overlay window
- Right-click to close the overlay

### Step Notes
Every step can include a descriptive note to help document your automation:
- Explain what each step accomplishes
- Add troubleshooting information
- Document expected outcomes

### Loop Control
Configure how your automation repeats:
- **0 loops**: Run once only
- **Finite loops**: Run specific number of times
- **Infinite loops**: Run continuously until stopped

### Reverse Execution
Run your automation sequence backwards:
- Useful for undoing actions
- Testing sequence reliability
- Creating complementary workflows

### Start Delay
Add a countdown before execution begins:
- Switch to target applications
- Position windows appropriately
- Prepare the workspace

## Safety Features

### Emergency Stop
- **Stop Button**: Immediately abort running sequences
- **Threading**: Non-blocking execution won't freeze the interface
- **Abort Flag**: Clean termination of all automation actions

### Workstation Lock
- Automatically lock your computer after automation completes
- Configurable delay before locking
- Cross-platform support (Windows, Linux, macOS)

## File Format

Sequences are saved as JSON files with the following structure:
- Each step contains action type, parameters, delay, and notes
- Human-readable format for easy sharing and version control
- Portable across different installations

## Tips for Effective Use

### Planning Your Automation
1. **Map Out Steps**: Write down the sequence before building
2. **Test Components**: Verify individual steps before running full sequence
3. **Use Notes**: Document each step's purpose and expected behavior
4. **Start Simple**: Begin with basic actions before adding complexity

### Coordinate Positioning
1. **Use Coords Overlay**: Get exact pixel positions for clicks
2. **Account for Scaling**: Consider display scaling on high-DPI monitors
3. **Test Positioning**: Verify coordinates work across different window states

### Timing and Delays
1. **Add Buffer Time**: Include pauses for slow-loading applications
2. **Test Different Speeds**: Verify automation works at various system speeds
3. **Use Step Delays**: Fine-tune timing between individual actions

### Error Prevention
1. **Save Frequently**: Protect your work with regular saves
2. **Backup Sequences**: Keep copies of working automations
3. **Test Thoroughly**: Run sequences multiple times before deployment

## Troubleshooting

### Common Issues
- **PyAutoGUI Missing**: Some features require PyAutoGUI installation
- **Coordinate Accuracy**: Verify screen resolution and scaling settings
- **Timing Issues**: Adjust delays for different system performance
- **Permission Errors**: Ensure application has necessary system permissions

### Best Practices
- Always test automations in safe environments
- Use appropriate delays to account for system lag
- Document your sequences with clear notes
- Keep backup copies of working automations

## Future Enhancements

The application is designed for extensibility and future improvements may include:
- Image recognition and clicking
- Conditional logic and branching
- Variable support and data input
- Network automation capabilities
- Plugin system for custom actions

---

**© 2025 nisanray** - Built with PyQt6 for cross-platform automation