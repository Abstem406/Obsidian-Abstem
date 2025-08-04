

## Método 1: Usando el comando `netstat`

1. **Acceder a la VPS**
   - Conéctate a tu VPS a través de SSH (Secure Shell) utilizando la siguiente sintaxis:
     ```bash
     ssh usuario@direccion_ip
     ```
     Reemplaza `usuario` con tu nombre de usuario y `direccion_ip` con la IP de tu VPS.

2. **Instalar `net-tools`**
   - En algunos sistemas, el comando `netstat` puede no estar instalado por defecto. Instálalo ejecutando:
     ```bash
     sudo apt-get install net-tools
     ```

3. **Ejecutar el comando `netstat`**
   - Utiliza el siguiente comando para ver todos los puertos en uso:
     ```bash
     sudo netstat -tuln
     ```
     - `-t`: Mostrar conexiones TCP.
     - `-u`: Mostrar conexiones UDP.
     - `-l`: Mostrar solo los sockets en estado de escucha.
     - `-n`: Mostrar direcciones y puertos en formato numérico.

   - Para buscar un puerto específico, puedes usar `grep`:
     ```bash
     sudo netstat -tuln | grep :puerto
     ```
     Reemplaza `puerto` con el número del puerto que deseas verificar.

## Método 2: Usando el comando `ss`

1. **Acceder a la VPS**
   - Conéctate a tu VPS a través de SSH:
     ```bash
     ssh usuario@direccion_ip
     ```

2. **Ejecutar el comando `ss`**
   - Utiliza el siguiente comando para ver todos los puertos en uso:
     ```bash
     sudo ss -tuln
     ```
     - `-t`: Mostrar conexiones TCP.
     - `-u`: Mostrar conexiones UDP.
     - `-l`: Mostrar solo los sockets en estado de escucha.
     - `-n`: Mostrar direcciones y puertos en formato numérico.

   - Para buscar un puerto específico, puedes usar `grep`:
     ```bash
     sudo ss -tuln | grep :puerto
     ```

## Método 3: Usando el comando `lsof`

1. **Acceder a la VPS**
   - Conéctate a tu VPS a través de SSH:
     ```bash
     ssh usuario@direccion_ip
     ```

2. **Instalar `lsof`**
   - En algunos sistemas, el comando `lsof` puede no estar instalado por defecto. Instálalo ejecutando:
     ```bash
     sudo apt-get install lsof
     ```

3. **Ejecutar el comando `lsof`**
   - Utiliza el siguiente comando para buscar un puerto específico:
     ```bash
     sudo lsof -i :puerto
     ```
     Reemplaza `puerto` con el número del puerto que deseas verificar.

## Ejemplo de Uso

Supongamos que deseas verificar si el puerto `80` está en uso:

```bash
sudo netstat -tuln | grep :80