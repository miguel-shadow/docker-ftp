# 1. FTP
Permite levantar un servidor FTP rápidamente con Docker

# 2. Instalación
- **Descomentar** la **imagen** en [docker-compose.yml](/docker-compose.yml) a utilizar:
    - Arquietecturas de **64 bits** (x64): `panubo/vsftpd`
    - Arquitecturas **ARM** (Raspberry): `pablokbs/panubo-vsftpd-arm`
- Modificar las **variables** de [docker-compose.yml](/docker-compose.yml) (marcadas con `<>`)
- Añadir el **volumen**: El volúmen deben estar enlazado con `/srv` y el **dueño** y los **permisos** de la carpeta deben ser los siguientes:
    ```bash
    sudo chown -R 1001:root <carpeta_volumen>
    sudo chmod -R 755 <carpeta_volumen>
    ```
- Ejecutar `docker compose up -d --build`
