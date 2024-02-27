# TallerFebrero2024
## Playbook de Actualización de Paquetes

Este playbook de Ansible se utiliza para actualizar los paquetes del sistema en servidores Linux. Se ejecutará en servidores basados en Red Hat (como Rocky Linux) y Debian (como Ubuntu). El playbook actualizará todos los paquetes del sistema a su última versión disponible.

## Tareas:
Actualiza los paquetes en los servidores basados en Red Hat utilizando yum.
Actualiza los paquetes en los servidores basados en Debian utilizando apt.
## Handlers:
Reinicia los servidores si es necesario después de la actualización.

## Uso

1. Clona este repositorio en tu máquina local:

   git clone <URL_del_repositorio>
   Asegúrate de tener Ansible instalado en tu máquina local.
   Edita el archivo de inventario hosts para incluir las direcciones IP o nombres de host de tus servidores Linux.
   Ejecuta el playbook con el siguiente comando:
   ```bash
    ansible-playbook -i ansible/hosts ansible/playbook.yml
    ```
## Personalización

- Si necesitas modificar el comportamiento del playbook, puedes editar el archivo `ansible/playbook.yml`.

## Playbook de Instalación de OpenJDK y Servidor Apache Tomcat

Este playbook de Ansible automatiza la instalación y configuración de Apache Tomcat en servidores Ubuntu y Rocky Linux.

## Requisitos previos

- Ansible debe estar instalado en la máquina desde la cual ejecutarás el playbook.
- Tener acceso SSH a los servidores Ubuntu y Rocky Linux donde deseas instalar Tomcat.
- Asegúrate de que los servidores tengan conectividad a internet para descargar paquetes y archivos necesarios.

## Taras:

- Instala OpenJDK 8 en el servidor.
- Crea el directorio de instalación de Tomcat.
- Descarga e instala Tomcat 8 desde el archivo binario.
- Configura un archivo de servicio systemd para administrar el inicio y el apagado de Tomcat.
- Descarga una aplicación de muestra (WAR file) y la despliega en Tomcat.
- Habilita el servicio Tomcat para que se inicie automáticamente en el arranque del sistema.
- Configura el cortafuegos para permitir el tráfico en los puertos 80, 443 y 8080

## Uso


1. Ejecuta el playbook desde el directorio raíz del repositorio:

    ```bash
    ansible-playbook -i ansible/hosts ansible/playbook.yml
    ```

## Personalización

- Si necesitas modificar el comportamiento del playbook, puedes editar el archivo `ansible/playbook.yml`.

## Playbook  configuracion de Proxy Reverso Apache2
Este playbook de Ansible se utiliza para configurar un servidor Ubuntu con Apache2 como un proxy reverso para acceder a una aplicación Java en otro servidor. El playbook realiza las siguientes tareas:
- Instala el cortafuegos UFW y habilita los puertos 80 y 22.
- Instala Apache2 en el servidor Ubuntu.
- Configura un archivo de sitio de proxy reverso en Apache2.
- Habilita el modulo proxy_http en Apache2.
- Reinicia el servicio Apache2 para aplicar los cambios.

## Uso

1. Ejecuta el playbook desde el directorio raíz del repositorio:

    ```bash
    ansible-playbook -i ansible/hosts ansible/playbook.yml
    ```
## Contribución

Si encuentras errores o mejoras para este playbook, siéntete libre de contribuir creando pull requests.


