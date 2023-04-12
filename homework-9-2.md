#9.2 «Система мониторинга Zabbix» Basmanov Vitaliy

#Задание 1
## все команды выполнял под root
## apt install postgresql
## wget https://repo.zabbix.com/zabbix/6.0/debian/pool/main/z/zabbix-release/zabbix-release_6.0-4+debian11_all.deb
## dpkg -i zabbix-release_6.0-4+debian11_all.deb
## apt update
## apt install zabbix-server-pgsql zabbix-frontend-php php7.4-pgsql zabbix-apache-conf zabbix-sql-scripts
## sudo -u postgres createuser --pwprompt zabbix
## sudo -u postgres createdb -O zabbix zabbix
## zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix
## измненил в файле /etc/zabbix/zabbix_server.conf "DBPassword=" "DBPassword=12345"
## systemctl restart zabbix-server zabbix-agent apache2
## systemctl enable zabbix-server zabbix-agent apache2
[Скриншот](https://github.com/basmanov/basmanovv/blob/main/9.2.1.png)

#Задание 2
## все команды выполнял под root 
## wget https://repo.zabbix.com/zabbix/6.0/debian/pool/main/z/zabbix-release/zabbix-release_6.0-4+debian11_all.deb
## dpkg -i zabbix-release_6.0-4+debian11_all.deb
## apt update
## apt install zabbix-agent
## systemctl restart zabbix-agent
## systemctl enable zabbix-agent
[Скриншот 1](https://github.com/basmanov/basmanovv/blob/main/9.2.2.png)
[Скриншот 2](https://github.com/basmanov/basmanovv/blob/main/9.2.2.2.png)
