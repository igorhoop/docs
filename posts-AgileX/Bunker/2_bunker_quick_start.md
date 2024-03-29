# Быстрый старт
## Краткое описание 
BUNKER был спроектирован как универсальное гусеничное шасси для различных сценариев применения: от простых ландшафтов до больших и сложных территорий, требующих высокой проходимости. Робот имеет широкий спектр возможностей для разработки, адаптации к различным сферам деятельности, благодаря независимой системе подвески, имеющей способность преодолевать различные подъемы (с углом наклона до 36 градусов), может подниматься по лестнице и также обладает высокой грузоподъемностью (до 100кг). Его можно использовать для разработки задач осмотра и разведки, спасения или подрыва, универсального спецтранспорта и т. д.

![bunker](/assets/images/bun2.png){: width="400px"}
![bunker](/assets/images/bun.png){: width="400px"}

![Размеры Bunker](/assets/images/sizeBun.png){: width="1000px"}

##  Настройка робота 

Для того, чтобы включить робота, необходимо нажать на кнопку включения питания (слева от красной кнопки): 

![Панель Bunker](/assets/images/PanelBun.jpg){: width="1000px"}

По истечении примерно 30 секунд робот готов к работе.

```note
Обязательным пунктом на этапе эксплуатации служит предварительный внешний осмотр робота перед каждым включением на наличие дефектов: повреждение проводки, отсутствие защищающих элементов корпуса, раскрученных винтов и прочих моментов, отличающихся от первоначального вида робота (в случае обнаружения дефектов дальнейшая эксплуатация робота возможна, однако мы не сможем гарантировать дальнейшее обслуживание в рамках гарантийного договора). 

В этом случае требуется обратиться к инженерам в службу поддержки в чате, они смогут оперативно ответить на любые интересующие вопросы.

```

## Инструкции по дистанционному управлению и настройке Пульта ДУ 
На RC-передатчике предварительно настроено отображение клавиш. Не изменяйте произвольно раскладку клавиш, иначе нормальное управление будет недоступно. Рычаг SWC — это переключатель ручного управления для управления выключением света; левый рычаг управляет движением вперед и назад; правый рычаг управляет автомобилем для вращения влево и вправо. Стоит отметить, что мобильное шасси на внутреннем контроле отображается в процентах, поэтому скорость будет постоянной, когда рычаг находится в том же положении. 

### Основное управление
![Основное управление](/assets/images/control.jpg){: width="700px"}
![Пульт ДУ](/assets/images/control1.png){: width="700px"}

    1. Рычаг SWA

    2. Рычаг SWB

    3. Рычаг SWC

    4. Рычаг SWD

    5. Левый стик

    6. Правый стик

    7. Кнопка питания 1

    8. Кнопка питания 2

    9. Крепление для шнурка
    
    10. Крепление для дополнительных устройств 

    11. Экран

    12. VRA – левое колесо

    13. VRB – правое колесо

Рычаг SWC(3) — отвечает за включение/выключением света; левый стик(5) управляет движением вперед и назад; правый стик(6) используется для вращения влево и вправо.

Для того, чтобы включить пульт, необходимо зажать кнопки 7 и 8 до включения пульта. По умолчанию пульт не требует каких-либо настроек, однако в случае некорректной работы пульта, рекомендуется выполнить следующие действия:

### Настройка используемой модели
  1. Разблокируйте контроллер долгим нажатием на значок замка
  ![Настройка пульта ДУ](/assets/images/rcset.png){: width="1000px"}
  2. Откроется меню “Function”	
  3. Выберите “System”
  ![Настройка пульта ДУ](/assets/images/rcset1.png){: width="1000px"}
  4. Нажмите на “Models”
  5. Выберите **“Model 1”** (4.1) и нажмите стрелочку назад (4.2)
  ![Настройка пульта ДУ](/assets/images/rcset2.png){: width="1000px"}
  6. Вернитесь в “Function”	
  7. Выберите “Aux. channels”
  ![Настройка пульта ДУ](/assets/images/rcset3.png){: width="1000px"}
  8. Выберите “Channel 5”  
  ![Настройка пульта ДУ](/assets/images/channel5.jpg){: width="500px"}
  
### Настройка канала получения информации

Далее настройте каналы связи следующим образом: Channel 5 – VRx – Vr A

Пример настройки Channel 5 – VRx – Vr A:

  1. Нажмите на Значок селектора  
  ![Настройка пульта ДУ](/assets/images/rcset5.jpg){: width="300px"}
  2. Выберите VRx 
  3. Нажмите на окно VrA 
  ![Настройка пульта ДУ](/assets/images/rcset6.png){: width="1000px"}
  4. Выберите VrA из установки выше, если значение не было установлено по умолчанию
  ![Настройка пульта ДУ](/assets/images/rcset7.png){: width="1000px"}
  5. Проделайте аналогичные операции с другими каналами связи, значения которых представлены   ниже:  
  **Channel 6 – SWx – SWC	Channel 7 – SWx – SWA**  
  **Channel 8 – SWx – SWB	Channel 9 – SWx – SWD Channel 10 – KEY – KEY1**  
  После этого нажмите на кнопку выхода	и перезагрузите контроллер.
  ![Настройка пульта ДУ](/assets/images/rcset8.png){: width="500px"}
  
### Калибровка контроллера

   1. Разблокируйте стартовый экран
   2. Выберите вкладку “System” и нажмите на “Stick adjust”
   ![Настройка пульта ДУ](/assets/images/rcset9.png){: width="1000px"}
   3. Далее необходимо левым и правым стиком выполнить следующие действия (последовательность неважна):  
   **Левый стик вверх (до упора)  Правый стик вверх (до упора) Левый стик вниз (до     упора)**   
   **Правый стик вниз (до упора)  Левый стик влево (до упора)Правый стик влево (до упора)**  
   **Левый стик вправо (до упора)  Правый стик вправо (до упора)**  
   **Также следует прокрутить VRA и VRB влево и вправо до упора**  
Результатом успешной калибровки служит заполненная индикация значений MR1, MR2, MR3, MR4, VRA, VRB (допустимы небольшие отклонения, как показано на рисунке):
   ![Настройка пульта ДУ](/assets/images/rcset10.png){: width="1000px"}
   После этого нажмите на кнопку выхода и перезагрузите контроллер
   ![Настройка пульта ДУ](/assets/images/rcset8.png){: width="500px"}
   
##  Интерфейсы

Интерфейс на задней панели показан на рисунке ниже, где:                                                                                                   
Q1 - авиационный интерфейс CAN и источника питания 48 В;                                                                                                    
Q2 - выключатель питания;                                                                                                   
Q3 - интерфейс подзарядки;                                                                                                    
Q4 - антенна;                                                                                                    
Q5 - интерфейс тестирования привода;                                                                                                    
Q6 - выключатель аварийной остановки;                                                                                                    
Q7 - это отображение напряжение батареи.                                                                                                   

![Интерфейсы](/assets/images/interfaceBun.png){: width="1000px"} 
   
## Зарядка 
Убедитесь, что робот Bunker выключен. 
Вставьте вилку зарядного устройства в зарядный интерфейс Q3 на задней панели робота. 
Батарея, поставляемая с BUNKER, заряжена не полностью. Пожалуйста, заряжайте аккумулятор вовремя, когда уровень напряжения на задней панели становится ниже 48 В.
Условия хранения: температура для хранения аккумулятора составляет от -20 ℃ до 60 ℃; 
В случае неиспользования аккумуляторной батареи необходимо заряжать и разряжать примерно раз в 1 месяц и затем хранить в состоянии полного заряда. Пожалуйста, не храните аккумулятор в высокотемпературной среде;
Зарядка: аккумулятор необходимо заряжать специальным зарядным устройством, идущим в комплекте; литий-ионные аккумуляторы нельзя заряжать при температуре ниже 0 ° C, категорически запрещено модифицировать или заменять оригинальные батареи.
    
   ![Панель Bunker](/assets/images/PanelBun.jpg){: width="1000px"}
Индикатором полного заряда служит датчик на блоке питания, который изменит свой цвет с красного на зеленый
   ![Блок питания](/assets/images/charging1.png){: width="1000px"}
   
## FAQ

Q ： BUNKER запускается правильно, но почему RC-передатчик не может управлять движением кузова автомобиля?  

A ： Сначала проверьте, находится ли источник питания привода в нормальном состоянии, нажат ли выключатель питания привода и опущены ли выключатели аварийной остановки; затем проверьте, выбран ли режим управления с помощью переключателя выбора режима вверху слева на ПДУ (см. инструкцию по настройке пульта ДУ)  

Q: Пульт дистанционного управления BUNKER находится в нормальном состоянии, и информация о состоянии шасси соответствует критериям, но почему нельзя переключить режим управления кузовом и шасси на режим управления с компьютера?  

A: Обычно, если BUNKER управляется с помощью RC-передатчика, это означает, что движение шасси находится под ручным управлением; для переключения на режим управления потребуется использовать специальное ПО, разработанное AgileX Robotics, чтобы взаимодействовать с роботом удаленно.   

Q: Робот начал издавать звуковые сигналы при движении/ ожидании, как это исправить?  

A: Этот звук сигнализирует о низком заряде батареи, необходимо проверить заряд на роботе и подключить его к зарядному устройству, ожидая его полной зарядки. Если возникает другой похожий звук, то это могут быть внутренние ошибки. Вы можете проверить соответствующие коды ошибок через шину CAN или
обратиться к соответствующему техническому специалисту   

Q: Робот включился, но не реагирует на команды пульта ДУ. В чем может быть проблема?   
 
A: Пожалуйста настройте пульт ДУ согласно главе 4; убедитесь, что все необходимые рычаги выставлены в правильное положение (прим.: если рычаги 2 и 3 выставлены в базовое положение «Вверх» и при этом робот не реагирует на нажатия, попробуйте перевести рычаги в положение «Посередине» после включения пульта (при включении пульт потребует выставить все рычаги в положение «Вверх»))   
 
Q: Робот начал издавать звуковые сигналы при движении/ ожидании, как это исправить?   
 
A: Этот звук сигнализирует о низком заряде батареи, необходимо проверить заряд на роботе и подключить его к зарядному устройству, ожидая его полной зарядки. Если возникает другой похожий звук, то это могут быть внутренние ошибки. Вы можете проверить соответствующие коды ошибок через шину CAN или обратиться к соответствующему техническому специалисту  
 
Q: Сколько робот может перемещаться по времени при полном заряде?  
 
A: По заявленным характеристикам: до 4 часов работы и до 2 часов осуществляется зарядка робота 
 
Q: Может ли робот перемещаться самостоятельно на определенной местности?  

А:  Да, это возможно при наличии навигационного модуля, который поставляется отдельно, а также специалиста, который сможет запрограммировать робота на выполнение автономных действий на заданной местности 
 

