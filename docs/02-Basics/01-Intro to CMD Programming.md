---
sidebar_position: 1
id: cmd-programming-intro
title: Intro to Command Based Programming
---

:::note
You can find the WPILib documentation for this [here](https://docs.wpilib.org/en/stable/docs/software/commandbased/index.html).
:::

## What is Command Based Programming?
Command Based programming is a popular WPILib design pattern. 
It features 2 core abstractions: commands and subsystems.

### [Subsystems](./subsystems)
A subsystem is a collection of robot hardware that operates together at the same time. 
A subsystem encapsulates this hardware so that you only have a single place for hardware-accessing code to be located.

### Commands
A command defines actions and behaviors that take advantage of the methods provided by the subsystems.
Commands have simple states; initialize, execute, and end.
Simple commands can be combined into command groups or complex commands (TODO: link documentation for what a complex command is).

## How Commands Are Run
Commands utilize the CommandScheduler, which is in charge of queuing commands and ensure that no conflicts occur.
The command scheduler runs every 20ms.