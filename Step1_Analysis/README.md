# Step 1: Analysis of the problem

## Problem Statement:

The level crossing area is always an area with requires the gratest attention to safety measures. When the train arrives on the crossing, it must be ensured that the gates are closed in order to prevent any vehicle from getting in the way of the train. The system is designed with a logic of only raising the gates when the train is not approaching the level crossing else the gates must be kept down. It must also send an alert signal to the train if a vehicle is on the tracks while the train is approaching to provide enough time for the vehicle to clear from the tracks. The system must ensure that the gates are down or closed in the case of any system failure.

## Inputs and Outputs for the System

### Inputs

    1. Signal from the sensors on the railway tracks
    2. Signal from the sensor on the cross-way road

### Outputs

    1. Gate control signals (Up or down)
    2. Warning lights
    3. Warning sound/bell to the vehicles
    4. Alert signals to the train.

The system takes in a set of input values to produce the gate control signals and the warning signals like lights and bells. The sensors when detect the train approaching sends the signal to the system that the train is approaching by setting value for IS_TRAIN_APPROACHING to be true. When the value true is sent to the system, the system responds with signals to lower gates and turn on the warning lights and warning bell by setting GATE_POSITION down and WARNING_LIGHTS = ON and WARNING_BELL = ON.
In the case where a vehicle is present in the intersection after the sensor has sent the train approaching signal, an alert is sent to the trains to either stop or slow down the train.

The inputs and outputs used in the system are as follows:

| Data                               | Type               | Possible Values (Example Values)      |
| ---------------------------------- | ------------------ | ------------------------------------- |
| Signal from the sensors            | Variable (Boolean) | On/ off                               |
| Signal from the sensor on the road | Variable(boolean)  | on/off                                |
| GATE_LOWER                         | Decision           | True/ False                           |
| IS_TRAIN_APPROACHING               | Decision (Boolean) | True/ False                           |
| IS_VEHICLE_PRESENT                 | Decision (Boolean) | True/False                            |
| Gate Contol Signals                | Output             | Up/ Down                              |
| Warning lights                     | Output             | On/ Off (True when on False when off) |
| Alert Signal to train              | Output             | On/Off (True when on, False when off) |

## Context, constraints and stakeholders for the system

### Context of the system

The level crossing gate control system is required inorder to ensure the safety of all the transport mediums making use of the intersection. It is used inorder to manage the intersection between vehicles on the road and train and ensure that it is safe and also does not cause delay to either of the transport mediums. The system must be reliable and must ensure operation regardless of any external conditions.

The system must detect the trains approaching and give alerts to the road traffic inorder to ensure that vehicles pass the intersection before the gates are lowered or vehicles are stopped on time.

### Constraints for the system

There are certain constraints to keep in mind while the system is designed, these can be categorised into:

1. Technical Constraints:
   I. Since the system must be on and working continuously, a reliable power supply must be used in order to ensure that the system always works. Power supply backups also need to be considered.
   II. The accuracy of the sensors must be ensured as the system heavily relies on the use of sensors to coordinate the opening and closing of the gates.
   III. In case of any failures in the system, the system must default to an approach of closed gates ensuring the safety.

2. Economic Constraints:
   I. The cost for using sensors could be high initially.
   II. The system once installed will require regular checks and maintenance.

3. Social Constraints:
   I. Possible long delays could lead to frustrated drivers.
   II. The route may not be accessible to all types of vehicles like bicycles or may not be accessible to pedestrians.

4. Environmental Constraints:
   I. The extreme weather conditions might interfere with the system.
   II. In busy roads, the warning buzzers or bells must be loud enough but should not cause any disturbances.

5. Legal Constraints:
   I. The system must comply with the safety standards set by the government.

### Stakeholders for the system

There are different people involved in the implementation of the system at different levels inorder to ensure the smooth operation of the system.

1. Railway operators: They must monitor the schedule of the trains and must be present to operate the system in the case of any failures.

2. Road users: The people who use the road are also the stakeholders for the system

3. Government: The government must regulate the laws for the system and must ensure that the system abides by the rules.

4. Maintenance staff and engineers: They are responsible for the installation and the maintenance of the system in an effective manner.
