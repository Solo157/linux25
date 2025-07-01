ДЗ. Управление пакетами. Дистрибьюция софта

Установили необходимые программы.
![img.png](imgs/HW7/img.png)

Установили nginx.
![img_1.png](imgs/HW7/img_1.png)

Поставили все зависимости для сборки nginx.
![img_2.png](imgs/HW7/img_2.png)

Скачали исходный код для модуля ngx_brotli для сборки.
![img_3.png](imgs/HW7/img_3.png)

Собрали модуль ngx_brotli.
![img_4.png](imgs/HW7/img_4.png)

Отредактировали файл спецификации nginx. Добавили путь до модуля.
![img_5.png](imgs/HW7/img_5.png)

Выполняем сборку RPM-пакета.
![img_6.png](imgs/HW7/img_6.png)

Пакеты собрались.
![img_7.png](imgs/HW7/img_7.png)

Скопировали в общий каталог.
![img_8.png](imgs/HW7/img_8.png)

Запустили nginx, убедились, что он активен.
![img_9.png](imgs/HW7/img_9.png)

Создать свой репозиторий и разместить там ранее собранный RPM

Создали repo и скопировали туда пакеты.
![img_10.png](imgs/HW7/img_10.png)

Отредактировали конфигурацию nginx.
![img_11.png](imgs/HW7/img_11.png)

По Curl видны пакеты в директории repo.
![img_12.png](imgs/HW7/img_12.png)

Добавляем новый наш репозиторий в общий перечень репозиторий в системе.
![img_13.png](imgs/HW7/img_13.png)

Репозиторий виден и работает.
![img_14.png](imgs/HW7/img_14.png)

Добавили пакет в репозиторий, обновили репозиторий и обновили кэш в yum.
![img_16.png](imgs/HW7/img_16.png)

Установили репозиторий percona-release.
![img_17.png](imgs/HW7/img_17.png)
