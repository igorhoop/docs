# Программная архитектура

```warning
Рекомендуем проводить разработку из-под операционной системы Linux Ubuntu 20.04. так как разработка из-под MacOS и Windows не 
поддерживается. 
```

## Структура DDS

![Структура DDS H1](/assets/images/sdk3.png){: width="400px" style="display: block; margin: 0 auto"}

  **DDS**(Служба распространения данных) это межпрограммный слой, является спецификацией распределенной связи. Служба принимает модель вещателя/подписчика и вызывает различные **QoS** службы политики качества для гарантии работы в режиме реального времени, эффективности и гибкости распространения данных.\
  Используется так же для взаимодействия службами запущенными на разный компьютерах.
  
![dds](/assets/images/sdk4.png){: width="600px" style="display: block; margin: 0 auto"}


## Программная архитектура робота

```warning
Запуск программ находясь в режиме отладки для робота (L2+R2 на пульте) 
```

На основном компьютере **ПК1** у робота запущенны сервисы, общающиеся через слой DDS.\

 ![H1services](/assets/images/h1services.png){: width="600px" style="display: block; margin: 0 auto"}

1. Basic service(базовая служба) в реальном времени получает данные о работе аккумулятора, приводов и IMU. Именно базовый интерфейс обладает доступом к интерфейсу команд низкого уровня для управления непосредсвенно приводами. С базовым сервисом можно взаимодействовать через DDS и упралвять приводами.\

![H1basicservice](/assets/images/h1basicservice.png){: width="600px" style="display: block; margin: 0 auto"}

2. High-level motion service(Высокоуровневая служба движения) отвечает за высокоуровневое движение, содержит в себе комманды переключения походки робота, управления позой и скоростями подъема ног и рук. Взаимодействие с данным сервисом возможно через RPC или DDS.\

![H1hlmotionservice](/assets/images/h1hlmotionservice.png){: width="600px" style="display: block; margin: 0 auto"}

3. RobotStateClient(Служба состояния) используется для взаимодействия с другими службами в H1, а так же отвечает за состояние контроллера ходьбы. Использует только RPC для взаимодействия.\
4. Internet service содержит настройки беспроводной сети, а также ноды для связи с мобильным приложением по средству **STA**(режим станции) и **AP**(режим активной точки доступа).\
5. Image service отвечает за стримминг изображений и видео, однако на данный момент не используется.
6. Lidar service(лидарная служба) содержит облако точек и трансформы для них, а также данные с IMU датчика. Строит 3D воксельные карты. Взаимодействие с данной службой доступно через DDS.\

### Basic service
 
 Как и говорилось выше, данный сервис позволяет опрашивать аккумулятор, датчики, IMU, а также сами приводы и управлять ими.\
 \
 Разработчик может отправлять инструкции управления используя подписавшись на топик DDS **"rt/lowcmd"**.
 + **Управление моторами.** Всего в роботе H1 есть 19 электроприводов. Для управления используется объявленный интерфейс **MotorCmd_.idl**.\
 
```cpp
   #ifndef __unitree_go__msg__motor_cmd__idl__
#define __unitree_go__msg__motor_cmd__idl__


module unitree_go {

module msg {

module dds_ {


struct MotorCmd_ {
octet mode;  // Motor control mode (Foc mode (working mode) ->0x01, stop mode (standby mode) ->0x00.)
float q;     //Joint target position
float dq;    //Joint target speed
float tau;   //Joint target torque
float kp;    //Joint stiffness coefficient
float kd;    //Joint damping coefficient
unsigned long reserve[3];   //reserved


};


};  // module dds_

};  // module msg

};  // module unitree_go


#endif  // __unitree_go__msg__motor_cmd__idl__   
```

+ **Управление аккумулятором.** Объявленный интерфейс **BmsCmd_.idl** позволяет отправлять комманду на отключение батарей:

```cpp
#ifndef __unitree_go__msg__bms_cmd__idl__
#define __unitree_go__msg__bms_cmd__idl__


module unitree_go {

module msg {

module dds_ {


struct BmsCmd_ {
octet off;         // Turn off battery: (Command: 0xA5)
octet reserve[3];  //reserve


};


};  // module dds_

};  // module msg

};  // module unitree_go


#endif  // __unitree_go__msg__bms_cmd__idl__
```
\
+ **Получение данных о состоянии.** Обеспечивает разработчика возможностью получать данные с моторов, датчиков, аккумуляторе, которые публикуются в топик DDS **"rt/lowState"**.
* информация о двигателях передается в виде последовательности значений, индекс каждого значения соотвествует индексу привода.

```cpp
// generated from rosidl_generator_dds_idl/resource/idl.idl.em
// with input from unitree_go:msg/MotorState.idl
// generated code does not contain a copyright notice

#ifndef __unitree_go__msg__motor_state__idl__
#define __unitree_go__msg__motor_state__idl__


module unitree_go {

module msg {

module dds_ {


struct MotorState_ {
octet mode;     //Motor control mode (Foc mode (working mode) ->0x01, stop mode (standby mode) ->0x00.)
float q;        // Shutdown feedback position information: The default value is the radian value (which can be changed to the angle value according to the actual situation), and it can be displayed according to the actual value (radian value range: -7-+7, displaying 3 decimal places).
float dq;       //Joint feedback speed
float ddq;      //Joint feedback acceleration
float tau_est;  //Joint feedback torque
  
float q_raw;    //It is still used, but not currently used.
float dq_raw;   //It is still used, but not currently used.
float ddq_raw;  //It is still used, but not currently used.
octet temperature;          //Motor temperature information: Type: int8_t. It can be displayed according to actual values (range: -100-150).
unsigned long lost;         //Motor packet loss information: can be displayed according to actual values (range: 0-9999999999).
unsigned long reserve[2];   //Current motor communication frequency+motor error flag bits: (Array: 0- Motor error flag bits (Range: 0-255, can be displayed according to actual values), 1- Current motor communication frequency (Range: 0-800, can be displayed according to actual values)


};


};  // module dds_

};  // module msg

};  // module unitree_go


#endif  // __unitree_go__msg__motor_state__idl_
```
\
* Получение данных с IMU

```cpp
#ifndef __unitree_go__msg__imu_state__idl__
#define __unitree_go__msg__imu_state__idl__


module unitree_go {

module msg {

module dds_ {


struct IMUState_ {
float quaternion[4];    // Кватернионы

float gyroscope[3];     // Угловые скорости по углам эйлера (0->x, 0->y, 0->z)

float accelerometer[3]; // Линейные ускорения (0->x, 0->y, 0->z)

float rpy[3];           // То же самое данные с гироскопа, только в радианах в секунду

octet temperature;      // Температура с IMU.

};


};  // module dds_

};  // module msg

};  // module unitree_go


#endif  // __unitree_go__msg__imu_state__idl__
```
* Получение данных с аккумулятора

```cpp
#ifndef __unitree_go__msg__bms_state__idl__
#define __unitree_go__msg__bms_state__idl__


module unitree_go {

module msg {

module dds_ {


struct BmsState_ {
octet version_high;    //Battery version
octet version_low;     //Battery version

//0: SAFE, (battery not turned on)
//1: WAKE_ UP, (wake up event)
//6: PRECHG, (during battery pre charging)
//7: CHG, (during normal battery charging)
//8: DCHG, (during normal battery discharge)
//9: SELF_ DCHG (during battery self discharge)
//11: ALARM, (battery presence warning)
//12: RESET_ ALARM, (waiting for button reset warning)
//13: AUTO_ RECOVERYOctet status // Battery status information.  
octet soc;             // Battery level information: (Type: uint8_t) (Range 1% -100%)
long current;          // Charging and discharging information: (positive: represents charging, negative represents discharging) can be displayed according to actual values
unsigned short cycle;  // Number of charging cycles
octet bq_ntc[2];       // The temperature of the two NTCs inside the battery (int8_t) (range: -100-150). 0- BAT1; 1- BAT2

octet mcu_ntc[2];      // Battery NTC array: 0- RES, 1- MOS (int8_t) (range: -100-150).

unsigned short cell_vol[15];      // The voltage of 15 batteries inside the battery.


};


};  // module dds_

};  // module msg

};  // module unitree_go


#endif  // __unitree_go__msg__bms_state__idl__
```
\

### Высокоуровневые команды

Данный сервис определяет походку робота и определяет алгоритм его движений. Сервис сам формирует на основе комманд низкого уровня сообщения для соответсвующих топиков DDS и трансформирует запросы на движения в команды для привода. Взаимодействие разработчика с высоким уровнем происходит с помощью формы request/response.
