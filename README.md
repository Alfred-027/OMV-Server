# Servidor openmediavault con Docker Compose para automatitazación de Plex Media Server

 En este repo se encuentra mi servidor personalizado basado en **[openmediavault](https://www.openmediavault.org/).**
 Aquí encontraras todos mis archivos de configuración y la manera en que estoy utilizando docker compose para integrar distintas herramientas en mi servidor casero.
 *Última version estable a la fecha de publicación de este repo: **7.0-Sandworm-Debian 12 Mar 2024.***
  
 ## Caracteristicas de mi hardware

- Tipo: Mini PC.
- CPU: Intel Alder Lake N100.
- RAM: 16 GB.
- SSD sistema: 512 GB NVME.
- Disco de datos: HDD 512 GB.

## Pasos para la instalación

### Prerrequisitos:

- Hardware compatible. Para información puedes visitar la web oficial: [Prerriquisites](https://docs.openmediavault.org/en/stable/prerequisites.html).
- Memoria flash USB (Pendrive) para usarlo como fuente de booteo para la instalación (mínimo 2GB).Considera que todos los datos de esta memoria serán borrados. En caso de que tu instalación sea disitnta como máquina virtual u otros, omitir.
- Acceso a internet para descargar la iso de openmediavault directamente desde la [web oficial](https://www.openmediavault.org/?page_id=77).
- Rufus, para crear un USB booteable para la instalación del sistema operativo. Puedes descargarlo desde su web oficial [aquí](https://rufus.ie/es/). Se recomienda la versión portable.

### Creación de USB booteable

Abrir rufus y conectar el USB stick. Seleccionar la ISO de openmediavault e iniciar la creación. A continuación una imagen de referencia: 

![rufus config](https://github.com/Alfred-027/OMV-Server/blob/master/assets/Rufus-OMV.png)

### Instalación de openmediavault

Seguir la documentación oficial [aquí](https://docs.openmediavault.org/en/stable/installation/index.html). Tambien les dejo un excelente tutorial que encontré del buen [Compucenter33](https://www.youtube.com/@compucenter33). Video de omv [aquí](https://www.youtube.com/watch?v=vySCnJ8TyCw).

**Aspectos importantes:**

- Durante la instalación, tu hardware debe contar con conectividad de red para una correcta configuración del acceso a la interfaz web. Esto puede configurarse mas adelante pero se recomienda esto para hacer la configuración mas sencilla. 
- Se debe configurar el orden de boot en tu sistema dependiendo del tipo de instalación, en este caso se selecciona el dispositivo de boot usb stick como primera opción de arranque para que inicie la instalación.
- Nombre de la máquina: Será el nombre del servidor para identificarlo dentro de tu red. Puede ser cualquiera de tu preferencia. 
- Nombre de dominio: Dependerá de tu propia instalación, en este caso va vacío. Por defecto el dominio sera local.
- Clave del super usuario: Esta será la clabe del usuario "root" en debian. Apúntala en un lugar seguro una vez la ingreses.
- Verificar el disco en donde se instalará el sistema operativo. Estos aparecen listados en la instalación con su modelo y espacio disponible.
- País de la réplica de debian: Es el repositorio oficial de Debian, debes configuar el mirror mas cercano a tu ubicación para una óptima descarga de paquetes. Verificar los mirrors oficiales en el sitio de debian https://www.debian.org/mirror/list.es.html.
- Información de proxy: Si tu red utiliza un proxy completar este campo, de lo contrario dejar en blanco.
- Una vez finalizado el proceso de instalación el sistema solicitará el reinicio. En este punto es necesario retirar el USB para evitar que inicie nuevamente el asistente de instalación.
 
## Configuraciones

Luego del arranque del sistema operativo, se mostrara la pantalla de login de debian solicitando el ingreso. En esta misma pantalla se indican el usuario y password por defecto del administador de la interfaz web "admin" y la password "openmediavault", ambos sin comillas. 

Tambien se muestra la direccion de red configurada por dhcp en la instalación. Esta nos servira para acceder a la interfaz web de configuración.

Para acceder al sistema base de debian se debe utilizar "root" y la contraseña de superusuario configurada en la instalación.

Como recomendación inicial, actualizar el sistema con los siguientes comandos: 

```
apt update Actualizar lista de paquetes actualizables
apt upgrade ejecutar actualzación
```
Para terminar la configuración vamos a seguir los siguientes pasos.

1. Acceder a la interfaz web segun la dirección asignada por tu router: "https://X.X.X.X:80".
2. Ingresar user y pass por defecto.
3. Configurar dashboard para tener distintos controles según nuestras preferencias. 
4. 
5. 
6. 
7. 
8. 
9. 

## Instalación de plugin OMV-Extras y puesta en marcha XXXXX


