---

copyright:

  years: 1994, 2019

lastupdated: "2019-05-16"

keywords: master user, Password tracking, Select Devices, managing passwords, password tracking tool 

subcollection: customer-portal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Gestión de contraseñas
{: #cp_manpws}

Si es un usuario maestro o el propietario de una cuenta, puede habilitar el seguimiento de contraseñas y configurar una contraseña para un acceso puntual a la cuenta. El seguimiento de contraseñas permite a los usuarios almacenar datos de contraseñas de software para dispositivos y su software asociado.
{:shortdesc}

## Habilitación del seguimiento de contraseñas
{: #cp_enabpwtrak}

El portal de clientes tiene una herramienta opcional de [seguimiento de contraseñas ![Icono de enlace externo](../icons/launch-glyph.svg)](https://control.softlayer.com/devices/passwords){:new_window} para cada cuenta. Los usuarios pueden recuperar sus nombres de usuario y contraseñas con la herramienta si se pierde o se olvida la información.

Los equipos de soporte también utilizan el seguimiento de contraseñas si el acceso remoto a un sistema es obligatorio. El servicio de soporte utiliza los nombres de usuario y contraseñas solo cuando sea necesario y tiene autorización de la resolución de incidencias.

El seguimiento de contraseñas dentro del portal de clientes es opcional. Cualquier usuario con los permisos adecuados puede ver todas las contraseñas que almacena esta herramienta. La información de usuarios y de contraseñas se sigue manualmente, por lo que no se sincroniza automáticamente con un dispositivo ni con su software. Por lo tanto, asegúrese de actualizar la herramienta de seguimiento de contraseñas a la vez que actualiza los usuarios y las contraseñas en los dispositivos y el software. Efectúe los pasos siguientes para añadir un usuario a la herramienta de seguimiento de contraseñas.

1. Acceda al portal de clientes utilizando sus credenciales exclusivas.
2. Seleccione **Dispositivos** > **Gestionar** > **Contraseñas** en el menú.
3. Pulse el separador **Añadir credenciales**.
4. Seleccione el **Nombre de dispositivo** con el que está asociado el usuario en la lista desplegable **Nombre de dispositivo**.
5. Seleccione el **Software** con el que está asociado el usuario en la lista **Software**.

  El software que se lista se proporciona mediante la infraestructura de {{site.data.keyword.BluSoftlayer_notm}} mediante suscripciones de pago o gratuitas. Ningún software de terceros que se instalara manualmente en el dispositivo está disponible para su seguimiento a través del portal de clientes.
  {: tip}

6. Escriba el nombre de usuario y la contraseña para el software en los campos correspondientes.
8. Opcionalmente, puede escribir cualquier comentario aplicable en el campo **Notas**.
9. Pulse **Añadir credenciales**.

Después de añadir el usuario a la herramienta de seguimiento de contraseñas, la información se almacena en la herramienta hasta que se suprime manualmente. Todas las combinaciones de nombre de usuario y contraseña se almacenan en función del nombre de dispositivo de forma predeterminada. Las entradas se visualizan alfabéticamente por nombre de dispositivo, y luego por nombre de usuario.

### Filtrado de información en la herramienta de seguimiento de contraseñas
{: #cp_tracktool}

Para ver, editar o suprimir la información de usuario de la herramienta de seguimiento de contraseñas, puede filtrar para localizar rápidamente un usuario. Filtrar para encontrar un usuario es útil cuando la lista de usuarios abarque varias filas o páginas. Utilice los pasos siguientes para filtrar por dispositivo, software o usuario en la herramienta de rastreo de contraseñas.

1. Acceda al portal de clientes utilizando sus credenciales exclusivas.
2. Seleccione **Dispositivos** > **Gestionar** > **Contraseñas** en el menú.
3. Pulse el separador **Filtro**.
4. Seleccione o especifique el nombre de dispositivo, software, o el nombre de usuario en los campos correspondientes.
5. Pulse **Filtro**.

Puede seleccionar la información de usuario para ver, editar o eliminar.

### Edición de la información de usuario en la herramienta de seguimiento de contraseñas
{: #cp_editusinfo}

Tras añadir un usuario a la herramienta de seguimiento de contraseñas, puede editar los detalles asociados con el usuario o la contraseña. Efectúe los pasos siguientes para editar información para un usuario en la herramienta de seguimiento de contraseñas.

1. Acceda al portal de clientes utilizando sus credenciales exclusivas.
2. Seleccione **Dispositivos** > **Gestionar** > **Contraseñas** en el menú.
3. Localice la combinación de dispositivo-usuario en la herramienta. Utilice la característica de filtro para localizar rápidamente un usuario.
4. Pulse en cualquier lugar de la fila para abrir la vista de detalles de usuario.
5. Actualice los campos **Nombre de usuario** o **Contraseña** según sea necesario.
6. Pulse **Actualizar** para guardar los cambios.

Después de editar un usuario o una contraseña en la herramienta de seguimiento de contraseñas, la información se actualiza inmediatamente.

## Configuración de una cuenta para el acceso mediante contraseña única
{: #cp_one-time}

Antes de poder configurar la cuenta, primero debe configurar la aplicación "Acceso VIP" de Verisign. Si Acceso VIP no está configurado, descargue en primer lugar la aplicación:
* [https://m.vip.symantec.com/home.v ![Icono de enlace externo](../icons/launch-glyph.svg)](https://m.vip.symantec.com/home.v){:new_window}


A continuación, realice los pasos siguientes:
1. Abra la aplicación. Busque el ID de credenciales y su contraseña única actual. Puede ignorar la contraseña inicialmente, pero necesita el ID de credenciales para el portal, por lo que mantenga la aplicación abierta.
2. Inicie sesión en el portal de clientes como el usuario para el que desea configurar la contraseña única.
3. Pulse **Cuenta** > **Usuarios** > **Acciones** > **Añadir autenticación externa**.
4. Seleccione el tipo de autenticación para añadir. Si está utilizando la aplicación Verisign, elija **Symantec Identity Protection**.
5. Escriba el ID de credencial desde el paso 1 y pulse **Continuar**.
6. Complete el proceso de pedido y su opción de seguridad adicional se aplicará automáticamente en pocos minutos.
7. Tras varios minutos, seleccione **Cuenta** > **Usuarios** desde la barra de navegación y seleccione el usuario para el que ha configurado la contraseña única.
8. Pulse el enlace **Actualizar credencial** debajo de la sección **Symantec Validation Settings**.
9. Seleccione **habilitado** para el **Estado de credencial** y pulse **Actualizar credencial**.
10. Una vez que se procese correctamente la opción de seguridad adicional, podrá iniciar sesión en el portal de clientes como de costumbre. Después de enviar su nombre de usuario y contraseña, se le solicitará que especifique un código de seguridad.
11. Abra la aplicación Verisign Identity Protection en el dispositivo que prefiera y proporcione el código que se muestra para iniciar sesión.

Guarde el ID de credenciales de Verisign Identity Protection original en una ubicación segura para referencia futura. Sin él, no podrá acceder al portal.

## Restablecimiento de su contraseña
{: #cp_reset-your-password}

La forma de restablecer la contraseña depende de si utiliza un IBMid para autenticarse al iniciar una sesión en su cuenta.  

### Restablecimiento de la contraseña de una cuenta de IBMid
{: #cp_reset}

Si utiliza IBMid para la autenticación, para restablecer o recuperar la contraseña, vaya a su perfil de IBMid y siga las instrucciones de la sección **Iniciar sesión**.

### Restablecimiento de la contraseña de una cuenta de SoftLayer
{: #cp_reset-sl}

Si no utiliza un IBMid para la autenticación de cuenta, siga estos pasos:

1. Pulse el enlace de contraseña perdida en la página de inicio de sesión del [portal de clientes ![Icono de enlace externo](../icons/launch-glyph.svg)](https://control.softlayer.com/){:new_window}.
2. Cuando se le solicite, introduzca su nombre de usuario actual.
3. Consulte su correo electrónico para ver si hay una nota con un enlace para restablecer la contraseña. Este enlace es válido durante veinticuatro horas.
4. Seleccione y responda tres preguntas de seguridad.

Tiene 5 intentos para responder a las preguntas de seguridad. Si realiza más de 5 intentos, el formulario de restablecimiento de contraseña se bloquea durante 15 minutos antes de que pueda intentarlo de nuevo.

Para obtener información sobre cómo trabajar con contraseñas de VPN, consulte [Actualizar la contraseña de VPN de un usuario](/docs/infrastructure/iaas-vpn?topic=VPN-update-users-vpn-password#update-users-vpn-password).
{: tip}
