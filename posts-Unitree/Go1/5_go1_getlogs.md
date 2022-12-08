# Снятие логов

## Логи спортпрограммы

Процесс `Legged_sport` при работе ведет логи в файл `/home/pi/Unitree/autostart/sportMode/log`. Файл перезаписывается при каждом включении. Логи носят отладочную информацию и предназначены для разработчиков. Однако простой пользователь интуитивно может также подчерпнуть полезную информацию.

Вот пример файла логов:
```
UDP Initialized. socketfd: 9   Port: 8008
UDP Initialized. socketfd: 10   Port: 8010
UDP Initialized. socketfd: 11   Port: 8082
UDP Initialized. socketfd: 12   Port: 8018
[Wait] for check
Check passed
GO1 EDU
[Wait] for trigger: SDK or L1 + start
[UDP Connected] client! Client IP:192.168.123.161 port:8091
SDK trigger detected
Be triggered
[UDP Disconnected] client! socketfd:11 Old Client IP:192.168.123.161 port:8091
[UDP Connected] client! Client IP:192.168.123.161 port:8083
[UDP Connected] client! Client IP:192.168.123.161 port:8084
[UDP Disconnected] client! socketfd:11 Old Client IP:192.168.123.161 port:8083
[CONTROL FSM] State changed to LOCOMOTION due to velocity command!
No available obstacle range data !
[CONTROL FSM] State changed to stand due to NO velocity command!
[CONTROL FSM] State changed to LOCOMOTION due to velocity command!
[Trigger CMD]: START
[Trigger CMD]: Double START
[Trigger CMD]: START
[Trigger CMD]: L2 + A
[Trigger CMD]: L2 + A
[Trigger CMD]: L2 + A
[Trigger CMD]: Double START
[Trigger CMD]: START
[Trigger CMD]: L1 + A
## size: 92
switch to move: 0
time: 1.66851e+12           torso_vertical
1  92
## size: 92
switch to move: 1
time: 1.66851e+12           move_hand_1
1  92
#@    203   2193  1990 
#    3314   4382.637207  404.670990 
0 2193
@@@@@@@@@@@@$$$$$$$$$$$$$$$$$@@@
switch to move: 2
time: 1.66851e+12           pre_stance
1  92
## size: 92
Dance is over this time.
[Trigger CMD]: Double START
[Trigger CMD]: START
```

Как минимум в нем можно увидеть комбинации клавиш нажимались, какие скрипты выполнялись.

А вот пример логов при отсутствии связи с одним из моторов:

```
UDP Initialized. socketfd: 9   Port: 8008
UDP Initialized. socketfd: 10   Port: 8010
UDP Initialized. socketfd: 11   Port: 8082
UDP Initialized. socketfd: 12   Port: 8018
[Wait] for check
Check passed
GO1 EDU
[Wait] for trigger: SDK or L1 + start
[UDP Connected] client! Client IP:192.168.123.161 port:8091
SDK trigger detected
Be triggered
[EM_DAMP]: Some joint may get stuck4
[UDP Disconnected] client! socketfd:11 Old Client IP:192.168.123.161 port:8091
[UDP Connected] client! Client IP:192.168.123.161 port:8083
[UDP Connected] client! Client IP:192.168.123.161 port:8084
[UDP Disconnected] client! socketfd:11 Old Client IP:192.168.123.161 port:8083
```
Здесь присутствует строчка `[EM_DAMP]: Some joint may get stuck4` - один из узлов "застрял". Понять какой именно мотор не отвечает с помощью этих логов нельзя, для этого придется воспользоваться отладочным портом - Type-C разъем на спине робособаки.


## Получение данных через диагностический порт
Основная плата управления в реальном времени постоянно отправляет поток отладочных данных, которые используются для диагностики. На спине робота располагаются 2 Type-C порта, необходимо подключиться к тому, что ближе к голове. Устройство (робособака) должно определиться как COM-порт. Любым терминалом (например **putty**) слушаем этот COM-порт.

```
Скорость: 115200
Формат кадра: 8-N-1
```


Пример вывода:

```
вывод вывод
```


