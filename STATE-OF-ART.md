# Este estado del arte es una documentación inicial sujeta a cambios, dependiendo del software final utilizado.

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

# Work in Progress

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=30&pause=1000&center=true&vCenter=true&repeat=false&random=true&width=435&lines=State+of+art" alt="Typing SVG" /></a>

The growing demand for accessible solutions for storage, digital media management, and virtualization has driven the development of home servers. These infrastructures, managed within a personal or household setting, enable the centralization of digital services such as file transfer, virtual machine hosting, multimedia streaming, and digital library access—ensuring user privacy, operational efficiency, and technological self-reliance.

Within this context, platforms such as Proxmox VE and TrueNAS stand out for their focus on virtualization and network-attached storage, respectively. This state of the art examines the most relevant tools for implementing each core service, selecting Proxmox VE as the host operating system due to its flexibility and support for both containers (LXC) and virtual machines (KVM).

# 2. Operating System: Proxmox Virtual Environment (VE)

Proxmox VE is a Debian-based Linux distribution that enables server management through both a web interface and CLI tools. It supports full virtualization via KVM and containerization through LXC, allowing the deployment of multiple services on a single physical machine.

Its cluster-based architecture and software-defined storage system make it suitable for both home and semi-professional environments, positioning it as an ideal choice for personal infrastructure projects (Proxmox Server Solutions GmbH, 2024).

# 3. Core Home Server Services
## 3.1 File Transfer

For file sharing and transfer across the local network and remotely, tools like Samba (for Windows/Linux interoperability) and Nextcloud enable secure document sharing and folder synchronization.

* Samba facilitates network folder sharing using the SMB/CIFS protocol, with customizable permissions.

* Nextcloud offers a private cloud solution with synchronization, online editing, and collaboration features (Nextcloud GmbH, 2023).

## 3.2 Virtual Machines

Proxmox’s virtualization environment allows the creation of full-featured virtual machines running various operating systems, from lightweight Linux distributions to Windows servers. This enables logical service separation, testing environments, or production emulation.

Using VirtIO drivers and incremental snapshots, Proxmox optimizes performance and enhances security across its virtual machines.

## 3.3 Multimedia

For managing and streaming multimedia content such as music, movies, and photos, platforms like:

* Jellyfin: an open-source media server for organizing and streaming content. It supports DLNA and mobile clients.

* Plex and Emby: alternatives with broader platform integration but more restrictive licensing models.

Jellyfin is particularly suitable for home use due to its focus on privacy and its telemetry-free philosophy.

## 3.4 Digital Library

A digital library can be implemented using Calibre Web, a lightweight interface built on top of the Calibre ebook management system. It allows browsing, managing, and downloading ebooks from a web browser.

User access control

Supports formats such as EPUB, PDF, MOBI

# 4. Security and Backup Considerations

Given that a home server stores and transmits potentially sensitive information, it is essential to implement automated backup mechanisms (e.g., using BorgBackup or Restic), along with secure authentication methods (SSH keys, two-factor authentication) and service isolation through containers or virtual machines.

Proper port management, HTTPS implementation via Let's Encrypt certificates, and system monitoring using tools like Grafana and Prometheus are also recommended practices to ensure a stable and secure home server environment.

# Bibliografía

<details>
<summary>Ver</summary>

* Proxmox VE Documentation. (2024). https://pve.proxmox.com/pve-docs/

* Nextcloud GmbH. (2023). Nextcloud Server Administration Manual. https://docs.nextcloud.com/

* Jellyfin Project. (2023). Jellyfin Docs. https://jellyfin.org/docs/

* Calibre Web Contributors. (2024). Calibre Web GitHub Repository. https://github.com/janeczku/calibre-web

* Samba Team. (2023). Samba Project Documentation. https://www.samba.org/samba/docs/

<details>
