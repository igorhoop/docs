# Снятие логов

Роботы Deep создают 3 типа логов во время работы.  

Журнал событий: здесь записывается каждое событие во время работы. Файл с расширением .log ххранится по адресу /home/ysc/jy_exe/log.  

Журнал операций: после нажатия кнопки [Сохранить данные] в приложении, данные о движении, записанные на частоте 200гц(каждые 0,005 секунд) за последние 5 минут. Каждый файл можно посмотреть в Microsoft Excel. Расширение файла - .csv и он объединен в один файл с журналом ошибок. Точный путь указан в конце журнала событий.  

Журнал ошибок: После нажатия кнопки [Сохранить данные] в приложении, в журнал ошибок записываются данные за последние 5 минут. Расширение файла - .snapshot.csv и он объединен в один файл с журналом операций.Точный путь указан в конце журнала событий.  

[Внимание] Журнал событий сохраняется в течение 7 дней, просроченные файлы будут удаляться каждый раз, когда
при запуске будет недостаточно места на жестком диске.  
[Внимание] Пожалуйста, убедитесь, что робот лежит, когда вы нажимаете кнопку [Сохранить данные].  

Вот пример содержимого журнала событий:  
```
new slave mask is 0xfff
sig = 36
Deep Robot Control System is going to work!.
Deepros Version: 0.2.17(35)
Deeprcs Version: 1.3.0(67)
DeepRAS Version 3.2.2(123)
CPU clock accuracy = 2e+06
[Info] Target robot is JY-M1-022
	Master version 1.6.48203.0

 AdapterList count = 2 
enp1s0 
lo 
At begining, ecat state = 8

master config file path = ../robot_common/MIP_config/master.xml
[Using Adapter: enp2s0] ... 

profied cycle time  = 250
new slave mask is 0xfff
slave 0 is motor 8 
slave 1 is motor 7 
slave 2 is motor 6 
slave 3 is motor 3 
slave 4 is motor 4 
slave 5 is motor 5 
slave 6 is motor 9 
slave 7 is motor 10 
slave 8 is motor 11 
slave 9 is motor 2 
slave 10 is motor 1 
slave 11 is motor 0 
 Master initialization routine complete.
 Master ready to work.

is_support gpio:  0
[Success] Enter Torque mode. 
Hello, Ethernet Listener.
Hello, Heartbeat Listener.
Hello, GridmapListener Listener.
Hello, IMU-Y sensor! 
Hello, ethernet speaker! 
Hello, Controller for MPC.
Hello, heat sensor3! 
Hello, Recorder.
Bye, Recorder.
Ethernet listener is listening...
Ethernet listener is listening...
ready to run heat sensor3!
Algorithm is start

******** Motion Config Setting ********
Forward Vel Offset: 0
Side Vel Offset: 0
Robot Stand Height: 0.38
******** Motion Config Setting ********

-------max_cycle = 0.00173996, count = 0
-------max_cycle = 0.00104181, count = 1
-------max_cycle = 0.00107271, count = 2
-------max_cycle = 0.00110401, count = 3
-------max_cycle = 0.00102618, count = 4
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 0.09 min [Motor Temperature]  FL:31.79, FR:32.04, HL:31.27, HR:32.57, Max [11]: 32.57, Min [01]: 22.65
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 0.22 min [Motor Temperature]  FL:31.27, FR:33.36, HL:29.73, HR:33.10, Max [05]: 33.36, Min [01]: 23.64
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 0.36 min [Motor Temperature]  FL:31.02, FR:32.04, HL:30.25, HR:32.04, Max [05]: 32.04, Min [01]: 22.90
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 0.49 min [Motor Temperature]  FL:30.25, FR:33.87, HL:30.76, HR:33.36, Max [05]: 33.87, Min [01]: 23.39
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 0.63 min [Motor Temperature]  FL:30.25, FR:32.57, HL:30.50, HR:34.39, Max [11]: 34.39, Min [01]: 23.64
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 0.77 min [Motor Temperature]  FL:32.04, FR:32.04, HL:30.76, HR:34.39, Max [11]: 34.39, Min [01]: 23.14
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 0.90 min [Motor Temperature]  FL:31.27, FR:33.61, HL:29.47, HR:34.13, Max [11]: 34.13, Min [01]: 23.14
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 1.04 min [Motor Temperature]  FL:31.53, FR:32.57, HL:28.95, HR:33.36, Max [11]: 33.36, Min [01]: 22.65
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 1.17 min [Motor Temperature]  FL:30.76, FR:32.84, HL:30.50, HR:33.10, Max [11]: 33.10, Min [01]: 22.15
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 1.31 min [Motor Temperature]  FL:31.27, FR:33.36, HL:31.02, HR:32.31, Max [05]: 33.36, Min [01]: 23.89
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
[Working State Judge] soft stop button: 1, driver enable: 1, wifi connect: 0, joystick connect: 0
gyro connect: 1, gyro nonzero: 1, heat data connect: 1app connect: 0, motor heat normal: 1, driver heat normal: 1, is_battery_level_normal:1
Time: 1.45 min [Motor Temperature]  FL:29.99, FR:33.61, HL:28.44, HR:32.31, Max [05]: 33.61, Min [01]: 24.15
stand up button is press!
Standing up, please wait...
Stand up action has finished, waitting to switch to force control mode!
Switching to force control mode, please wait...
Switch to force control has finished, waitting to start or stand down!
Time: 1.58 min [Motor Temperature]  FL:31.53, FR:33.87, HL:31.02, HR:35.17, Max [11]: 35.17, Min [01]: 22.90
ButtonY is pressed...
JY is Moving... (TVMPC)
Time: 1.72 min [Motor Temperature]  FL:31.27, FR:34.65, HL:33.10, HR:34.91, Max [11]: 34.91, Min [01]: 24.15
ButtonLB is pressed...
ButtonLB is pressed...
Time: 1.85 min [Motor Temperature]  FL:32.57, FR:38.07, HL:32.31, HR:37.80, Max [05]: 38.07, Min [01]: 23.89
[Target Gait:] 3
Switch to Vision Mode!!!
[Jump Type]:  Forward Jump!
[Jump Type]:  Further Forward Jump!
Switch to Joystick Mode!!!
Time: 1.99 min [Motor Temperature]  FL:35.69, FR:40.73, HL:35.43, HR:40.47, Max [05]: 40.73, Min [01]: 22.90
ButtonY is pressed...
Switching to force control mode, please wait...
ButtonY is pressed...
ButtonY is pressed...
Switch to force control has finished, waitting to start or stand down!
ButtonY is pressed...
JY is Moving... (TVMPC)
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Time: 2.13 min [Motor Temperature]  FL:38.34, FR:42.35, HL:37.28, HR:41.00, Max [05]: 42.35, Min [01]: 24.40
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
Time: 2.26 min [Motor Temperature]  FL:39.67, FR:46.42, HL:37.28, HR:42.08, Max [05]: 46.42, Min [01]: 23.89
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
Time: 2.40 min [Motor Temperature]  FL:40.47, FR:48.34, HL:39.14, HR:44.25, Max [05]: 48.34, Min [01]: 22.90
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
Time: 2.53 min [Motor Temperature]  FL:41.54, FR:49.17, HL:42.62, HR:46.42, Max [05]: 49.17, Min [01]: 23.89
Time: 2.67 min [Motor Temperature]  FL:43.71, FR:51.39, HL:42.35, HR:46.42, Max [05]: 51.39, Min [01]: 24.15
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
Switch to Joystick Mode!!!
[Target Gait:] 4
Time: 2.81 min [Motor Temperature]  FL:45.86, FR:52.79, HL:43.16, HR:49.17, Max [05]: 52.79, Min [01]: 23.89
Switch to Vision Mode!!!
[Target Gait:] 3
Switch to Vision Mode!!!
ButtonY is pressed...
Switching to force control mode, please wait...
Time: 2.94 min [Motor Temperature]  FL:45.33, FR:52.51, HL:44.25, HR:50.28, Max [05]: 52.51, Min [01]: 24.91
Switch to force control has finished, waitting to start or stand down!
Time: 3.08 min [Motor Temperature]  FL:45.33, FR:55.33, HL:43.16, HR:49.72, Max [05]: 55.33, Min [01]: 24.66
Time: 3.21 min [Motor Temperature]  FL:47.24, FR:53.35, HL:43.16, HR:48.90, Max [05]: 53.35, Min [01]: 23.39
ButtonY is pressed...
JY is Moving... (TVMPC)
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
[Target Gait:] 4
Time: 3.35 min [Motor Temperature]  FL:47.79, FR:52.79, HL:43.16, HR:48.34, Max [05]: 52.79, Min [01]: 23.89
[Target Gait:] 3
[Target Gait:] 4
[Target Gait:] 3
ButtonY is pressed...
Switching to force control mode, please wait...
Time: 3.49 min [Motor Temperature]  FL:48.90, FR:54.76, HL:44.25, HR:48.06, Max [05]: 54.76, Min [01]: 24.15
Switch to force control has finished, waitting to start or stand down!
ButtonY is pressed...
JY is Moving... (TVMPC)
Time: 3.62 min [Motor Temperature]  FL:49.17, FR:56.46, HL:43.16, HR:50.00, Max [05]: 56.46, Min [01]: 23.89
Switch to Joystick Mode!!!
Switch to Vision Mode!!!
Time: 3.76 min [Motor Temperature]  FL:50.56, FR:56.17, HL:45.06, HR:50.84, Max [05]: 56.17, Min [10]: 25.67
Switch to Joystick Mode!!!
Time: 3.89 min [Motor Temperature]  FL:48.34, FR:57.32, HL:45.86, HR:51.67, Max [05]: 57.32, Min [01]: 24.40
get soft emergency signal...
[Soft Emergency Pressed!!!]
Switching to force control mode, please wait...
[Warning] Robot is lose control, Switch to position control mode, wait a moment to press [STAND UP BUTTON] to let robot lose power!!!
Time: 4.03 min [Motor Temperature]  FL:49.17, FR:57.61, HL:45.86, HR:53.91, Max [05]: 57.61, Min [01]: 25.42
stand up button is press!
Robot is lose power, wait a moment to press [STAND UP BUTTON] to recover the posture!!!
stand up button is press!
Time: 4.17 min [Motor Temperature]  FL:49.45, FR:57.32, HL:46.69, HR:52.51, Max [05]: 57.32, Min [01]: 25.17
stand up button is press!
get soft emergency signal...
[Soft Emergency Pressed!!!]
ButtonY is pressed...
Time: 4.30 min [Motor Temperature]  FL:47.79, FR:53.63, HL:44.79, HR:49.45, Max [05]: 53.63, Min [01]: 24.40
Time: 4.44 min [Motor Temperature]  FL:48.06, FR:52.51, HL:43.43, HR:50.00, Max [05]: 52.51, Min [01]: 24.40
Time: 4.57 min [Motor Temperature]  FL:47.24, FR:51.95, HL:42.62, HR:47.52, Max [05]: 51.95, Min [01]: 24.66
stand up button is press!
Robot is recovering posture...
Robot is waitting to stand up!!!
stand up button is press!
Standing up, please wait...
stand up button is press!
Stand up action has finished, waitting to switch to force control mode!
Switching to force control mode, please wait...
Switch to force control has finished, waitting to start or stand down!
ButtonY is pressed...
JY is Moving... (TVMPC)
Time: 4.71 min [Motor Temperature]  FL:46.42, FR:50.84, HL:42.08, HR:45.60, Max [05]: 50.84, Min [01]: 23.39
stand up button is press!
ButtonY is pressed...
Switching to force control mode, please wait...
stand up button is press!
stand up button is press!
Time: 4.85 min [Motor Temperature]  FL:47.24, FR:52.23, HL:44.25, HR:46.97, Max [05]: 52.23, Min [01]: 24.40
Switch to force control has finished, waitting to start or stand down!
stand up button is press!
Standing down, please wait...
Stand down action has finished, waitting to stand up again!!!
Tips: press "x" to exit without saving data!!!
      press "s" to exit with saving data!!!
Time: 4.98 min [Motor Temperature]  FL:47.24, FR:53.08, HL:45.06, HR:47.52, Max [05]: 53.08, Min [01]: 25.92
get soft emergency signal...
[Soft Emergency Pressed!!!]
Exit and save!!!
Bye, Controller.
Bye,IMU sensor.
Bye,ethernet speaker.
ScopeNamesMap (Size:140)
No.0: control_state_record
No.1: goal_robot_state.forward_vel
No.2: goal_robot_state.side_vel
No.3: goal_robot_state.body_height
No.4: goal_robot_state.body_vel
No.5: goal_robot_state.roll_posture
No.6: goal_robot_state.roll_vel
No.7: goal_robot_state.pitch_posture
No.8: goal_robot_state.pitch_vel
No.9: goal_robot_state.yaw_posture
No.10: goal_robot_state.yaw_vel
No.11: actual_robot_state.forward_vel
No.12: actual_robot_state.side_vel
No.13: actual_robot_state.body_height
No.14: actual_robot_state.body_vel
No.15: actual_robot_state.roll_posture
No.16: actual_robot_state.roll_vel
No.17: actual_robot_state.pitch_posture
No.18: actual_robot_state.pitch_vel
No.19: actual_robot_state.yaw_posture
No.20: actual_robot_state.yaw_vel
No.21: actual_robot_state.is_robot_lose_control
No.22: basic motion global_.state
No.105: slam_vel_x
No.106: slam_vel_y
No.107: yaw_vel

Recorder: I'm ready!
../data/JY-M1-022 2023-04-13 19-50.snapshot.csv
window = 1600
Bye, Ethernet Listener.
Secretary Log: The Log file is created!
Recorder: I'm ready!
../data/JY-M1-022 2023-04-13 19-50.csv
Secretary Log: The Log file is created!
[Info] All logs have been generated.
start to tar: tar -czvPf "../data/JY-M1-022 2023-04-13 19-50".tar.gz "../data/JY-M1-022 2023-04-13 19-50"*
../data/JY-M1-022 2023-04-13 19-50.csv
../data/JY-M1-022 2023-04-13 19-50.snapshot.csv
removed '../data/JY-M1-022 2023-04-13 19-50.csv'
removed '../data/JY-M1-022 2023-04-13 19-50.snapshot.csv'
all registered threads is over
Bye,heat sensor3.
Deep Robot Control System is over.
```
В конце журнала событий мы видим адрес, куда были сохранены, журнал операций и журнал ошибок(если ошибок нет, то файлы идентичны)  

![Пульт управления](/assets/images/deepLogs.png){: width="1000px"}
 

