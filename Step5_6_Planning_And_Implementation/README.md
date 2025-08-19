# Planning and Implementation of solution

## Sequence of tasks to be performed by the system

1. On the arrival of train, the sensor placed at a calculated distance detects the approach of the train and sets IS_TRAIN_APPROACHING to True.

2. Once IS_TRAIN_APPROACHING = True, send a control signal to the warning lights and bells to be turned on and send the control signal to the gates to be lowered i.e GATE_LOWER= True.

3. When the GATE_LOWER signal is true and at the same time a vehicle is stuck between the road that is IS_VEHICLE_PRESENT = true, then send an alert signal to the train to either stop or slow down the train.

4. Once the sensor detects that the train has passed through the intersection, that is , IS_TRAIN_APPROACHING= False, the control signals to the gates are sent to raise the gates (GATE_LOWER = False) and the warning lights and bells are also sent a signal to be turned off.

## Flowchart of the system

![Level crossing control system](<Level crossing system.drawio (1).png>)

## Word Coding

```
    START
    IF TRAIN IS APPROACHING THEN:
        IS_TRAIN_APPROACHING = TRUE
        WARNING_LIGHTS = ON
        WARNING_BELL = ON
        GATE_LOWER = TRUE
    ELSE :
        WARNING_LIGHTS = OFF
        WARNING_BELL = OFF
        GATE_LOWER = FALSE
        MONITOR IF THE TRAIN IS APPROACHING

    IF GATE_LOWERED = TRUE AND IS_VEHICLE_PRESENT= TRUE:
        ALERT_SIGNAL = ON
    ELSE:
        ALERT_SIGNAL = OFF

    MONITOR IF THE TRAIN IS APPROACHING
    END
```
