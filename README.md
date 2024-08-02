**Contenidos**
- [1. Docker FTP](#1-docker-ftp)
- [2. Instalación](#2-instalación)


# 1. Docker FTP
Permite levantar un servidor FTP rápidamente con Docker


# 2. Instalación
- **Descomentar** la **imagen** en [docker-compose.yml](/docker-compose.yml) a utilizar:
    - Arquietecturas de **64 bits** (x64): `panubo/vsftpd`
    - Arquitecturas **ARM** (Raspberry): `pablokbs/panubo-vsftpd-arm`

- Modificar las **variables** en [docker-compose.yml](/docker-compose.yml) (marcadas con `<>`)
    - `<usuario>`: Nombre del **usuario** FTP
    - `<password>`: **Contraseña** del usuario FTP
    - `<ruta_local>`: **Ruta** local de la **carpeta** a compartir

- Añadir el **volumen**: El volúmen deben estar enlazado con `/srv` y el **dueño** y los **permisos** de la carpeta deben ser los siguientes:
    ```bash
    sudo chown -R 1001:root <ruta_local>
    sudo chmod -R 755 <ruta_local>
    ```

- Ejecutar `docker compose up -d --build`
