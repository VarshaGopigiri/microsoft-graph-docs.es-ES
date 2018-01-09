# <a name="get-started-with-microsoft-graph-in-a-python-app"></a>Introducción a Microsoft Graph en una aplicación de Python 

En este artículo, se describen las tareas necesarias para obtener un token de acceso desde Azure AD y llamar a Microsoft Graph. Le muestra los pasos para [Enviar un correo electrónico a través de Microsoft Graph desde Python]((https://github.com/microsoftgraph/python-sample-send-mail)) y explica los conceptos principales que implementará para usar la API de Microsoft Graph. El artículo describe cómo obtener acceso a Microsoft Graph mediante llamadas de REST directas.

![Enviar formulario de correo electrónico](https://raw.githubusercontent.com/microsoftgraph/python-sample-send-mail/master/static/images/sendmail.png)

## <a name="choosing-an-authentication-library"></a>Selección de una biblioteca de autenticación

Para realizar llamadas a Microsoft Graph, la aplicación debe obtener un token de acceso válido de Azure Active Directory (Azure AD), el servicio de identidad de nube de Microsoft, y el token se debe pasar de un encabezado HTTP con cada llamada a la API de REST de Microsoft Graph. El método de autenticación de Graph se basa en los estándares de OAuth 2.0 y Open ID Connect, por lo que existen muchas [bibliotecas de autenticación]((https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-libraries)) de las que puede elegir para implementar la autenticación en la aplicación.

En el ejemplo siguiente se usa la biblioteca [Flask-OAuthlib]((https://flask-oauthlib.readthedocs.io/en/latest/)) para implementar el flujo de trabajo [Concesión de código de autorización](https://tools.ietf.org/html/rfc6749#section-4.1) de OAuth 2.0 , que es el flujo de trabajo de autenticación recomendado para las aplicaciones web escritas en Python. Para obtener información sobre otras opciones de autenticación, vea [Ejemplos de autenticación de Python para Microsoft Graph]((https://github.com/microsoftgraph/python-sample-auth)).

## <a name="installing-and-running-the-send-mail-sample"></a>Instalación y ejecución del ejemplo de envío de correos electrónicos

Para instalar y configurar la aplicación de ejemplo, siga las instrucciones de [Instalar los ejemplos de REST de Python]((https://github.com/microsoftgraph/python-sample-auth)/blob/master/installation.md). Para el ejemplo de envío de correos electrónicos que se muestra a continuación, use este comando para clonar el repo:

```git clone https://github.com/microsoftgraph/python-sample-send-mail.git```

Al registrar la aplicación como se explica en las [instrucciones de instalación]((https://github.com/microsoftgraph/python-sample-auth)/blob/master/installation.md), asegúrese de incluir los permisos **User.Read** y **Mail.Send**, que son necesarios para en este ejemplo.

Después de completar la instalación o configuración, puede ejecutar la aplicación de ejemplo siguiendo las instrucciones de [ejecutar el ejemplo]((https://github.com/microsoftgraph/python-sample-send-mail)#running-the-sample).

## <a name="code-walkthrough"></a>Tutorial de código

La siguiente es una descripción general del [código fuente]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py) para la aplicación de ejemplo.

Las primeras líneas de código son las [importaciones]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L4-L32) de los paquetes y módulos de Python usados en este ejemplo:

* El módulo **base64** de la biblioteca estándar se usa para codificar los datos adjuntos de correo electrónico.
* El módulo **mimetypes** se usa para determinar el tipo MIME para archivos adjuntos.
* El módulo **os** proporciona funciones comunes del sistema de archivos.
* El módulo **pprint** de la biblioteca estándar se usa para imprimir con sangría los mensajes de error que devuelve Graph. (Por ejemplo, si intenta enviar un mensaje de correo electrónico a una dirección no válida).
* El módulo **uuid** de la biblioteca estándar se usa para generar una cadena aleatoria de 36 caracteres para identificar exclusivamente cada solicitud de gráfico. Esto puede resultar útil para propósitos de depuración.
* El paquete **Flask** es el marco de la web para el ejemplo.
* La clase **OAuth** de **flask_oauthlib.client** es el empaquetador de la aplicación Flask que implementa el flujo de trabajo de autenticación de OAuth 2.0.
* El módulo **config** contiene la configuración de registro de la aplicación, como se ha configurado en el proceso de instalación anterior.

Después, se [crea una aplicación de Flask]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L15-L17) y el [objeto de cliente de Graph]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L19-L28), denominado **MSGRAPH**.

Después de estos pasos de configuración inicial, se usan tres funciones de controlador de ruta de Flask que implementan el flujo de trabajo de autenticación: [homepage()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L30-L33), [login()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L35-L39) y [authorized()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L41-L48). Para más información sobre el flujo de trabajo de autenticación, vea la sección [Arquitectura de ejemplo]((https://github.com/microsoftgraph/python-sample-auth)#sample-architecture) del repo de autenticación de Phyton.

El controlador de ruta siguiente, [mailform()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L50-L83), es el formulario donde se especifican los destinatarios, el asunto y el cuerpo del correo electrónico. Tenga en cuenta que, en esta función, también se incluyen nuestras primeras llamadas a Graph, incluida la recuperación del perfil de usuario y la foto de perfil, la carga de la foto en OneDrive y la creación de un vínculo para compartir. Los datos se [pasan a la plantilla mailform.html]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L77-L83), donde se puede editar el destinatario, el asunto y el cuerpo antes de enviar el mensaje. 

La siguiente función es [send_mail()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L85-L107), que envía el correo electrónico y muestra la respuesta de la API de Graph. Usa una función auxiliar sendmail(), y pasa a los parámetros de cadena de consulta que se publicaron desde el formulario:

```python
response = sendmail(client=MSGRAPH,
                    subject=flask.request.args['subject'],
                    recipients=flask.request.args['email'].split(';'),
                    body=flask.request.args['body'],
                    attachments=[profile_pic])
```

La instancia de cliente Flask-OAuthlib (```MSGRAPH```) usa la función [get_token()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L109-L123) para obtener un token de acceso cuando al realizar llamadas a Graph. Se pasa el token de acceso en un encabezado HTTP denominado **Autorización**, pero no es necesario hacer esto en el código. Solo puede realizar llamadas a Graph con métodos de verbo HTTP del cliente (por ejemplo, get() o post()) y la instancia de cliente sabrá cómo llamar a ```get_token()``` para obtener un token, porque la función está [decorada]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L109-L109) con ```tokengetter```.

El resto del ejemplo son funciones auxiliares que simplifican actividades comunes de Graph:

* [request_headers()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L114-L123) devuelve un diccionario de encabezados HTTP para que se envíen a cada llamada a Graph.
* [profile_photo()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L125-L154) devuelve la foto de perfil del usuario y, de forma opcional guarda una copia en un archivo local.
* [sendmail()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L156-L202) envía un mensaje a el punto de conexión ```me/microsoft.graph.sendMail```.
* [sharing_link()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L204-L221) crea un vínculo para compartir de un elemento especificado en OneDrive.
* [upload_file()]((https://github.com/microsoftgraph/python-sample-send-mail)/blob/master/sample.py#L223-L255) carga un archivo en OneDrive.

Puede que estas funciones auxiliares le resulten útiles en otras aplicaciones.

## <a name="other-python-rest-samples"></a>Otros ejemplos de REST de Python

Estos son otros ejemplos de Python donde se demuestra cómo trabajar con diferentes aspectos de Microsoft Graph:

* [Ejemplos de autenticación de Python para Microsoft Graph]((https://github.com/microsoftgraph/python-sample-auth))
* [Trabajar con respuestas de Microsoft Graph paginadas en Python]((https://github.com/microsoftgraph/python-sample-pagination))
* [Trabajar con extensiones abiertas de Graph en Python]((https://github.com/microsoftgraph/python-sample-open-extensions))

Si hay un ejemplo concreto que quiera ver, háganoslo saber al [enviar un problema]((https://github.com/microsoftgraph/python-sample-auth)/issues). Estamos muy interesados en sus comentarios sobre cualquier escenario de Microsoft Graph que desee compilar en Python.

La API de Microsoft Graph es una interfaz unificadora y muy avanzada que permite trabajar con todos los tipos de datos de Microsoft. Consulte la [documentación de desarrollador]((https://developer.microsoft.com/es-ES/graph/docs/concepts/overview)) o el [Probador de Graph]((https://developer.microsoft.com/es-ES/graph/graph-explorer)) para explorar qué más puede realizar con Microsoft Graph.
