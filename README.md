# Server-Redis
tener instalado el sistema Operativo  y en mi caso instalamos  linux mint , ya unas vez  instalado  iniciaremos   hacer que reciba el Ethernet 
se me  asigno la ip 10.4.8.41 con esta ip usaremos para configurar  cuando terminados  empesaremos la configuracion de  server  .

# INSTALACION  DE SERVER  REDIS
`````
sudo apt-get install lsb-release curl gpg
`````
```
curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg
````
```
sudo chmod 644 /usr/share/keyrings/redis-archive-keyring.gpg
`````
````
echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list
`````
```
sudo apt-get update
```
```
sudo apt-get install redis
`````

Una vez que Redis se esté ejecutando, puedes probarlo ejecutando redis-cli:
```
redis-cli
```
Pruebe la conexión con el comando ping:
````
127.0.0.1:6379> ping
PONG
````

Para crear ACL USERS

Tendremos que probar se crear el Users
Syntax
````
ACL USERS
````
probamos si guarda los datos  
ejemplo  
````
127.0.0.1:6379> set key1 10
````
````
Output
OK
````
`````
127.0.0.1:6379> set key1 10
`````
````
Output
"10"
````
verificamos que si funciona 
Ejemplo
`````
> ACL USERS
1) "anna"
2) "antirez"
3) "default"
`````
nota: sale un error en crear  el usuario Acl que ocupa permiso y este "El error ACL en Redis está relacionado con el sistema de Control de Acceso (Access Control Lists) que se introdujo en Redis 6.0" y cuando se instalo  Redis  la version de redis mucho menor  v:3.0.6 ya la version menos actualizado 
continuacion  se mostra  el error acrear los usuarios en redis en terminal 



![IMG_20241106_170246_357](https://github.com/user-attachments/assets/cd7b4181-ab1b-4d71-9134-ef738b24f89b)


## Creacion de Usuarios en Terminal
1 Ejecuta el comando en la terminal:
`````
sudo adduser nombre_usuario
`````

2. Ingresa la contraseña para el nuevo usuario:
Después de ejecutar el comando, el sistema te pedirá que ingreses una contraseña para el usuario recién creado.
````
Enter new UNIX password:
````
3.Confirma la contraseña:

El sistema te pedirá que ingreses la contraseña nuevamente para confirmar
``````
 sudo password ite2024
``````
 usuarios ya creados 
 ![IMG_20241106_170102_133](https://github.com/user-attachments/assets/bd202f7e-c720-4b50-a290-2c724c2e6a4f)
