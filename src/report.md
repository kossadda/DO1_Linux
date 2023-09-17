# Part 1. Установка ОС

**Установить Ubuntu 20.04 Server LTS без графического интерфейса. (Используем программу для виртуализации - VirtualBox)**  <br>

- Устанавка образа ОС в VirtualBox:

<div align="center">
  <img src="screenshots/1.jpg" alt="install OS">
</div>

- Проверка номера версии:

<div align="center">
  <img src="screenshots/2.jpg" alt="version">
</div>

<br>

# Part 2. Создание пользователя

**Создать пользователя, отличного от пользователя, который создавался при установке. Пользователь должен быть добавлен в группу adm**  <br>

- Создание нового пользователя user_two и добавление его в группу adm:

<div align="center">
  <img src="screenshots/3.jpg" alt="add user">
</div>

- Вывод команды \ cat /etc/passwd:

<div align="center">
  <img src="screenshots/4.jpg" alt="show user">
</div>

<br>

# Part 3. Настройка сети ОС 

**1. Задать название машины вида user-1**  
**2. Установить временную зону, соответствующую вашему текущему местоположению**  
**3. Вывести названия сетевых интерфейсов с помощью консольной команды**  <br>

- Определение названия машины вида user-1

<div align="center">
  <img src="screenshots/5.jpg" alt="change user">
</div>

- Установка временной зоны, соответствующей нашему текущему местоположению (выбор производится из списка по команде **timedatectl list-timezones**) и отображение изменений на выводе консоли:

<div align="center">
  <img src="screenshots/6.jpg" alt="switch timezone">
</div>

- Установка набора сетевых инструментов:

<div align="center">
  <img src="screenshots/7.jpg" alt="tools install">
</div>

- Вывод названия сетевых интерфейсов:

<div align="center">
  <img src="screenshots/8.jpg" alt="show net name">
</div>

***Информация:***  
***Интерфейс lo (Loopback Interface)** представляет собой виртуальный сетевой интерфейс в операционных системах, таких как Linux и UNIX-подобные системы. Он используется для локальной коммуникации на самом устройстве и обычно имеет IP-адрес 127.0.0.1, который также обозначается как "localhost".*  

- Получение ip адреса устройства, на котором производится работа, от DHCP сервера.

<div align="center">
  <img src="screenshots/9.jpg" alt="show ip adress">
</div>

***Информация:***  
***DHCP (Dynamic Host Configuration Protocol)** - это сетевой протокол, используемый для автоматической настройки сетевых параметров устройствам в компьютерной сети. Протокол DHCP позволяет устройствам автоматически получать IP-адреса, а также другие сетевые параметры, такие как шлюз по умолчанию (gateway), маску подсети (subnet mask), адреса DNS-серверов и многое другое.*  

- Вывод на экран внешнего ip-адрес шлюза:  

<div align="center">
  <img src="screenshots/10.jpg" alt="show external ip">
</div>

- Вывод на экран внутреннего IP-адрес шлюза, он же ip-адрес по умолчанию (gw):  

<div align="center">
  <img src="screenshots/11.jpg" alt="show internal ip">
</div>

- Установка статичных настроек ip, gw, dns (с использованием публичных DNS серверов, например 1.1.1.1 или 8.8.8.8):  

<div align="center">
  <img src="screenshots/12.jpg" alt="set static settings">
</div>

- Сохранение изменений. Перезагрузка виртуальной машины:

<div align="center">
  <img src="screenshots/13.jpg" alt="save changes">
</div>

- Проверка изменений статичных сетевых настроек (ip, gw, dns) на соответстветствие заданным в предыдущем пункте:

<div align="center">
  <img src="screenshots/14.jpg" alt="check changes">
</div>

- Пингование удаленных хостов 1.1.1.1 и ya.ru. Убедить в наличии на выводе команды фразы “0% packet loss”:

<div align="center">
  <img src="screenshots/15.jpg" alt="ping hosts">
</div>

<br>

# Part 4. Обновление ОС 

**Обновить системные пакеты до последней на момент выполнения задания версии**  <br>

- После успешного обновления повторно применяем команду и проверяем установлена ли последняя версия:

<div align="center">
  <img src="screenshots/16.jpg" alt="check updates">
</div>

<br>

# Part 5. Использование команды sudo 

**Разрешить пользователю, созданному в Part 2, выполнять команду sudo**  <br>

***Информация:***  
*Команда **sudo (Superuser Do)** в системах **Unix** и **Linux** используется для выполнения команд с правами суперпользователя (root) или другого пользователя, имеющего необходимые разрешения на выполнение определенной команды. Команда sudo позволяет пользователям выполнять административные задачи и другие привилегированные операции, обычно требующие повышенных привилегий, без необходимости входа в систему под учетной записью суперпользователя (root).*  

- Добавление нового пользователя в группу обладающих привелегией **sudo**. Переключение на данного пользователя. Изменение hostname ОС от имени пользователя, созданного в пункте Part 2 (используя sudo):

<div align="center">
  <img src="screenshots/17.jpg" alt="sudo root">
</div>

# Part 6. Установка и настройка службы времени

**Настроить службу автоматической синхронизации времени**

- Вывод времени, часового пояса, в соответствии с нашим местоположением:

<div align="center">
  <img src="screenshots/18.jpg" alt="time and date">
</div>

<br>

# Part 7. Установка и использование текстовых редакторов

**Установить текстовые редакторы VIM (+ любые два по желанию NANO, MCEDIT, JOE и т.д.)**  <br>

<div align="center">
  <img src="screenshots/19.jpg" alt="install redactors">
</div>

<br>

### Открытие редактора vim и ввод ника:

<div align="center">
  <img src="screenshots/20.jpg" alt="open vim">
</div>

***Для сохранения в новый файл test_vim.txt:***  
1. Нажимается ESC.  
2. Нажимается ":".  
3. В появившейся командной строке программы прописывается "wq test_vim.txt" (для сохранения текста в файл с указанным названием и последующего выхода из программы).  

<div align="center">
  <img src="screenshots/21.jpg" alt="save change">
</div>

- Проверка файла на сохранение введенного текста:

<div align="center">
  <img src="screenshots/22.jpg" alt="check vim text">
</div>

### Открытие редактора nano и ввод ника:

<div align="center">
  <img src="screenshots/23.jpg" alt="open nano">
</div>

- Нажатие Ctrl+X приводит к появлению следующего сообщения:

<div align="center">
  <img src="screenshots/24.jpg" alt="nano move 1">
</div>

- При подтверждении сохранения (нажатие на Y) выходит поле для имени будущего файла. Прописывается ***test_nano.txt***:

<div align="center">
  <img src="screenshots/25.jpg" alt="nano move 2">
</div>

- Проверка файла на сохранение введенного текста:

<div align="center">
  <img src="screenshots/26.jpg" alt="check nano text">
</div>

### Открытие редактора joe и ввод ника:

<div align="center">
  <img src="screenshots/27.jpg" alt="open joe">
</div>

- Нажатие Ctrl+K и W приводит к появлению поля для имени будущего файла. Прописывается ***test_joe.txt***:

<div align="center">
  <img src="screenshots/28.jpg" alt="joe move 1">
</div>

**Нажатие Ctrl+C после сохраненных изменений приводит к выходу из программы.**

- Проверка файла на сохранение введенного текста:

<div align="center">
  <img src="screenshots/29.jpg" alt="check joe text">
</div>

<br>

### Открытие test_vim.txt через vim и замена текста:

<div align="center">
  <img src="screenshots/30.jpg" alt="change vim text">
</div>

***Для выхода из vim без сохранения изменений:***  
1. Нажимается ESC.  
2. Нажимается ":".  
3. В появившейся командной строке программы прописывается "q!".  

<div align="center">
  <img src="screenshots/31.jpg" alt="vim move">
</div>

- Проверка файла на отсутствие изменений в тексте:

<div align="center">
  <img src="screenshots/32.jpg" alt="check vim text">
</div>

### Открытие test_nano.txt через nano и замена текста:

<div align="center">
  <img src="screenshots/33.jpg" alt="change nano text">
</div>

- Нажатие Ctrl+X приводит к появлению следующего сообщения (нажимается N для подтверждения выхода без сохранения изменений):

<div align="center">
  <img src="screenshots/34.jpg" alt="nano move">
</div>

- Проверка файла на отсутствие изменений в тексте:

<div align="center">
  <img src="screenshots/35.jpg" alt="check nano text">
</div>

### Открытие test_joe.txt через joe и замена текста:

<div align="center">
  <img src="screenshots/36.jpg" alt="change joe text">
</div>

- Нажатие Ctrl+C приводит к появлению следующего сообщения (нажимается y для подтверждения выхода без сохранения изменений):

<div align="center">
  <img src="screenshots/37.jpg" alt="joe move">
</div>

- Проверка файла на отсутствие изменений в тексте:

<div align="center">
  <img src="screenshots/38.jpg" alt="check joe text">
</div>

<br>

***Для поиска текста в vim необходимо:***  
1. Нажать на "/".  
2. Ввести шаблон поиска.  
3. Нажать Enter, чтобы выполнить поиск.  
4. Нажатие на "n" чтобы найти следующее вхождение, или "N" чтобы найти предыдущее вхождение.  

<div align="center">
  <img src="screenshots/39.jpg" alt="search vim text">
</div>

***Для поиска текста в nano необходимо:***  
1. Нажать на Ctrl+W.  
2. Ввести шаблон поиска.  
3. Нажать Enter, чтобы выполнить поиск.  
4. Для повторения поиска далее по тексту повторно нажимается Ctrl+W и Enter, для хождения в обратную сторону Ctrl+Q.  

<div align="center">
  <img src="screenshots/40.jpg" alt="search nano text">
</div>

***Для поиска текста в joe необходимо:***  
1. Нажать Ctrl+K и F.  
2. Ввести шаблон поиска и Enter.  
3. Нажать Enter, чтобы выполнить поиск далее по тексту.  
4. Для повторения поиска выполняются те же действия. Для поиска в обратную сторону необходимо после первого нажатия на Enter прописать b.  

<div align="center">
  <img src="screenshots/41.jpg" alt="shablon vim">
</div>

<div align="center">
  <img src="screenshots/42.jpg" alt="forward move">
</div>

<br>

***Для замены текста в vim необходимо:***  
1. Нажать на ":".  
2. Прописать "%s" для поиска по всему тексту.  
3. Через "/" ввести шаблон поиска.  
4. Снова через "/" прописать шаблон замены и нажать Enter.  
5. Для повторения команды выполнить все шаги заново.  

<div align="center">
  <img src="screenshots/43.jpg" alt="change shablon vim">
</div>

***Для замены текста в nano необходимо:***  
1. Нажать на "Ctrl+\".  
2. Ввести шаблон поиска и нажать Enter.  
3. Ввести шаблон замены и нажать Enter.  
4. Подтвердить замену текста нажатием на "Y". Для продолжения замены повторно нажать на "Y".  

<div align="center">
  <img src="screenshots/44.jpg" alt="change shablon nano 1">
</div>

<div align="center">
  <img src="screenshots/45.jpg" alt="change shablon nano 2">
</div>

<div align="center">
  <img src="screenshots/46.jpg" alt="change shablon nano 3">
</div>

***Для замены текста в joe необходимо:***  
1. Нажать Ctrl+K и F.  
2. Ввести шаблон поиска и Enter.  
3. Прописать r в появившейся командной строке и нажать Enter.  
4. Ввести шаблон замены и нажать Enter.  
5. Подтвердить замену текста нажатием на "Y". Для продолжения замены повторно нажать на "Y".  

<div align="center">
  <img src="screenshots/47.jpg" alt="change shablon joe 1">
</div>

<div align="center">
  <img src="screenshots/48.jpg" alt="change shablon joe 2">
</div>

<div align="center">
  <img src="screenshots/49.jpg" alt="change shablon joe 3">
</div>

<div align="center">
  <img src="screenshots/50.jpg" alt="change shablon joe 4">
</div>

<br>

# Part 8. Установка и базовая настройка сервиса SSHD 

**1. Установить службу SSHd.**  
**2. Добавить автостарт службы при загрузке системы.**  
**3. Перенастроить службу SSHd на порт 2022.**  
**4. Используя команду ps, показать наличие процесса sshd. Для этого к команде нужно подобрать ключи.**  <br>

- Установка службы SSHd:

<div align="center">
  <img src="screenshots/51.jpg" alt="install SSHd">
</div>

- Настройка автозапуска службы:

<div align="center">
  <img src="screenshots/52.jpg" alt="autostart SSHd">
</div>

- Изменение конфига:

<div align="center">
  <img src="screenshots/53.jpg" alt="change config">
</div>

- Проверка на запущенный процесс:

<div align="center">
  <img src="screenshots/54.jpg" alt="check SSHd">
</div>

***Информация:***  
*"ps" - выводит сведения о процессах в статическом виде*  
*"-e" - позволяет выбрать все процессы*  
*"| grep sshd" - вывод всех строк содержащих sshd*  

- Перезагрузка системы через reboot.  

- Вывод команды netstat -tan:

<div align="center">
  <img src="screenshots/55.jpg" alt="check netstat -tan">
</div>

***Информация:***  
*-t (флаг TCP): Этот флаг указывает netstat отображать только информацию о TCP-соединениях. TCP (Transmission Control Protocol) - это протокол управления передачей данных, который обеспечивает надежное и упорядоченное соединение между устройствами.*  
*-a (флаг All): Этот флаг указывает netstat отображать все сетевые соединения, включая прослушивающие порты и активные соединения. Если этот флаг не указан, netstat будет выводить только активные соединения.*  
*-n (флаг Numeric): Этот флаг указывает netstat не выполнять разрешение DNS-имен в IP-адреса. Вместо этого он отображает IP-адреса в числовом виде, что может ускорить выполнение команды и предотвратить задержки, связанные с DNS-запросами.*  

***Расшифровка столбцов вывода:***  
*1. Proto (Протокол): Этот столбец показывает используемый сетевой протокол для каждого соединения. Протокол может быть TCP (Transmission Control Protocol) или UDP (User Datagram Protocol). TCP используется для установления надежных соединений, а UDP - для более быстрой, но менее надежной передачи данных.*  
*2. Recv-Q (Очередь приема): Этот столбец показывает количество байт данных, ожидающих приема на сокете.*  
*3. Send-Q (Очередь отправки): Этот столбец показывает количество байт данных, ожидающих отправки на сокете.*  
*4. Local Address (Локальный адрес): Этот столбец указывает IP-адрес и порт вашего компьютера, на котором работает процесс или служба. IP-адрес обычно представлен в формате IPv4 (например, 192.168.1.1) или IPv6 (например, fe80::1).*  
*5. Foreign Address (Удаленный адрес): Этот столбец указывает IP-адрес и порт удаленного компьютера или сервера, с которым установлено сетевое соединение.*  
*6. State (Состояние): Этот столбец показывает текущее состояние сетевого соединения. Например, "ESTABLISHED" означает, что соединение установлено и активно, "LISTEN" означает, что порт прослушивается на входящие соединения, "TIME_WAIT" означает, что соединение было закрыто, но ожидает завершения последних пакетов данных.*  

<br>

# Part 9. Установка и использование утилит top, htop   

**Установить и запустить утилиты top и htop.**  <br>

1. uptime - 46 min  
2. Количество авторизованных пользователей - 1 user  
3. Общая загрузка системы - 0.00, 0.01, 0.00  
4. Общее количество процессов - 113 total  
5. Загрузка cpu - 0.0 us, 0.0 sy, 0.0 ni, 100.0 id, 0.0 wa, 0.0 hi, 0.0 si, 0.0 st  
6. Загрузка памяти - 2412.2 total, 1867.1 free, 157.3 used, 387.7 buff/cache  
7. pid процесса, занимающего больше всего памяти - 708  
8. pid процесса, занимающего больше всего процессорного времени - 708  

<br>

***Вывод команды htop отсортированной по PID:***  

<div align="center">
  <img src="screenshots/56.jpg" alt="sort by PID">
</div>

<br>

***Вывод команды htop отсортированной по PERCENT_CPU:***  

<div align="center">
  <img src="screenshots/57.jpg" alt="sort by PERCENT_CPU">
</div>

***Вывод команды htop отсортированной по PERCENT_MEM:***  

<div align="center">
  <img src="screenshots/58.jpg" alt="sort by PERCENT_MEM">
</div>

***Вывод команды htop отсортированной по TIME:***  

<div align="center">
  <img src="screenshots/59.jpg" alt="sort by TIME">
</div>

***Вывод команды htop отфильтрованной для процесса sshd:***  

<div align="center">
  <img src="screenshots/60.jpg" alt="filtred by sshd procces">
</div>

***Вывод команды htop с процессом syslog, найденным, используя поиск:***  

<div align="center">
  <img src="screenshots/61.jpg" alt="with syslog procces">
</div>

***Вывод команды htop с добавленным выводом hostname, clock и uptime:***  

<div align="center">
  <img src="screenshots/62.jpg" alt="with hostname, clock, uptime">
</div>

# Part 10. Использование утилиты fdisk

**Запустить команду fdisk -l.**  

**Disk /dev/sda, size: 25 GiB, 26843545600 bytes, 52428800 sectors**

<div align="center">
  <img src="screenshots/63.jpg" alt="fdisk -l">
</div>

<br>

# Part 11. Использование утилиты df

**1. Запустить команду df.**  
**2. Запустить команду df -Th.**  <br>

<div align="center">
  <img src="screenshots/64.jpg" alt="df /">
</div>

***Единица измерения в выводе: bytes***  <br>

<div align="center">
  <img src="screenshots/65.jpg" alt="df -Th /">
</div>

***Тип файловой системы раздела: ext4***  <br>

# Part 12. Использование утилиты du

**1. Запустить команду du.**  
**2. Вывести размер папок /home, /var, /var/log (в байтах, в человекочитаемом виде)**  
**3. Вывести размер всего содержимого в /var/log (не общее, а каждого вложенного элемента, используя "*")**  <br>

- Стандартная команда du:  

<div align="center">
  <img src="screenshots/66.jpg" alt="du">
</div>

- Вывод размера папок /home:  

<div align="center">
  <img src="screenshots/67.jpg" alt="du -h /home">
</div>

- Вывод размера папок /var:  

<div align="center">
  <img src="screenshots/68.jpg" alt="du -h /var">
</div>

- Вывод размера папок /var/log:  

<div align="center">
  <img src="screenshots/69.jpg" alt="du -h /var/log">
</div>

- Вывод размера всего содержимого в /var/log (не общее, а каждого вложенного элемента, используя *):  

<div align="center">
  <img src="screenshots/70.jpg" alt="du -h /var/log/*">
</div>

<br>

# Part 13. Установка и использование утилиты ncdu

**1. Установить утилиту ncdu.**  
**2. Вывести размер папок /home, /var, /var/log.**  <br>

- Установка ncdu:

<div align="center">
  <img src="screenshots/71.jpg" alt="install ncdu">
</div>

- Вывод размера папок /home:  

<div align="center">
  <img src="screenshots/72.jpg" alt="ncdu /home">
</div>

- Вывод размера папок /var:  

<div align="center">
  <img src="screenshots/73.jpg" alt="ncdu /var">
</div>

- Вывод размера папок /var/log:  

<div align="center">
  <img src="screenshots/74.jpg" alt="ncdu /var/log">
</div>

**Размеры папок на выводе ncdu совпадают с выводом du.**  

<br>

# Part 14. Работа с системными журналами

**Открыть для просмотра:**  
**1. /var/log/dmesg**  
**2. /var/log/syslog**  
**3. /var/log/auth.log**  <br>

- Данные о времени последней успешной авторизации, имени пользователя и методе входа в систему:

<div align="center">
  <img src="screenshots/75.jpg" alt="auth info">
</div>

- Производится перезапуск службы SSHd (sudo systemctl restart sshd).  

- Вывод с сообщением о рестарте службы:  

<div align="center">
  <img src="screenshots/76.jpg" alt="restart info">
</div>

# Part 15. Использование планировщика заданий CRON 

**1. Используя планировщик заданий, запустите команду uptime через каждые 2 минуты.**  
**2. Удалите все задания из планировщика заданий.**  <br>

- Внесение в планировщик заданий конфигурации для запуска uptime через каждые 2 минуты:  

<div align="center">
  <img src="screenshots/77.jpg" alt="uptime every 2 minute">
</div>

- Вывод в системном журнале строчек о минимум двух выполнениях:  

<div align="center">
  <img src="screenshots/78.jpg" alt="three time using uptime">
</div>

- Вывод на экран текущих заданий для CRON:  

<div align="center">
  <img src="screenshots/79.jpg" alt="running cron tasks">
</div>

- Удаление всех заданий из планировщика заданий:  

<div align="center">
  <img src="screenshots/80.jpg" alt="delete all tasks">
</div>