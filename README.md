# OOAD-WEEK11
#การบ้าน
State Diagram 1 
code
```
@startuml

[*] -up-> one
one -right-> Two
Two --> Three
Three -left-> [*]

@enduml

```
<img src = "http://www.plantuml.com/plantuml/img/SoWkIImgAStDuUAArefLq2qjqBLJoCzBvG9Y1TsYpFIC4g10I7a-5n0hw8BO6KMfgLnWKa4t9pKD90_KoiNba9gN0ZG80000">

State Diagram 2 
code
```
@startuml

[*] --> Lamp

state "Lamp" as Lamp {
  state "Switch" as Neon
  state "Neon_on_close" as onclose
  onclose : power on
  onclose : power off
  Neon : Open
  Neon : close
  [*] --> Neon
 Neon --> onclose : Open
onclose --> Neon : Close
}

@enduml

```
<img src ="http://www.plantuml.com/plantuml/img/SoWkIImgAStDuUAArefLqDMrK_19p2tWuWAAbwGgA84uIWg9nM1HXMek1GMeH71vPabo1bZABpK_3o41uiK3KN9EVd4gM3u_3ym6Ae6o5AmK2lBBKuiKmFem1DFIWA8WOu12_WMfUGWUp1oOKo4sWoL1N8H9O6qmBambKDmPR40j5n0ufEQb0FqD0000">

State Diagram 3
code
```
@startuml
title Turn on-off
state "off" as b
state "On" as a

[*] --> b
b: Shut_down
b -right-> a
a : computer_on
state "Boot" as c
a -up-> c
c:Boot_Window
state "Ready" as d
c -left-> d
d:waiting_System
d -down-> [*]

@enduml

```
<img src = "http://www.plantuml.com/plantuml/img/DO_12eCm38RlUOhWST0Nw678Nc0m1pkCKMfRjQ2fj2dYsoyAvfJy_yUVf2riCzTb1euy1tpNJ9X8fM40iJXW8ss3jc1_2KywPmlmlVrGgRjOlSPkgcnysWXwL3cE4ujZmQ96bvQrSiWcqHNoI8dF62U4ggkm3fm-PFE993aN-GhMxoVgmQ6Qmt04U_1wiv4ZZQRR2uS5FAfZlPXo5qYrWRoyzWS0">

State Diagram 4
code
```
@startuml
scale 1.5
title Decode
state "Ready" as a
state "Decoding" as b

[*] --> a
a:do/waiting for instruction
a -right-> b 
b:do/decoding instruction
b -right-> b :Deocoding_not_complete
b--> a : Decodeing_complete


@enduml

```
<img src = "http://www.plantuml.com/plantuml/img/LO_12i8m38RlUOgmep35WvSTP8SzWLUHaRPn5hP6sWpnxUtg5Bs5__j8yhT9AUeyZP0iZOpxxG7KQvuwjk8OCbV6wiJadXLIGlf4HV1XAAa1E6ykMDV7B53ZPFSWhvdYLIBwa3JELhq48AoZ7swQJODW5jMjc_uyy-ir7SlRwODeRsMwZwmCfXp4PlrsuLy6q79mkTeB">

State Diagram 5
code
```
@startuml
scale 1.5
title Login
state "Login" as a
state "Control" as b
state "Process Text" as c
state "database" as d
state "control_device" as e

[*] --> a
a -r-> b : login complete
b -r-> c : process
c -d-> d : sent text
d -l-> e :sent command
e -l-> [*] : END


@enduml
```
<img src = "http://www.plantuml.com/plantuml/img/DP2n2W8n38RtF4MuKQZWu7A37AYRY8ERYEJQ80UzzcYZ-FZcMhebtqVoXmnPACbdzf0jUSRTTWyoYLQN-9u2g1R6hZGTKaPgw1Y3fEWB71kyfMWvPxppJugnpJWI6YbpeQvHMvUy77ydMnq3F3PFDEQWMOGcQJ5YZtuz0MsS5y_2C5PZrImr52mQfyWfoXm4HOy0XyOhPEmBq_cPWWEkU4tgyNmz0S30mUaZ_W00">

Activity Diagram 1
code
```
@startuml
(*) --> "Door"

if "Pass" then
  -->[true] "door open"
  -right-> (*)
else
  ->[false] "Back to door"
  -->[Ending ] (*)
endif

@enduml
```
<img src = "http://www.plantuml.com/plantuml/img/9Own3eCm34HtVyN94wt4Bo24shqxOeWQ1wBIf4hC_-EKoVRvxkd6ggxeyTsfkz_GzmFuaNDXeXZ0BrShGpT9XFQSjHooWBrPa7-IkEabhfjQqWWaUvMc3NDmjfftSkyFDCF_iHVccNnCAvOhOaSW6crQZnC0">

Activity Diagram 2
code
```
@startuml

title Activity Diagram 
start -r-> "calculate"
 if   time then
 -r->[hour<=40]"Normal" 
else 
    -d->[hour>40] "Overtime"


@enduml
```
<img src = "http://www.plantuml.com/plantuml/img/BSun2i9044RXVaxni_s2XQM62DPw0B4Oaj4Cp2OmcGruUzTW_pru_HhiKOiHXOO9BaFefl71LVdjN42xGFRS8GriGpKEIGHz0GWjWfXafbqyfgNwwNmyFDDjySAMG6AhW9f57l-YQm3fled_-aH4lSnZk_W2">


Activity Diagram 3
code
```
@startuml

title Score 
start --> "Score"
if score> 50 then 
  -r->[Pass] "Good"
  else 
    -->[Fail] "Bad"

@enduml
```
<img src = "http://www.plantuml.com/plantuml/img/7Oqn2e0m40JxUyMIFc1Z6uA5jeAbM0GzCH0DvCx_czWjCmphHKFHzqv46ZKnbZqN1lqOrZgOdnYA9wGjXxw3Nlo005kiM-SWii5CEH-cCax2pQ7bwnXYgd88rP7dvwXV7m00">

Activity Diagram 4
code
```
@startuml

(*) --> if "Grade" then


  
  if "" then
    -> [Score>60]"Grade C" as a3
  else
    if "" then
      -right->[Score>70] "Grade B"
    else
       if "" then
      -right->[Score>80] "Grade A"
      else
       -down->[Score<50] "Grade F"
    endif
  endif
 endif
else

  ->[Score>50] "Grade D"
  
endif


@enduml
```
<img src = "http://www.plantuml.com/plantuml/img/SoWkIImgAStDuUBIqD9KqDMrKyXCKr1oBqfCILLIACb8pUFYub9G02AGC5H40GY02gE3a_EBKktC368XwXMSbHGIYnKIZO4AKdEAKy7gqBG1DHPbfcUKwDf1TPiRn4AjKt1I0Yk1QoL2jmL2jwCIL0coVjsK_F8yc6eRKuHgDwXTUIcPQLnm6aA13U02UH5g2v8-5v0-BeWwBYu780COTW00">

Activity Diagram 5
code
```
@startuml

(*)--> "Login"
--> ===B1=== 
--> "ID Student"
--> ===B2===

===B1=== --> "Password"
--> ===B2===
--> "WEBSITE"
--> (*)

@enduml
```
<img src = "http://www.plantuml.com/plantuml/img/SoWkIImgAStDuUBIqDBKrRLJKFB9Jy_CK-82iMrjRPqCWOG2cAVawQ8GN5AQaffNWf0s0X9SN725O7K1YSN5vVb5AMYgm7BXhax1dY6k42cWbLnS3gbvAK070000">
