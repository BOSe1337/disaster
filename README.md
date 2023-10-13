Домашнее задание к занятию 1 «Disaster recovery и Keepalived»

### Задание 1

- Дана [схема](1/hsrp_advanced.pkt) для Cisco Packet Tracer, рассматриваемая в лекции.
- На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
- Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).

Для настройки интерфейса Gi0/0 на обоих маршрутизаторах используем следующие команды:

![alt text](https://github.com/BOSe1337/disaster/blob/main/1.jpg)


![alt text](https://github.com/BOSe1337/disaster/blob/main/2.jpg)


При обрыве связи с одним маршрутизатором данные идут через второй:

![alt text](https://github.com/BOSe1337/disaster/blob/main/3.jpg)


### Задание 2
- Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в лекции, используя пример конфигурационного [файла](1/keepalived-simple.conf).
- Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах
- Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.
- Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный IP на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script

![alt text](https://github.com/BOSe1337/disaster/blob/main/4.jpg)

![alt text](https://github.com/BOSe1337/disaster/blob/main/5.jpg)

![alt text](https://github.com/BOSe1337/disaster/blob/main/6.jpg)

![alt text](https://github.com/BOSe1337/disaster/blob/main/7.jpg)

![alt text](https://github.com/BOSe1337/disaster/blob/main/8.jpg)

![alt text](https://github.com/BOSe1337/disaster/blob/main/9.jpg)

![alt text](https://github.com/BOSe1337/disaster/blob/main/10.jpg)

![alt text](https://github.com/BOSe1337/disaster/blob/main/11.jpg)

![alt text](https://github.com/BOSe1337/disaster/blob/main/12.jpg)

![alt text](https://github.com/BOSe1337/disaster/blob/main/13.jpg)
