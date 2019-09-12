
ejecutar en terminal como superusuario 

Vim .bashrc
Presione la tecla i para insertar
Luego agregar en la ultima lines xhost +
Presione la tecla esc
Presione la tecla shift + :
Digitar wq
Enter

luego copiar la carpeta tigervnc en la direccion documentos


agregamos a la tarea programada crontab desde una terminal como superusuario ejecutamos crontab -e

Presione la tecla i para insertar los siguiente:

@reboot /bin/sleep 60 ; /home/nuo/Documentos/tigervnc/usr/bin/x0vncserver -display=:0 -SecurityTypes=none > /home/nuo/Documentos/tigervnc/usr/bin/log/crone.log 2>&1

En esta linea hay que tener en cuenta la ruta /home/nuo/Documentos/..
donde nuo es el nombre del equipo, si el equipo se llama dirferente hay que reemplazar ejemplo  /home/{nombre_del_equipo}/Documentos/.. 

Presione la tecla esc
Presione la tecla shift + :
Digitar wq
Enter


Finalmente desde una terminal como superusuario su dar los permisos escribiendo

chmod +x /home/nuo/Documentos/tigervnc/usr/bin/x0vncserver


