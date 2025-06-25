# 🤖 Line-Following Robot – Flowchart

```text
[Start]
   ↓
[Initialize Sensors and Motors]
   ↓
[Read IR Sensors]
   ↓
[Is Robot Centered on Line?] ──No──→ [Adjust Direction]
          │
         Yes
          ↓
[Move Forward]
   ↓
[Is End of Line Reached?] ──No──→ [Loop Back to Read Sensors]
          │
         Yes
          ↓
[Stop Motors]
   ↓
[End]
```





# 🧠 Pseudocode – Line-Following Robot

```plaintext
BEGIN

  InitializeMotors()
  InitializeIRSensors()

  WHILE true DO
    left ← ReadLeftSensor()
    right ← ReadRightSensor()

    IF left = BLACK AND right = BLACK THEN
      MoveForward()
    
    ELSE IF left = WHITE AND right = BLACK THEN
      TurnRight()
    
    ELSE IF left = BLACK AND right = WHITE THEN
      TurnLeft()
    
    ELSE IF left = WHITE AND right = WHITE THEN
      StopMotors()
      Print("End of line reached.")
      BREAK

    ENDIF
  ENDWHILE

END






![image](https://github.com/user-attachments/assets/b6d21a16-70ee-4670-8d6a-294f04212f4c)
