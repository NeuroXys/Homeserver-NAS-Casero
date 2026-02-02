<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=30&pause=1000&center=true&vCenter=true&repeat=false&random=true&width=435&lines=Estado+del+arte" alt="Typing SVG" /></a>

La creciente demanda de soluciones de almacenamiento, gestión de medios digitales y virtualización accesibles ha impulsado el desarrollo de servidores domésticos (homeservers). Estas infraestructuras, gestionadas en el ámbito personal o familiar, permiten centralizar servicios digitales como la transferencia de archivos, gestión de máquinas virtuales, servidores multimedia y bibliotecas digitales, manteniendo la privacidad, la eficiencia y la autonomía tecnológica del usuario.

En este contexto, plataformas como Proxmox VE y TrueNAS destacan por ser opciones "gratuitas" que facilitan la virtualización y el almacenamiento en red, respectivamente. En el presente estado del arte se analizarán herramientas representativas para la implementación de cada servicio, optando por Proxmox VE como sistema operativo anfitrión, dada su flexibilidad y soporte para contenedores (LXC) y máquinas virtuales (KVM).

# 2. Sistema Operativo: Proxmox Virtual Environment (VE)

Proxmox VE es una distribución Linux basada en Debian que permite la gestión de servidores mediante una interfaz web y herramientas CLI. Soporta virtualización completa a través de KVM y contenedores mediante LXC, facilitando así el despliegue de múltiples servicios sobre una sola máquina física.

Su arquitectura de clúster y su sistema de almacenamiento definido por software permiten tanto el uso doméstico como semiprofesional, convirtiéndolo en una opción ideal para proyectos personales de infraestructura de servicios digitales (Proxmox Server Solutions GmbH, 2024).

# 3. Servicios Fundamentales del Homeserver
## 3.1 Transferencia de Archivos

Para la transferencia y gestión de archivos dentro de la red local y desde el exterior, soluciones como Samba (para redes Windows/Linux) o Nextcloud permiten compartir documentos y sincronizar carpetas de forma segura.

* Samba: facilita el uso compartido de carpetas mediante el protocolo SMB/CIFS, con permisos personalizables.

* Nextcloud: proporciona una nube privada con funcionalidades de sincronización, edición en línea y colaboración (Nextcloud GmbH, 2023).

## 3.2 Máquinas Virtuales

El entorno de Proxmox permite la creación de máquinas virtuales completas con distintos sistemas operativos, desde distribuciones Linux livianas hasta servidores Windows. Esto facilita la separación lógica de servicios, pruebas de laboratorio o la emulación de entornos de producción.

Además, mediante VirtIO drivers y snapshots incrementales, se optimiza el rendimiento y la seguridad del entorno virtualizado.

## 3.3 Multimedia

Para la gestión y distribución de contenido multimedia (música, películas, fotografías), destacan plataformas como:

* Jellyfin: servidor multimedia de código abierto que permite la transmisión y organización de contenidos. Compatible con DLNA y clientes móviles.

* Plex o Emby: opciones con mayor integración multiplataforma, aunque con licencias más restrictivas.

Jellyfin es especialmente adecuado para servidores domésticos por ofrecer una mayor privacidad al usuario y no tomar datos de telemetría.

## 3.4 Biblioteca Digital

La implementación de una biblioteca digital puede realizarse mediante el despliegue de Calibre Web, una interfaz ligera basada en el sistema de gestión de ebooks Calibre, que permite visualizar, gestionar y descargar libros digitales desde un navegador.

* Permite control de acceso por usuarios

* Soporta formatos EPUB, PDF, MOBI, entre otros

* Integración con lectores Kindle mediante OPDS

# 4. Consideraciones de Seguridad y Backup

Dado que un homeserver almacena y transmite información sensible, resulta imprescindible configurar copias de seguridad automatizadas (p. ej. con BorgBackup o Restic), así como establecer mecanismos de autenticación segura (SSH, 2FA) y aislamiento de servicios por contenedor o máquina virtual.

La gestión de puertos, el uso de HTTPS mediante certificados Let's Encrypt y el monitoreo con herramientas como Grafana y Prometheus son componentes recomendables para un servidor doméstico estable y seguro.

<details>
<summary># Bibliografía</summary>

* Proxmox VE Documentation. (2024). https://pve.proxmox.com/pve-docs/

* Nextcloud GmbH. (2023). Nextcloud Server Administration Manual. https://docs.nextcloud.com/

* Jellyfin Project. (2023). Jellyfin Docs. https://jellyfin.org/docs/

* Calibre Web Contributors. (2024). Calibre Web GitHub Repository. https://github.com/janeczku/calibre-web

* Samba Team. (2023). Samba Project Documentation. https://www.samba.org/samba/docs/

<details>
