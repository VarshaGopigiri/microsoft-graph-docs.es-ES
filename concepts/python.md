# <a name="get-started-with-microsoft-graph-in-a-python-app"></a>Introducción a Microsoft Graph en una aplicación de Python 

En este artículo, se describen las tareas necesarias para obtener un token de acceso desde Azure AD y llamar a Microsoft Graph. Le muestra los pasos para [Enviar un correo electrónico a través de Microsoft Graph desde Python](https://github.com/microsoftgraph/python-sample-send-mail) y explica los conceptos principales que implementará para usar la API de Microsoft Graph. El artículo describe cómo obtener acceso a Microsoft Graph mediante llamadas de REST directas.

![Enviar formulario de correo electrónico](https://raw.githubusercontent.com/microsoftgraph/python-sample-send-mail/master/static/images/sendmail.png)

## <a name="choosing-an-authentication-library"></a>Selección de una biblioteca de autenticación

Para realizar llamadas a Microsoft Graph, la aplicación debe obtener un token de acceso válido de Azure Active Directory (Azure AD), el servicio de identidad de nube de Microsoft, y el token se debe pasar de un encabezado HTTP con cada llamada a la API de REST de Microsoft Graph. El método de autenticación de Graph se basa en los estándares de OAuth 2.0 y Open ID Connect, por lo que existen muchas [bibliotecas de autenticación](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-libraries) de las que puede elegir para implementar la autenticación en la aplicación.

En el ejemplo siguiente se usa la biblioteca [Flask-OAuthlib](https://flask-oauthlib.readthedocs.io/en/latest/) para implementar el flujo de trabajo [Concesión de código de autorización](https://tools.ietf.org/html/rfc6749#section-4.1) de OAuth 2.0 , que es el flujo de trabajo de autenticación recomendado para las aplicaciones web escritas en Python. Para obtener información sobre otras opciones de autenticación, vea [Ejemplos de autenticación de Python para Microsoft Graph](https://github.com/microsoftgraph/python-sample-auth).

## <a name="installing-and-running-the-send-mail-sample"></a>Instalación y ejecución del ejemplo de envío de correos electrónicos

Para instalar y configurar la aplicación de ejemplo, siga las instrucciones de [Instalar los ejemplos de REST de Python](https://github.com/microsoftgraph/python-sample-auth/blob/master/installation.md). Para el ejemplo de envío de correos electrónicos que se muestra a continuación, use este comando para clonar el repo:

    ```git clone https://github.com/microsoftgraph/python-sample-send-mail.git```

Al registrar la aplicación como se explica en las [instrucciones de instalación](https://github.com/microsoftgraph/python-sample-auth/blob/master/installation.md), asegúrese de incluir los permisos **User.Read** y **Mail.Send**, que son necesarios para en este ejemplo.

Después de completar la instalación o configuración, puede ejecutar la aplicación de ejemplo siguiendo las instrucciones de [ejecutar el ejemplo](https://github.com/microsoftgraph/python-sample-send-mail#running-the-sample).

## <a name="code-walkthrough"></a>Tutorial de código

La siguiente es una descripción general del [código fuente](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py) para la aplicación de ejemplo.

Las primeras líneas de código son las [importaciones](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L4-L11) para los paquetes y módulos de Python utilizados en este ejemplo:

* El módulo **base64** de la biblioteca estándar se usa para los datos adjuntos de correo electrónico de codificación.
* El módulo **pprint** de la biblioteca estándar se usa para imprimir con sangría los mensajes de error que devuelve Graph. (Por ejemplo, si intenta enviar un mensaje de correo electrónico a una dirección no válida).
* El módulo **uuid** de la biblioteca estándar se usa para generar una cadena aleatoria de 36 caracteres para identificar exclusivamente cada solicitud de gráfico. Esto puede resultar útil para propósitos de depuración.
* El paquete **Flask** es el marco de la web para el ejemplo.
* La clase **OAuth** de **flask_oauthlib.client** es el empaquetador de la aplicación Flask que implementa el flujo de trabajo de autenticación de OAuth 2.0.
* El módulo **config** contiene la configuración de registro de la aplicación, como se ha configurado en el proceso de instalación anterior.

Después, se [crea una aplicación Flask](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L13-L15) y, a continuación, se crea el [objeto de cliente de Graph](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L17-L26), denominado **MSGRAPH**.

Después de estos pasos de instalación iniciales, vienen tres funciones de identificador de ruta Flask que implementan el flujo de trabajo de autenticación: [homepage()](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L28-L31), [login()](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L33-L37), and [authorized()](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L39-L46). Para más información sobre el flujo de trabajo de autenticación, vea la sección [Arquitectura de ejemplo](https://github.com/microsoftgraph/python-sample-auth#sample-architecture) del repo de autenticación de Phyton.

El controlador de ruta siguiente, [mailform()](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L48-L54), es el formulario donde especificar los destinatarios, asunto y cuerpo de correo electrónico. Tenga en cuenta que esta función también incluye la primera llamada a Graph: [recuperar el perfil de usuario](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L51-L51) para obtener la dirección de correo electrónico y el nombre actual del usuario que se muestra, que se [pasan a la plantilla mailform.html](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L52-L54).

La siguiente es la función [send_mail()](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L56-L73), que envía el correo electrónico y muestra la respuesta de la API de Graph. Usa una función auxiliar sendmail(), y pasa a los parámetros de cadena de consulta que se publicaron desde el formulario:

```python
response = sendmail(MSGRAPH,
                    subject=flask.request.args['subject'],
                    recipients=flask.request.args['email'].split(';'),
                    html=flask.request.args['body'])
```

La función [get_token()](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L75-L78) se usa por la instancia de cliente Flask-OAuthlib (```MSGRAPH```) para obtener un token de acceso cuando realice llamadas a Graph. Se pasa el token de acceso en un encabezado HTTP denominado **Autorización**, pero no es necesario hacer esto en el código. Solo puede realizar llamadas a Graph mediante métodos de verbo HTTP del cliente (por ejemplo, get() o post()) y la instancia de cliente sabrá cómo llamar a ```get_token()``` para obtener un token, porque la función está [decorada](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L75-L75) con ```tokengetter```.

A continuación viene [request_headers()](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L80-L85), que devuelve un diccionario de encabezados HTTP que se envían con cada llamada a Graph.

Por último tenemos [sendmail()](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L87-L129), la función auxiliar para enviar un correo electrónico. Envía un mensaje con el punto de conexión ```me/microsoft.graph.sendMail``` en la API de Microsoft Graph, y puede volver a usar esta función en su propio código cuando sea necesario enviar un correo electrónico a través de Microsoft Graph. Consulte la [docstring](https://github.com/microsoftgraph/python-sample-send-mail/blob/master/sample.py#L88-L97) para obtener información sobre cómo se llama a esta función.

## <a name="other-python-rest-samples"></a>Otros ejemplos de REST de Python

Además del ejemplo explicado anteriormente, los ejemplos siguientes muestran cómo trabajar con otras características de Microsoft Graph desde Phyton:

* [Ejemplos de autenticación de Python para Microsoft Graph](https://github.com/microsoftgraph/python-sample-auth)
* [Trabajar con respuestas de Microsoft Graph paginadas en Python](https://github.com/microsoftgraph/python-sample-pagination)
* [Trabajar con extensiones abiertas de Graph en Python](https://github.com/microsoftgraph/python-sample-open-extensions)

Si hay un ejemplo concreto que quiera ver, háganoslo saber al [enviar un problema](https://github.com/microsoftgraph/python-sample-auth/issues). Estamos muy interesados en sus comentarios sobre cualquier escenario de Microsoft Graph que desee compilar en Python.

La API de Microsoft Graph es una interfaz unificadora y muy avanzada que permite trabajar con todos los tipos de datos de Microsoft. Consulte la [documentación de desarrollador](https://developer.microsoft.com/es-ES/graph/docs/concepts/overview) o el [Probador de Graph](https://developer.microsoft.com/es-ES/graph/graph-explorer) para explorar qué más puede realizar con Microsoft Graph.
