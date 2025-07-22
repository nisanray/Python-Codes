# Automation Builder - Complete User Guide

## Table of Contents
1. [Overview](#overview)
2. [Getting Started](#getting-started)
3. [Interface Tour](#interface-tour)
4. [Creating Your First Automation](#creating-your-first-automation)
5. [Step Types Reference](#step-types-reference)
6. [Advanced Features](#advanced-features)
7. [Best Practices](#best-practices)
8. [Troubleshooting](#troubleshooting)
9. [Keyboard Shortcuts](#keyboard-shortcuts)

## Overview

Automation Builder is a powerful desktop automation tool that allows you to create, edit, and execute sequences of mouse clicks, keyboard inputs, and other actions. Perfect for repetitive tasks, testing, or workflow automation.

### Key Features
- **Visual Step Editor**: Easy-to-use interface for building automation sequences
- **Multiple Action Types**: Support for keyboard, mouse, pause, and hotkey actions
- **Loop Control**: Run sequences multiple times or infinitely
- **Coordinate Display**: Real-time mouse position overlay
- **File Management**: Save and load automation sequences
- **Reverse Execution**: Run sequences backwards
- **Step Management**: Edit, duplicate, reorder, and remove steps

## Getting Started


### First Launch
1. Run the application: `Automation_builder.exe`
2. The main window will open with an empty sequence editor
3. You're ready to start building your first automation!

## Interface Tour

### Main Window Layout

The application is divided into four main areas:

#### 1. Menu Bar (Top)
- **File**: New, Open, Save, Save As
- **Edit**: (Reserved for future features)
- **View**: (Reserved for future features)  
- **Help**: Show Guide, About

#### 2. Sequence Editor (Left Panel)
- Displays your automation sequence as a numbered list
- Each step shows the action type, parameters, and delay
- Click on steps to select them for editing

#### 3. Tools Panel (Right Panel)

**Add Step Section:**
- **+ Key Press**: Capture and simulate single key presses
- **+ Type Text**: Type text strings
- **+ Mouse Click**: Click at specific coordinates
- **+ Mouse Move**: Move mouse to coordinates
- **+ Pause**: Add delays in your sequence
- **+ Key Down**: Press and hold a key
- **+ Key Up**: Release a held key
- **+ Image Click**: Click on image patterns (basic implementation)
- **+ Hotkey**: Execute key combinations (Ctrl+C, Alt+Tab, etc.)

**Step Management Section:**
- **Edit Step**: Modify selected step parameters
- **Duplicate Step**: Create a copy of the selected step
- **Remove Step**: Delete the selected step
- **Move Up/Down**: Reorder steps in the sequence

#### 4. Control Panel (Bottom)
- **Start Delay**: Countdown before sequence begins
- **Run in Reverse**: Execute steps in reverse order
- **Loop Times**: Number of repetitions (0 = infinite)
- **Lock after loop**: Lock workstation after completion
- **Start/Stop**: Execute or halt the sequence
- **Save to DB**: Save current sequence to file
- **Details**: View complete sequence information
- **Coords**: Toggle coordinate overlay

## Creating Your First Automation

Let's create a simple automation that opens Notepad and types "Hello World":

### Step 1: Add a Hotkey Step
1. Click **"+ Hotkey"** in the Tools panel
2. Click **"Click then Press Key"** button
3. Press **Win+R** (Windows Run dialog)
4. Add a note: "Open Run dialog"
5. Set delay to 1.0 seconds
6. Click **OK**

### Step 2: Add Type Text Step
1. Click **"+ Type Text"**
2. Enter text: `notepad`
3. Add note: "Type notepad command"
4. Set delay to 0.5 seconds
5. Click **OK**

### Step 3: Add Key Press Step
1. Click **"+ Key Press"**
2. Click **"Click then Press Key"**
3. Press **Enter**
4. Add note: "Press Enter to execute"
5. Set delay to 2.0 seconds (wait for Notepad to open)
6. Click **OK**

### Step 4: Add Another Type Text Step
1. Click **"+ Type Text"**
2. Enter text: `Hello World! This is my first automation.`
3. Add note: "Type welcome message"
4. Set delay to 0.5 seconds
5. Click **OK**

### Step 5: Test Your Automation
1. Click **"Start"** to run the sequence
2. Watch as your automation executes each step
3. Use **"Stop"** if you need to interrupt

### Step 6: Save Your Work
1. Click **"Save to DB"** or use **File > Save As**
2. Choose a filename like `notepad_hello.json`
3. Your sequence is now saved for future use

## Step Types Reference

### Key Press
**Purpose**: Simulate pressing and releasing a single key
**Use Cases**: Enter, Escape, Arrow keys, Function keys
**Parameters**:
- Key: The key to press
- Delay: Wait time after action
- Note: Description of the step

**Example**: Press F5 to refresh a webpage

### Type Text
**Purpose**: Type a string of text
**Use Cases**: Filling forms, entering commands, writing content
**Parameters**:
- Text: The string to type
- Delay: Wait time after typing
- Note: Description of the step

**Example**: Type an email address into a login form

### Mouse Click
**Purpose**: Click at specific screen coordinates
**Use Cases**: Clicking buttons, links, or interface elements
**Parameters**:
- X, Y: Screen coordinates
- Button: left or right mouse button
- Delay: Wait time after click
- Note: Description of the step

**Tip**: Use the Coords overlay to find exact coordinates

### Mouse Move
**Purpose**: Move cursor to specific coordinates without clicking
**Use Cases**: Hover effects, preparing for subsequent actions
**Parameters**:
- X, Y: Target coordinates
- Delay: Wait time after move
- Note: Description of the step

### Pause
**Purpose**: Add a delay in your sequence
**Use Cases**: Waiting for applications to load, creating timing gaps
**Parameters**:
- Seconds: Duration of pause
- Delay: Additional wait time after pause
- Note: Description of the step

### Key Down/Up
**Purpose**: Press and hold (or release) keys for complex key combinations
**Use Cases**: Custom hotkeys, gaming macros, holding modifier keys
**Parameters**:
- Key: The key to press/release
- Delay: Wait time after action
- Note: Description of the step

### Hotkey
**Purpose**: Execute key combinations like Ctrl+C, Alt+Tab
**Use Cases**: Shortcuts, system commands, application switching
**Parameters**:
- Hotkey: Key combination (captured as single input)
- Delay: Wait time after execution
- Note: Description of the step

**Common Examples**:
- Ctrl+C (Copy)
- Ctrl+V (Paste)
- Alt+Tab (Switch applications)
- Ctrl+Shift+Esc (Task Manager)

### Image Click (Beta)
**Purpose**: Click on visual elements by image recognition
**Use Cases**: Clicking buttons that change position, game automation
**Parameters**:
- Path: Image file path
- Delay: Wait time after click
- Note: Description of the step

**Note**: This feature requires additional setup and image files

## Advanced Features

### Coordinate Overlay
1. Click **"Coords"** to open the coordinate overlay
2. A semi-transparent window shows current mouse position
3. Left-click and drag to move the overlay
4. Right-click to close
5. Use these coordinates for precise mouse actions

### Loop Control
- **Loop Times = 0**: Infinite loop (use Stop to halt)
- **Loop Times > 0**: Specific number of repetitions
- **Run in Reverse**: Execute steps backwards
- **Lock after loop**: Automatically lock workstation when complete

### File Management
- **New**: Clear current sequence
- **Open**: Load saved automation files
- **Save**: Update current file
- **Save As**: Create new file with different name

### Step Management
- **Reordering**: Use Move Up/Down or drag-drop (if supported)
- **Editing**: Double-click or use Edit button
- **Duplication**: Copy steps to avoid recreating similar actions
- **Bulk Operations**: Select multiple steps (if supported in future versions)

## Best Practices

### Planning Your Automation
1. **Map out the process**: Write down each step manually first
2. **Identify timing**: Note where delays are needed
3. **Test incrementally**: Build and test small sections
4. **Add descriptive notes**: Document what each step does

### Timing and Delays
- **Start with longer delays**: You can always reduce them later
- **Account for slow applications**: Some programs need extra time to load
- **Network operations**: Add extra delays for web-based actions
- **System resources**: Slower computers may need longer delays

### Error Prevention
- **Save frequently**: Use Ctrl+S or File > Save regularly
- **Test on test data**: Don't run automations on important files initially
- **Have escape plans**: Know how to stop automations quickly
- **Backup sequences**: Keep copies of working automations

### Coordinate-Based Actions
- **Use relative positioning**: When possible, avoid hard-coded coordinates
- **Account for resolution**: Coordinates change with screen resolution
- **Window positioning**: Ensure target windows are consistently placed
- **Multiple monitors**: Be aware of coordinate differences

### Maintenance
- **Review regularly**: Check that automations still work after system updates
- **Update coordinates**: Screen layouts may change over time
- **Version control**: Keep backups of different automation versions
- **Documentation**: Maintain notes about when and why automations were created

## Troubleshooting

### Common Issues

#### Automation Won't Start
- **Check PyAutoGUI**: Ensure the library is installed
- **Permission issues**: Some systems require admin rights
- **Security software**: Antivirus may block automation tools

#### Steps Execute Too Fast
- **Increase delays**: Add more time between steps
- **System load**: High CPU usage can affect timing
- **Application response**: Some programs need more time to process

#### Mouse Clicks Miss Target
- **Verify coordinates**: Use the coordinate overlay to check positions
- **Window positioning**: Ensure target window is in the expected location
- **Resolution changes**: Screen resolution affects coordinate accuracy

#### Keys Not Registering
- **Focus issues**: Target application may not have focus
- **Input method**: Some applications handle input differently
- **Key mapping**: Certain keys may be mapped differently

#### Sequence Stops Unexpectedly
- **Error in step**: Check for invalid parameters
- **Application crashes**: Target application may have closed
- **System interruption**: Other processes may interfere

### Debug Strategies
1. **Run step by step**: Execute one step at a time to isolate issues
2. **Add debugging pauses**: Insert longer delays to observe behavior
3. **Use minimal sequences**: Start with simple 2-3 step sequences
4. **Check system resources**: Ensure adequate CPU and memory
5. **Review logs**: Check console output for error messages

### Getting Help
- **In-app guide**: Help > Show Guide
- **User community**: Check project GitHub for issues and solutions
- **Documentation**: Review this guide and code comments
- **System compatibility**: Verify OS and Python version requirements

## Keyboard Shortcuts

Currently, the application primarily uses mouse interaction. Future versions may include:

- **Ctrl+N**: New sequence
- **Ctrl+O**: Open file
- **Ctrl+S**: Save
- **Ctrl+Shift+S**: Save As
- **Delete**: Remove selected step
- **F1**: Show help
- **Space**: Start/Stop sequence
- **Esc**: Emergency stop

## Tips for Success

### Start Simple
- Begin with basic sequences (3-5 steps)
- Test each step individually before combining
- Use generous delays while learning

### Build Gradually
- Create reusable components
- Combine simple sequences into complex workflows
- Save intermediate versions

### Test Thoroughly
- Run automations multiple times
- Test on different system states
- Verify behavior under various conditions

### Stay Organized
- Use descriptive filenames
- Add detailed step notes
- Group related automations in folders
- Keep a log of what each automation does

---

**Author**: nisanray  
**GitHub**: https://github.com/nisanray  
**Email**: nisanray114@gmail.com  

© 2025 nisanray - Automation Builder