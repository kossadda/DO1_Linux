# Part 1. Установка ОС

**Установить Ubuntu 20.04 Server LTS без графического интерфейса. (Используем программу для виртуализации - VirtualBox)**  

- Устанавка образа ОС в VirtualBox:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/1.jpg" alt="install OS">
</div>

- Проверка номера версии:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/2.jpg" alt="version">
</div>


# Part 2. Создание пользователя

**Создать пользователя, отличного от пользователя, который создавался при установке. Пользователь должен быть добавлен в группу adm**  

- Создание нового пользователя user_two и добавление его в группу adm:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/3.jpg" alt="add user">
</div>

- Вывод команды \ cat /etc/passwd:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/4.jpg" alt="show user">
</div>

# Part 3. Настройка сети ОС 

**1. Задать название машины вида user-1**  
**2. Установить временную зону, соответствующую вашему текущему местоположению**  
**3. Вывести названия сетевых интерфейсов с помощью консольной команды**  

- Определение названия машины вида user-1

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/5.jpg" alt="change user">
</div>

- Установка временной зоны, соответствующей нашему текущему местоположению (выбор производится из списка по команде **timedatectl list-timezones**) и отображение изменений на выводе консоли:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/6.jpg" alt="switch timezone">
</div>

- Установка набора сетевых инструментов:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/7.jpg" alt="tools install">
</div>

- Вывод названия сетевых интерфейсов:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/8.jpg" alt="show net name">
</div>

***Информация:***  
***Интерфейс lo (Loopback Interface)** представляет собой виртуальный сетевой интерфейс в операционных системах, таких как Linux и UNIX-подобные системы. Он используется для локальной коммуникации на самом устройстве и обычно имеет IP-адрес 127.0.0.1, который также обозначается как "localhost".*  

- Получение ip адреса устройства, на котором производится работа, от DHCP сервера.

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/9.jpg" alt="show ip adress">
</div>

***Информация:***  
***DHCP (Dynamic Host Configuration Protocol)** - это сетевой протокол, используемый для автоматической настройки сетевых параметров устройствам в компьютерной сети. Протокол DHCP позволяет устройствам автоматически получать IP-адреса, а также другие сетевые параметры, такие как шлюз по умолчанию (gateway), маску подсети (subnet mask), адреса DNS-серверов и многое другое.*  

- Вывод на экран внешнего ip-адрес шлюза:  

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/10.jpg" alt="show external ip">
</div>

- Вывод на экран внутреннего IP-адрес шлюза, он же ip-адрес по умолчанию (gw):  

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/11.jpg" alt="show internal ip">
</div>

- Установка статичных настроек ip, gw, dns (с использованием публичных DNS серверов, например 1.1.1.1 или 8.8.8.8):  

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/12.jpg" alt="set static settings">
</div>

- Сохранение изменений. Перезагрузка виртуальной машины:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/13.jpg" alt="save changes">
</div>

- Проверка изменений статичных сетевых настроек (ip, gw, dns) на соответстветствие заданным в предыдущем пункте:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/14.jpg" alt="check changes">
</div>

- Пингование удаленных хостов 1.1.1.1 и ya.ru. Убедить в наличии на выводе команды фразы “0% packet loss”:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/15.jpg" alt="ping hosts">
</div>

# Part 4. Обновление ОС 

**Обновить системные пакеты до последней на момент выполнения задания версии**

- После успешного обновления повторно применяем команду и проверяем установлена ли последняя версия:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/16.jpg" alt="check updates">
</div>

# Part 5. Использование команды sudo 

**Разрешить пользователю, созданному в Part 2, выполнять команду sudo**

***Информация:***  
*Команда **sudo (Superuser Do)** в системах **Unix** и **Linux** используется для выполнения команд с правами суперпользователя (root) или другого пользователя, имеющего необходимые разрешения на выполнение определенной команды. Команда sudo позволяет пользователям выполнять административные задачи и другие привилегированные операции, обычно требующие повышенных привилегий, без необходимости входа в систему под учетной записью суперпользователя (root).*  

- Добавление нового пользователя в группу обладающих привелегией **sudo**. Переключение на данного пользователя. Изменение hostname ОС от имени пользователя, созданного в пункте Part 2 (используя sudo):

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/17.jpg" alt="sudo root">
</div>

# Part 6. Установка и настройка службы времени

**Настроить службу автоматической синхронизации времени**

- Вывод времени, часового пояса, в соответствии с нашим местоположением:

<div align="center">
  <img src="/home/deadline/DO1_Linux/src/18.jpg" alt="time and date">
</div>

# Part 7. Установка и использование текстовых редакторов

**Установить текстовые редакторы VIM (+ любые два по желанию NANO, MCEDIT, JOE и т.д.)**

