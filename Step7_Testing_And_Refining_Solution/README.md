# Testing and Refining The Solution

## Input values

IS_TRAIN_APPROACHING : Boolean (TRUE / FALSE)

IS_VEHICLE_PRESENT :Boolean (TRUE / FALSE)

## Output values

WARNING_LIGHTS : ON / OFF

WARNING_BELL : ON / OFF

GATE_LOWER : TRUE / FALSE

ALERT_SIGNAL : ON / OFF

## Test cases

1. When the train is not approaching that is, IS_TRAIN_APPROACHING = False and vehicle is not present in the road that is, IS_VEHICLE_PRESENT = False, then in this case,

   Expected output: Warning lights and bell must be off and the gate must not be lowered.

   Actual output: WARNING_LIGHTS = OFF , WARNING_BELL = OFF , GATE_LOWER = FALSE

2. When the train is approaching, that is IS_TRAIN_APPROACHING = True and vehicle is not present that is, IS_VEHICLE_PRESENT = False, then in this case,

   Expected output: Warning lights and bell must be on and the gates must be lowered.

   Actual output: WARNING_LIGHTS = ON, WARNING_BELL = ON , GATE_LOWER = TRUE

3. When the train is not approaching, that is IS_TRAIN_APPROACHING = False and vehicle is present that is, IS_VEHICLE_PRESENT = True, then in this case,

   Expected output: Warning lights and bell must be off and the gates must be raised.

   Actual output: WARNING_LIGHTS = OFF, WARNING_BELL = OFF , GATE_LOWER = FALSE

4. When the train is approaching, that is IS_TRAIN_APPROACHING = True and vehicle is present that is, IS_VEHICLE_PRESENT = True, then in this case,

   Expected output: Alert must be sent to the train to stop or slow the train.

   Actual output: Alert is sent to the train

The table below summarises the expected and actual outputs:
| Case | IS_TRAIN_APPROACHING | IS_VEHICLE_PRESENT | Expected Output | Actual Output |
| ---- | -------------------- | ----------------- | --------------- | ------------- |
| 1 | FALSE | FALSE | WARNING_LIGHTS=OFF, WARNING_BELL=OFF, GATE_LOWER=FALSE, ALERT_SIGNAL=OFF | WARNING_LIGHTS=OFF, WARNING_BELL=OFF, GATE_LOWER=FALSE, ALERT_SIGNAL=OFF |
| 2 | TRUE | FALSE | WARNING_LIGHTS=ON, WARNING_BELL=ON, GATE_LOWER=TRUE, ALERT_SIGNAL=OFF | WARNING_LIGHTS=ON, WARNING_BELL=ON, GATE_LOWER=TRUE, ALERT_SIGNAL=OFF |
| 3 | FALSE | TRUE | WARNING_LIGHTS=OFF, WARNING_BELL=OFF, GATE_LOWER=FALSE, ALERT_SIGNAL=OFF | WARNING_LIGHTS=OFF, WARNING_BELL=OFF, GATE_LOWER=FALSE, ALERT_SIGNAL=OFF |
| 4 | TRUE | TRUE | WARNING_LIGHTS=ON, WARNING_BELL=ON, GATE_LOWER=TRUE, ALERT_SIGNAL=ON | WARNING_LIGHTS=ON, WARNING_BELL=ON, GATE_LOWER=TRUE, ALERT_SIGNAL=ON |

## Possible Refinement in solution:

1. Addition of concepts of train state like Approaching, Train_present, Train_leaving, etc can make the system more reliable through the confirmation of the state of the train.

2. For train not arriving in the scheduled interval, some timeout can be added to accomodate the delay and ensure safety in the intersection.

3. Multiple sensors can be used to confirm the position of the train as well as the vehicles to ensure that the gates are properly down and vehicles are completely out of the intersection when the train approaches.
