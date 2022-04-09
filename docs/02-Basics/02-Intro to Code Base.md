---
sidebar_position: 2
id: intro-to-code-base
title: Intro to Code Base
---

## Folder Layout
:::info
This is subject to change based on the year's code. This file might not be up to date.
:::
```bash
src
└── main
    ├── deploy # files that are sent to the robot that are not code
    └── java
        └── frc
            └── robot
                ├── commands # Contains command classes
                ├── constants # Constant information such as speeds and motor ids etc...
                    ├── Constants.java # Interface holding all constants but not set
                    └── ...Constants.java # Files that implement Constants.java and have values set
                ├── controllers # Contains the Custom Controller and Xbox Controller classes.
                ├── gyro # Contains tools needed for the Gyro sensor
                ├── led # Contains tools needed for the robot LEDs
                ├── logging # Contains tools needed for logging
                ├── motors # Contains tools needed for controlling motors and constant templates for tuning.
                ├── output # Contains trajectories
                ├── PathFilesToRun # Contains trajectories
                ├── subsystems # Contains subsystem classes
                ├── tuning # Contains tools used for tuning
                ├── utilities # Contains extra utilities
                ├── vision # Contains tools for interacting with vision NetworkTables
                ├── Main.java # Main file, do not touch
                ├── Robot.java # Tool used for setting up the robot
                ├── RobotConstants.java # Bulk of the code, calls commands
                └── RobotContainer.java # A class used to access the correct constant based on robot used

```

## Main files
These files are located in the root of frc/robot and are used to control the robot.

### Main.java
This file runs and creates a new instance of Robot.java

### Robot.java
This file initializes different aspects of the robot.

:::note
This file is not edited often, the majority of the code is in RobotContainer.java
:::
Robot.java contains the following methods: 
`robotInit()` 
`robotPeriodic()`
`disabledInit()`
`disabledPeriodic()`
`autonomousInit()`
`autonomousPeriodic()`
`teleopInit()`
`teleopPeriodic()`
`testInit()`
`testPeriodic()`
.

Every `init` method is run the first time the robot is started, and every `periodic` method is run every 20ms.

A different method is called based on the mode the robot is in; disabled, autonomous, teleop, test.
However, all `robot` prefixed methods are run every time, regardless of the status of the robot.

