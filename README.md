# Instalar servidor DEBIAN (12)

# Instalación de VM

Se instala una versión en una VM

En la etapa final de la instalación en programas:

[x] SSH Server

[x] Utilidades estándar del sistema

# Post instalación

ingresar al sistema con el usuario root

Obtener la IP para conectarse remotamente

```
ip addres
```
y luego

```
apt update
apt -y upgrade
```
## Instalar herramientas

```
apt install vim
#apt install wget 
apt install htop
apt install duf
apt install net-tools
apt install network-manager
apt install git
apt install ufw # firewall
```

### Activar firewall

```bash
ufw enable
```
#### Habiliar puerto

```bash
ufw allow [PORT]/tcp
```

## Ver los puertos abiertos de linux

```
netstat -tulpn
```
para abrir los puertos:

https://jmjinformatico.es/abrir-puertos-en-debian-11/

## cambiar los datos de conexión


```
apt install network-manager
```

y luego ejecutar para cambiar la configuración de red local

```
nmtui
```

# Conexión remota

Para conectarse remotamente

```
ssh root@IP
```

ingresar la contraseña y listo


**IMPORTANTE**
En debian no existe el comando sudo, hay que ingresar con el root. 


# Instalar Apache

Utilizar esta guía.

https://laboratoriolinux.es/index.php/-noticias-mundo-linux-/software/34772-como-configurar-eficientemente-un-servidor-web-en-debian-gnu-linux.html


```bash
apt install apache2
systemctl start apache2
systemctl enable apache2
apt install ufw
```

## Comandos de apache

```
systemctl [start|restart|stop] apache2
```

```
a2ensite mi-sitio.com
systemctl reload apache2
```


# Instalar PHP

https://itslinuxfoss.com/install-php-debian-12/

```bash
apt install php libapache2-mod-php
```

## Instalar extensiones de PHP

```bash
apt install -y php-gd php-curl php-zip
systemclt restart apache2a
```