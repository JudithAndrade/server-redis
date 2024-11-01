# Server-Redis
tener instalado el sistema Operativo  y en mi caso instale linux mint , ya unas vez  instalado  iniciaremos   hacer que reciba el Ethernet 
se me  asigno la ip 10.4.8.41 con esta ip usaremos para configurar  cuando terminados 



##INSTALL DE SERVER  REDIS
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
nota: sale un error en crear  el usuario Acl que ocupa permiso y este "El error ACL en Redis está relacionado con el sistema de Control de Acceso (Access Control Lists) que se introdujo en Redis 6.0" y cuando se instalo  Redis  la version de redis mucho menor v:3.0.6 ya la version menos actualizado 


