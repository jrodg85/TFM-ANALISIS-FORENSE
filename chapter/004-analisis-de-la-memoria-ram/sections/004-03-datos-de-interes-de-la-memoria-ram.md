En el anexo Creación perfil ubuntu AWS, hemos realizado una guia para crear el perfil de Linux AWS que detectado durante el análisis del sistema operativo.

Una vez creado el perfil de linuxUbuntu_4.15.0-1021-aws procederemos a hacer un pslist para listar todas las aplicaciones que estaban ejecutándose en el momento de la captura.

Para comprobar que el perfil funciona, vamos a comenzar a comprobar cual es el CPU que usa el sistema.

Para ello ejecutaremos $\text{sudo python2.7 vol.py --profile=LinuxlinuxUbuntu_4_15_0-1021-awsx64 -f '/home/jrodg85/Server_RAM.mem' linux_cpuinfo}$.
Al comprobar que el perfil funciona, obtenemos que solo hay un procesador de marca GenuineIntel modelo Intel(R) Xeon(R) CPU E5-2676 v3 que tiene una frecuencia de 2.4Ghz.

Otro comando de interés es obtener el history del la terminal, con ello podemos observar los pasos realizados y los que ha ejecutado. Para ello ejecutaremos el comando $\text{sudo python2.7 vol.py --profile=LinuxlinuxUbuntu_4_15_0-1021-awsx64 -f '/home/jrodg85/Server_RAM.mem' linux_bash}$. Los comandos usados son los siguientes




\begin{enumerate}
    \item exit
    \item sudo apt update
    \item sudo systemctl restart postfix
    \item ls -l
    \item mysql -uroot -p
    \item cd apache2/
    \item ls -l
    \item sudo vi /etc/mysql/debian.cnf
    \item ps -ef| grep mysql
    \item tail access.log.1
    \item cd /var/www/html
    \item sudo kill -9 4539
    \item ls -als
    \item cd /
    \item ps -ef| grep mysql
    \item sudo mysqld_safe --skip-grant-tables
    \item H?=? &
    \item qls -l tmp
    \item qls -l tmp
    \item cd
    \item exit
    \item vi functions.php
    \item ps -ef| grep mysql
    \item ls -l /var/run/mysqld
    \item ls -l /run
    \item ls -lt
    \item ls -lt| more
    \item vi access.log.1
    \item sudo mysql_secure_installation
    \item ls -l
    \item p?JU
    \item su mysql
    \item tail access.log
    \item cat /var/log/mysql/error.log
    \item cd /var/log
    \item find . -name functions.php
    \item sudo apt install python-certbot-apache
    \item sudo service apache2 restart
    \item ps -ef| grep mysql
    \item mysql -uroot -p
    \item sudo apt-get install apache2
    \item apt-cache search mysql-server
    \item apt-cache search php
    \item mysql -u root -p
    \item ls -l
    \item #1546501785
    \item tail error.log
    \item sudo vi functions.php
    \item sudo mysql
    \item ls -l /var/run
    \item exit
    \item ls -l
    \item apt-cache search php| grep apache
    \item sudo vi /etc/mysql/debian
    \item tail syslog
    \item sudo apt-get install mysql-server
    \item _service
    \item apt-cache search mysql | grep php
    \item sudo cp /home/ubuntu/wordpress-4.9.8.tar.gz  .
    \item cd /var/log
    \item cd
    \item U
    \item H???Nt??nu??6
    \item sudo mysqld_safe --skip-grant-tables &
    \item apt-cache search mysql
    \item pwd
    \item ls -l
    \item ls -l
    \item `uSU
    \item sudo mv * ..
    \item ?,YU
    \item sudo mysqld_safe --skip-grant-tables
    \item r="$c_clear$r"
    \item ls -l /run
    \item ls -l
    \item COMPREPLY=($(compgen -W "--help --local" -- $cur_word))
    \item ls -l
    \item sudo tar xzf wordpress-4.9.8.tar.gz
    \item sudo apt-get install aapche2
    \item tail -100 kern.log
    \item mysql -u root -p
    \item cd ..
    \item cd /var/www/html/
    \item ps -ef| grep mysql
    \item apt-cache search php
    \item cd wordpress/
    \item cd hhtml
    \item sudo rm -r wordpress/
    \item ls -l
    \item ls -l
    \item sudo chmod 777 /var/run/mysqld
    \item sudo apt upgrade
    \item ls -l
    \item sudo vi /etc/apache2/sites-enabled/000-default.conf
    \item cd htmlls -l
    \item mysql -uroot -p
    \item ls -l
    \item ls -l
    \item ls -l
    \item sudo chown -R www-data:www-data html
    \item sudo mysqld_safe --skip-grant-tables
    \item cd /var/www/html
    \item find . -name functions.php -exec grep -H add_filer {} \;
    \item sudo apt install libapache2-mod-php
    \item exit
    \item cd /var/lg
    \item suudo mysqld_safe --skip-grant-tables &
    \item ls -l
    \item cd /var/log/apache2/sites-e
    \item mysql -u root -p
    \item cd
    \item sudo service mysql restart
    \item find . -name functions.php -exec grep -H add_filter {} \;
    \item apt-cache search apache2
    \item sudo apt-get update
    \item cat debian
    \item ?2JU
    \item echo "Test 1" | mail -s "Test 1" test12312321@mailinator.com
    \item sudo chmod 777 /run/mysqld/
    \item dpkg -l | grep mysql-server
    \item sudo certbot --apache -d ganga.site -d www.ganga.site
    \item ps -ef| grep mysql
    \item cd /var/log/apache2/
    \item sudo mkdir /run/mysqld
    \item cd /etc/mysql/
    \item sudo grep root *
    \item mysql -u root -p
    \item ps -ef| grep mysql
    \item sudo mysqld_safe --skip-grant-tables
    \item mysql -u root
    \item ls -l /run
    \item cd /var/log
    \item cd
    \item sudo dpkg-reconfigure mysql-server-5.7
    \item sudo service mysql stop
    \item cd apache2/
    \item sudo service mysql stop
    \item cat /var/log/mysql/error.log
    \item sudo kill -9 3181
    \item ls -l
    \item mysql -u root
    \item more access.log.1
    \item dpkg -l | grep mysql
    \item chmod 777 /run/mysqld/
    \item g|MP?(E)G|wm[av]|WM[AV]|avi|AVI|asf|vob|VOB|bin|dat|divx|DIVX|vcd|ps|pes|fli|flv|FLV|fxm|FXM|viv|)4[av]|M?(P)4[AV]|mkv|MKV|og[agmvx]|OG[AGMVX]|t[ps]|T[PS]|m2t?(s)|M2T?(S)|mts|MTS|wav|WAV|flac||XM)|+([0-9]).@(vdr|VDR))?(.part)'
    \item sudo kill -9 3182 3542
    \item sudo kill -9 4179
    \item ls
    \item ls -l
    \item sudo service mysql stop
    \item ?
    \item ls -l
    \item sudo service apache2 rewtart
    \item ls
    \item sudo apt install mailutils
    \item ls -lt| more
    \item sudo cat debian.cnf
    \item exit
    \item pwd
    \item mysql -u root -p
    \item cat /etc/issue
    \item cd wordpress/
    \item tail error.log
    \item tail error.log
    \item vi access.log
    \item cd ..
    \item cd wp-content/themes/twentyseventeen/
    \item sudo systemctl restart psotfix
    \item ls -l
    \item exit
    \item mysql_secure_installation
    \item mysql -uroot -p
    \item sudo cat /etc/mysql/debian
    \item ls -l tmp
    \item mysql -u root -p
    \item tail syslog
    \item cd /tmp
    \item exit
    \item cd html
    \item find . -name functions.php -exec grep -H add_filter {} \;
    \item cat debian.cnf
    \item mysql -u root
    \item suudo mysql_secure_installation
    \item sudo cat /etc/mysql/debian.cnf
    \item sudo service apache2 retart
    \item sudo rm index.html
    \item sudo rm -r /run/mysqld
    \item sudo vi wp-config.php
    \item sudo systemctl reload apache2
    \item sudo service mysql start
    \item sudo vi /etc/postfix/main.cf
    \item tail access.log
    \item tail -100 syslog
    \item ps -ef| grep mysql
    \item cd /var/log/apache2/
    \item ls- l
    \item pwd
    \item vi index.html
    \item sudo apachectl configtest
    \item ps -ef| grep mysql
    \item sudo mkdir /var/run/mysqld
    \item tail access.log
    \item exit
    \item sudo add-apt-repository ppa:certbot/certbot
    \item tail access.log
    \item ls -l
    \item tail -100 access.log
    \item tail -100 access.log
    \item execute-command
    \item sudo mysqld_safe --skip-grant-tables &
    \item sudo kill 3181
    \item exit
    \item !
    \item sudo service apache2 restart
    \item sudo apt install php-mysql
    \item date
    \item cd ap
    \item ls -l
    \item grep POST access.log
    \item ls -l
    \item vi access.log
    \item ls -l
    \item cd home
    \item cd /var/log
    \item sudo apchectl configtest
    \item sudo service mysql start
    \item sudo vi /etc/php/7.2/apache2/php.ini
    \item sudo kill -9 4178
    \item tail -100 syslog
    \item ps -ef| grep mysql
    \item tail -100 syslog
    \item sudo rm wordpress-4.9.8.tar.gz
    \item ls -l /run
    \item ??OU
    \item ls -l /etc/cron.d
    \item ls -l
    \item cd /tmp
    \item sudo insmod lime-4.15.0-42-generic.ko "path=captura.mem format=lime"
    \item cat /etc/issue
    \item uname -a
    \item ls -l
    \item rm lime-4.15.0-42-generic.ko
    \item ls -l
    \item sudo insmod lime-4.15.0-1021-aws.ko "path=captura.mem format=lime"
\end{enumerate}

Analizando los comandos realizados se pueden destacar los siguientes:

\begin{itemize}
    \item \textbf{exit}: Sale de la sesión actual, ya sea una sesión de terminal o una conexión SSH.
    \item \textbf{sudo apt update}: Actualiza la lista de paquetes disponibles y sus versiones. Es un paso previo común antes de instalar o actualizar paquetes.
    \item \textbf{sudo systemctl restart postfix}: Reinicia el servicio Postfix, un agente de transferencia de correo (MTA).
    \item \textbf{ls -l}: Lista los archivos en el directorio actual en un formato detallado.
    \item \textbf{mysql -uroot -p}: Inicia sesión en el servidor MySQL como usuario 'root', pidiendo la contraseña.
    \item \textbf{cd apache2/ y movimientos similares}: Cambia el directorio actual a uno especificado.
    \item \textbf{sudo vi /etc/mysql/debian.cnf}: Edita el archivo de configuración de MySQL usando el editor vi.
    \item \textbf{ps -ef| grep mysql}: Muestra los procesos actuales relacionados con MySQL.
    \item \textbf{sudo kill -9 4539}: Mata de manera forzosa el proceso con el ID 4539.
    \item \textbf{sudo mysqld_safe --skip-grant-tables}: Inicia MySQL en un modo especial que omite ciertas comprobaciones de seguridad.
    \item \textbf{sudo apt install python-certbot-apache}: Instala Certbot para Apache, una herramienta para obtener certificados SSL/TLS de Let's Encrypt.
    \item \textbf{sudo service apache2 restart}: Reinicia el servidor web Apache.
    \item \textbf{sudo mysql_secure_installation}: Ejecuta un script para mejorar la seguridad de MySQL.
    \item \textbf{sudo apt-get install mysql-server}: Instala el servidor MySQL.
    \item \textbf{sudo chmod 777 /var/run/mysqld}: Cambia los permisos del directorio /var/run/mysqld para que todos los usuarios puedan leer, escribir y ejecutar archivos en él.
    \item \textbf{sudo chown -R www-data:www-data html}: Cambia la propiedad del directorio html al usuario y grupo www-data, comúnmente usado para servidores web.
    \item \textbf{find . -name functions.php -exec grep -H add_filer {} \;}: Busca en archivos functions.php y ejecuta grep en ellos.
    \item \textbf{tail access.log y variantes}: Muestra las últimas líneas de los archivos de registro especificados.
    \item \textbf{sudo vi /etc/apache2/sites-enabled/000-default.conf}: Edita la configuración predeterminada del sitio de Apache.
    \item \textbf{sudo apt upgrade}: Actualiza todos los paquetes instalados a sus últimas versiones.
    \item \textbf{sudo systemctl reload apache2}: Recarga la configuración de Apache sin reiniciar el servicio.
    \item \textbf{sudo service mysql stop}: Detiene el servicio MySQL.
    \item \textbf{sudo dpkg-reconfigure mysql-server-5.7}: Reconfigura la versión especificada del servidor MySQL.
    \item \textbf{sudo apachectl configtest}: Verifica la sintaxis de los archivos de configuración de Apache.
    \item \textbf{sudo add-apt-repository ppa:certbot/certbot}: Añade el repositorio PPA para Certbot.
    \item \textbf{sudo apt install php-mysql}: Instala el módulo PHP para interactuar con MySQL.
    \item \textbf{sudo insmod lime-4.15.0-42-generic.ko "path=captura.mem format=lime"}: Carga un módulo del kernel para la captura de memoria.

\end{itemize}




















