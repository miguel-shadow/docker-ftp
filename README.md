# 1. FTP
Permite levantar un servidor FTP rápidamente con Docker

# 2. Instalación
- Seleccionar una imagen en [docker-compose.yml](/docker-compose.yml):
    - Arquietecturas de **64 bits** (x64): `panubo/vsftpd`
    - Arquitecturas **ARM** (Raspberry): `pablokbs/panubo-vsftpd-arm`
- Modificar las variables de [docker-compose.yml](/docker-compose.yml) (marcadas con `<>`)
- Ejecutar `docker compose up -d --build`
