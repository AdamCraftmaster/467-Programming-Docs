---
sidebar_position: 3
id: subsystems
title: Subsystems
---

:::note
You can find the WPILib documentation for this [here](https://docs.wpilib.org/en/stable/docs/software/commandbased/subsystems.html).
:::

## What is a subsystem?

A subsystem is a collection of robot hardware that operates together at the same time.
A subsystem encapsulates this hardware so that you only have a single place for hardware-accessing code to be located.

More info about command based programming can be found [here](./cmd-programming-intro)

## How to make a subsystem

Subsystems are located in the subsystems package (folder) of the robot code.
Each subsystem is located in it's own class.
When naming your class, make sure that it's suffix is the year that the robot was made, for example *Indexer*2022**

Every subsystem is unique. The only requirement is that the class `extends SubsystemBase` and has `super();` in it's constructor.

```java title="/src/main/java/frc/robot/subsystems/Indexer2022.java"
public class Indexer2022 extends SubsystemBase {
    public Indexer2022() {
        super();
    }
}
```

## Simple Example

:::caution Note
The example usage of the motors is not (fully) accurate. More information on how to control motors can be found here: TODO add doc
:::

```java title="/src/main/java/frc/robot/subsystems/Indexer2022.java"
public class Indexer2022 extends SubsystemBase {
    public Indexer2022() {
        super();
    }
    
    public void forward() {
        indexerMotor.set(10);
    }
    
    public void backward() {
        indexerMotor.set(-10);
    }
    
    public void stop() {
        indexerMotor.set(0);
    }
}
```