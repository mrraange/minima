# # minim

Обновляем пакет

<code>sudo apt update && sudo apt install wget && sudo apt install curl -y</code>

Запускаем скрипт установки

<code>wget -O minima_setup.sh https://raw.githubusercontent.com/minima-global/Minima/master/scripts/minima_setup.sh && chmod +x minima_setup.sh && sudo ./minima_setup.sh -p 9001</code>

как пойдут логи CTR+C

Вводим команду:

<code>curl 127.0.0.1:9005/incentivecash%20uid:xxx-xxx-xxx-xxx-xxx</code>

![Screenshot_5](https://user-images.githubusercontent.com/100018176/187982681-17412873-ac59-40ab-ac49-80a5e661df3e.png)

<i>пример: curl 127.0.0.1:9005/incentivecash%20uid:00F3E50D-5A52-444B-8F1A-0DA72D6CAA84</i>

ПОЛЕЗНЫЕ КОМАНДЫ

<code>curl 127.0.0.1:9005/incentivecash | jq</code>   -  Выводит информацию о ревардах

p.s.
подойтет всем, кто администрирует не одну ноду

Запуск нескольких узлов на одном сервере? Вы можете указать разные номера портов в конце, чтобы сделать это. Например (с использованием 9122 и 9121)

пример:

wget -O minima_setup.sh https://raw.githubusercontent.com/minima-global/Minima/master/scripts/minima_setup.sh && chmod +x minima_setup.sh && sudo ./minima_setup.sh -r 9122 -p 9121

p.p.s

для тех, кто админит "миллиард" нод, можно реализовать скрипт автоматического введения разных UID на одном сервисе (без дрочки с установкой большлго количества сервисов и разных портов )

1. вводите 

<code>crontab -e</code>

<code>0 */3 * * *  bash /root/minima_cron_minima_9001.sh</code>  (крон будет выполнять скрипт minima_cron_minima_9001.sh раз в три часа)

![photo1662055952](https://user-images.githubusercontent.com/100018176/187984157-23b6f784-58e9-4e0c-8d7d-6021fca69ade.jpeg)

CTR+O Enter CRT+X

2. далее

<code>wget -O minima_cron_minima_9001.sh https://raw.githubusercontent.com/mrraange/minima/main/minima_cron_minima_9001.sh</code>

<code>nano minima_cron_minima_9001.sh</code>

вносите правки в файл (меняете везде "ваш UID" на настоящий UID)

CTR+O Enter CRT+X

Извините за внимание!
