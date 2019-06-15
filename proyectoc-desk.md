# C-DESK
## Herramienta HELP DESK

En primer lugar estos son los requisitos necesarios para la instalación de C-DESK.
![](imagenes/6.png)
![](imagenes/7.png)

Vaya a su administrador de IIS.

Seleccione su sitio web para implementar la aplicación.

Seleccione “deploy” y “Import application”.
![](imagenes/8.png)

El asistente de "Import Application Package" se abre y muestra el cuadro de diálogo "Seleccionar el paquete".

En el cuadro "Package path", busque y seleccione su archivo zip desde la ubicación donde descargó

El cuadro de diálogo "Select the Package" se parece a la siguiente imagen
![](imagenes/9.png)

Haga clic en "Next".

El cuadro de diálogo "Select the Contents of the Package" se muestra como se muestra en la siguiente imagen:
![](imagenes/10.png)

Haga clic en "Next".

El cuadro de diálogo "Enter Application Package Information" se muestra como se muestra en la siguiente imagen:
![](imagenes/11.png)

Mientras "Web Deploy" instala el paquete, se muestra el cuadro de diálogo "Installation Progress and Summary". El cuadro de diálogo muestra una barra de progreso durante el proceso de instalación. Cuando se completa el proceso, el cuadro de diálogo muestra un registro de lo que se hizo, como se muestra en la siguiente imagen:
![](ProyectoC-DESK/imagenes/12.png)

Clic derecho en C-Desk site y browse.
![](ProyectoC-DESK/imagenes/13.png)

![](ProyectoC-DESK/imagenes/14.png)

Vaya a su administrador de IIS y añada un sitio

Vaya a "IIS" y añada un sitio web. O si tiene instalado un despliegue web, puede importar directamente la aplicación
![](ProyectoC-DESK/imagenes/15.png)

Apunte la ruta física a la carpeta C-Desk y defina el Puerto. O el valor del encabezado de host para su aplicación cdesk.
De manera similar, agregue un nuevo sitio para Cdeskapp y señale la ruta física a la carpeta Cdeskapp. Use el puerto 80 y proporcione el nombre del host para que podamos acceder al host desde el exterior. Recuerde abrir el puerto 80 en su firewall y señalarlo al servidor. También recuerde agregar las entradas de DNS necesarias para el nombre de host en su configuración de DNS en el panel de alojamiento.
![](ProyectoC-DESK/imagenes/16.png)

Haga clic derecho en C-Desk y browse.
![](ProyectoC-DESK/imagenes/22.png)

Clic en Create Database.
![](ProyectoC-DESK/imagenes/23.png)

Proporcione detalles del servidor SQL y proporcione el nombre preferido de la base de datos. Y clic en "submit configuration settings".
![](ProyectoC-DESK/imagenes/24.png)
![](ProyectoC-DESK/imagenes/25.png)

Click en "Create Database".
![](ProyectoC-DESK/imagenes/26.png)

Después de la creación de la base de datos, debería obtener la página de estado del servicio.
![](ProyectoC-DESK/imagenes/27.png)

Coloque el nombre de usuario predeterminado ‘cd_admin’ y la contraseña ‘admin @ 123’.

Como esta es la primera vez que inicia sesión, obtendrá el asistente de configuración.
![](ProyectoC-DESK/imagenes/28.png)

Proporcionar detalles del servidor FTP. Esto se usa para la galería de fotos y es obligatorio. Si no tiene un servidor ftp configurado, puede configurar lo mismo en IIS. Necesitará esto si va a tener varias capas de aplicación instaladas en una ubicación diferente, luego asegúrese de que se pueda acceder al servidor FTP desde todas las ubicaciones. De lo contrario, si se trata de una sola capa de aplicación, puede tener un servidor FTP local.
![](ProyectoC-DESK/imagenes/29.png)

Dirección IP y configuración de dominio. Proporcione los rangos de IP para los usuarios que van a acceder a la base de conocimiento.
Si desea que los usuarios accedan a la base de conocimientos desde un recurso externo, proporcione IP como 0.0.0.0 y subred como 0.0.0.0 y envíe
![](ProyectoC-DESK/imagenes/31.png)

Proporcione el nombre de dominio de los identificadores de correo electrónico que pueden registrarse. Esta función se mantiene para que los empleados no se registren con sus ID de correo electrónico personales. Para los usuarios que no tienen acceso por correo electrónico desde la organización puede usar @nombre_dominio.local
![](ProyectoC-DESK/imagenes/32.png)

Por favor, proporcione la configuración del servidor SMTP aquí. También proporcione la configuración de URL para acceder a la aplicación C-desk. Esto se utiliza como un hipervínculo en los correos enviados por C-Desk. Déjelo desactivado si no desea que la aplicación envíe correos a los usuarios.
![](ProyectoC-DESK/imagenes/33.png)

Proporcionar acceso a su servidor de correo web. Si está utilizando Exchange, puede seleccionar el acceso web de Outlook. O si estás usando roundcube entonces puedes usar eso. También puede usar ambos si tiene ambos instalados en su organización y configura uno como predeterminado. A través de un usuario, se le permite dar el nombre de usuario y la contraseña de su buzón manualmente una vez que ingresa y puede seleccionar cuál de los dos está usando. Esto permite iniciar sesión automáticamente en el correo web desde la aplicación C-Desk.
![](ProyectoC-DESK/imagenes/34.png)

Esto es muy importante ya que los empleados pueden usar el mismo nombre de usuario y contraseña para acceder a esta aplicación. También puede colocar varias entradas si tiene un bosque con más de un controlador de dominio o dominios secundarios. Asegúrese de tener acceso a las rutas LDAP definidas aquí. El servidor IIS necesita el acceso a todos los servidores LDAP de su organización. Esto también ayuda al usuario a utilizar el proceso de registro.
![](ProyectoC-DESK/imagenes/35.png)

Cree la primera ubicación y la oficina / unidad de negocios en esa ubicación. Puede tener varias ubicaciones y varias oficinas / Unidades de negocio en cada ubicación. Esto se hace desde las rutas de solicitud de servicio según la ubicación del usuario. Así que si el usuario solicita un servicio en particular. Luego, la solicitud se envía a la persona asignada para esa categoría de servicio para esa ubicación.
![](ProyectoC-DESK/imagenes/36.png)

Aquí puedes crear una o más empresas. Debe tener al menos una empresa para iniciar el proceso de registro de usuarios.
![](ProyectoC-DESK/imagenes/37.png)

