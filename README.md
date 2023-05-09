# `Домашнее задание 10.6 «Disaster recovery» - Зозуля Максим`

### Задание 1

В чём разница между DRaaS, BaaS, Active-Active, Active-Passive?

Приведите ответ в свободной форме.

### Ответ:

DRaaS - инструмент, который создает полноценную копию IT-инфраструктуры, в случае аварии принимает на себя всю нагрузку.

BaaS - инструмент, который создает копию системы, позволяет восстановить систему в случае потери или аварии.

Active-Passive - если один компонент системы падает, автоматически поднимается второй, который берет на себя всю работу.

Active-Active - есть два работающих компонента, оба работают с данными, если один из компонентов упадет никто даже не заметит что произошло.

---

### Задание 2

Компании нужно составить план восстановления в случае Disaster recovery. Сервер состоит из системного диска и диска с данными. Требуется копировать два логических диска на один физический:

системный диск (C:) (20 гигабайт);
диск с данными (D:) (256 гигабайт).
В требованиях говорится:

данные критичны в течение 24 часов после аварии;
сеть критична к большим потокам данных в рабочее время;
рабочее время с 9.00 до 18.00, пять дней (понедельник – пятница);
план резервирования должен быть реализован для диска C и для диска D. В случае Linux-систем /dev/sda1, /dev/sda4 или /dev/sdb1-данные;
считается, что для этой задачи может быть: 1) поставлен второй сервер или 2) выбрана облачная инфраструктура с определённой услугой;
компания готова платить за 10 терабайт места как в одном, так и в другом случае.
Приведите ответ в форме плана востановления с выбранным механизмом и получившейся топологией. 

### Ответ: 

При таких требованиях, можно использовать для бэкапа второй сервер внутри компании по модели Active-Passive. Если выйдет из строя первый сервер, второй возьмет на себя нагрузку, работа клиентов будет продолжена...
Также можно делать бэкапы инфраструктуры в облако, в нерабочее время к примеру: пн-пт в 19:00.
