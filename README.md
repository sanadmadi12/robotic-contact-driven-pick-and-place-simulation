# Contact-Driven Pick-and-Place Robotic Arm Simulation

**Robotics | Multibody Dynamics | Contact Mechanics | Mechanical Design**

## Overview

This project develops a physics-based simulation of a robotic pick-and-place system in **MATLAB Simscape Multibody**, with mechanical components designed in **SolidWorks**. Unlike a scripted animation or a model that rigidly attaches the object to the gripper, the simulation represents grasping, transportation, and release through physical contact, friction, gravity, and joint actuation.

The system combines a linear rail, articulated revolute joints, and a parallel-jaw gripper to complete a time-sequenced manipulation cycle.

## Project Objective

The goal was to simulate a complete pick-and-place operation while preserving realistic mechanical interactions between the robot and a freely moving object. Key considerations included stable contact during grasping, load transfer during transport, and controlled release without artificial kinematic attachment.

## Engineering Approach

### Mechanical and multibody modeling

- Designed the robotic assembly in SolidWorks, including its linear rail, articulated joints, and parallel-jaw gripper.
- Built the multibody model in Simscape Multibody to represent the robot's motion and mechanical interactions.
- Modeled the object as a free body subject to gravity and contact forces rather than constraining it to the end effector.

### Motion sequencing and manipulation

- Applied input-signal trajectories to coordinate the robot's joints through the pick-and-place cycle.
- Included deliberate dwell intervals for grasping and releasing the object.
- Concluded the sequence with the robot in a defined parked configuration.

### Contact modeling and dynamic analysis

- Used spatial contact forces to model interaction between the gripper, object, and relevant surfaces.
- Tuned contact stiffness, damping, and friction parameters to obtain stable grasping and transport behavior.
- Enabled joint force and torque sensing to investigate reaction loads during motion and payload handling.

## Results

The completed simulation executed a full pick-and-place sequence: the gripper grasped a freely moving object, transported it, and released it using modeled physical interaction alone. The simulation demonstrated stable contact behavior and load transfer during the manipulation cycle, with repeatable task sequencing and a final parked robot configuration.

Joint reaction-force and torque outputs were also available for analyzing the dynamic loads associated with robot motion, grasping, and payload transport.

## Tools and Methods

| Tool or method | Application |
| --- | --- |
| SolidWorks | Mechanical assembly design |
| MATLAB Simscape Multibody | Physics-based multibody simulation |
| Input-signal-based control | Time-sequenced joint actuation |
| Spatial contact and friction modeling | Grasping, transport, and release interactions |
| Joint force and torque sensing | Dynamic load analysis |

## Key Engineering Concepts

Multibody dynamics, robotic manipulation, revolute and prismatic motion, contact mechanics, friction, joint actuation, and force/torque analysis.
