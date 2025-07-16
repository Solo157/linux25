ДЗ. SYSTEMD

Написать service, который будет раз в 30 секунд мониторить лог на предмет наличия ключевого слова

Создал файлы. /etc/default/watchlog - конфиг сервиса. и сами логи.
![img.png](imgs/HW9/img.png)

Создал скрипт.
![img_1.png](imgs/HW9/img_1.png)

Создал юнит для сервиса.
![img_2.png](imgs/HW9/img_2.png)

Создал юнит для таймера.
![img_3.png](imgs/HW9/img_3.png)

Почему-то таймер не отрабатывает, но вручную запуск сервис вотчера работает.
![img_4.png](imgs/HW9/img_4.png)

Нет, начал отрабатывать. Показывает время следующего запуска. 
![img_5.png](imgs/HW9/img_5.png)
![img_6.png](imgs/HW9/img_6.png)


Установить spawn-fcgi и создать unit-файл (spawn-fcgi.sevice) с помощью переделки init-скрипта

Установил spawn-fcgi.
![img_7.png](imgs/HW9/img_7.png)

Создал файл fcgi.conf
![img_8.png](imgs/HW9/img_8.png)

Написал fcgi.service
![img_9.png](imgs/HW9/img_9.png)

Создал php-fcgi.sock и выполнил spawn-fcgi статус - работает.
![img_10.png](imgs/HW9/img_10.png)


Доработать unit-файл Nginx (nginx.service) для запуска нескольких инстансов сервера с разными конфигурационными файлами одновременно

Создал файл unit-а и установил nginx.
![img_11.png](imgs/HW9/img_11.png)

Создал два файла и добавил конфигурацию в них.
![img_12.png](imgs/HW9/img_12.png)

Запустил nginx-ы с разными конфигами на разных портах. Видим, что слушаются указанные в конфиге порты.
![img_13.png](imgs/HW9/img_13.png)
![img_14.png](imgs/HW9/img_14.png)
![img_15.png](imgs/HW9/img_15.png)

Видим две группы процессов. Все в порядке.
![img_16.png](imgs/HW9/img_16.png)

p.s. была проблема с запуском экземпляров nginx, как оказалось, надо было закомментить "include /etc/nginx/sites-enabled/*;"
![img_17.png](imgs/HW9/img_17.png)