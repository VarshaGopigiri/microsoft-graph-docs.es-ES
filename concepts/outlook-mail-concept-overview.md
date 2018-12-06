---
title: Información general sobre la API de correo de Outlook
description: Outlook es un centro de comunicación de mensajería en Office 365. También le permite administrar contactos, programar reuniones, buscar información sobre los usuarios en una organización,
ms.openlocfilehash: a4ae3c00b578cf2f3bce7a23b73ec47dadc81cf8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092935"
---
# <a name="outlook-mail-api-overview"></a>Información general sobre la API de correo de Outlook

Outlook es un centro de comunicación de mensajería en Office 365. También le permite administrar contactos, programar reuniones, encontrar información sobre los usuarios de una organización, iniciar conversaciones en línea, compartir archivos y colaborar en grupos.

## <a name="why-integrate-with-outlook-mail"></a>¿Por qué integrar con el correo de Outlook?

### <a name="integrate-with-rich-features-and-reach-hundreds-of-millions-of-customers"></a>Integración con características avanzadas y llegar a cientos de millones de clientes

La integración con Outlook permite obtener acceso a la experiencia enriquecida que les encanta a los clientes: una experiencia uniforme e intuitiva para correo, [contactos](outlook-contacts-concept-overview.md) y [calendario](outlook-calendar-concept-overview.md), disponible en todos los dispositivos (móvil, web y escritorio).

Con [Microsoft Graph](overview.md), puede realizar la integración con Outlook al escribir una aplicación solo una vez y llegar a más de cientos de miles de consumidores, y decenas de millones de clientes de organizaciones que eligieron Outlook como su cliente de correo electrónico. Puede escribir aplicaciones que se centran en escenarios de correo, o bien conectarse a una amplia variedad de otras relaciones, recursos e inteligencia de Outlook y que no son de Outlook, y alcanzar escenarios admitidos por la nube de Microsoft.

### <a name="automate-message-organization-and-processing"></a>Automatizar el procesamiento y la organización de mensajes

A los clientes les gusta la forma en que Outlook les ayuda a organizarse. Microsoft Graph lleva estas características a los desarrolladores de aplicaciones, permitiéndoles crear flujos de trabajo de cliente que optimizan el descubrimiento y mejoran la eficiencia y la productividad:

- Los clientes organizan sus mensajes de formas distintas: algunos dejan todos los mensajes en la bandeja de entrada y simplemente los buscan, mientras que otros archivan sus mensajes en carpetas. Les gusta el método intuitivo y flexible de Outlook que permite realizar organizaciones simples o basadas en carpetas. Las aplicaciones pueden [filtrar, buscar u ordenar](query-parameters.md) fácilmente los mensajes de carpetas específicas o de todo el buzón del usuario.

- Las categorías de Outlook se diferencian por nombre y color. Las categorías permiten a los clientes etiquetar mensajes para mejorar su organización y descubrimiento. Las aplicaciones pueden obtener acceso y [definir la lista general de categorías de un usuario](/graph/api/outlookuser-post-mastercategories?view=graph-rest-1.0). Es más, esa lista se comparte en los mensajes de Outlook, así como en eventos, contactos, tareas y publicaciones del grupo, y facilita el acceso a escenarios creativos para los desarrolladores de aplicaciones. Por ejemplo, un proveedor de aprendizaje en línea puede codificar por colores los correos electrónicos, eventos de cursos y tareas de seguimiento de cada curso donde se inscribió un usuario.

- Además, los usuarios de la aplicación pueden cambiar la importancia de un mensaje (o de un evento o tarea), o bien marcar un mensaje para seguimiento. (La función de marcar está actualmente [en versión preliminar](versioning-and-support.md#beta-version) en Microsoft Graph).

- La API de reglas lleva la organización de mensajes al siguiente nivel. Las aplicaciones pueden configurar [reglas de la Bandeja de entrada](/graph/api/resources/messagerule?view=graph-rest-1.0) para procesar rápidamente los mensajes entrantes y mejorar la organización de los correos electrónicos. Por ejemplo, una aplicación puede mover mensajes automáticamente a otra carpeta si las líneas de asunto contienen determinadas palabras clave, y asignar categorías e importancia para facilitar el seguimiento posteriormente.

### <a name="write-smarter-apps-that-leverage-intelligence"></a>Escribir aplicaciones más inteligentes

Use Microsoft Graph para sugerir datos contextuales a los usuarios de la aplicación:

- Integre la [Bandeja de entrada Prioritarios](/graph/api/resources/manage-focused-inbox?view=graph-rest-1.0) y las [@menciones (versión preliminar)](/graph/api/message-get?view=graph-rest-beta#request-2), y permita a los usuarios de la aplicación leer y responder primero a lo que sea más relevante para ellos.

- Vea [sugerencias de correo ](/graph/api/resources/mailtips?view=graph-rest-1.0) al redactar un mensaje para obtener información de estado útil sobre un destinatario (por ejemplo, cuando el destinatario envía una respuesta automática o tiene el buzón lleno). Las sugerencias de correo pueden avisar a las aplicaciones de determinadas condiciones para, en su lugar, realizar acciones de seguimiento más eficientes.

- Use la [API de contactos](people-example.md) para proporcionar controles interactivos, como el Selector de personas, en su aplicación. La API de contactos puede sugerir los contactos más relevantes para un usuario basándose en las relaciones empresariales y los modelos de colaboración y comunicación del usuario.

- Ofrezca a los usuarios de la aplicación un selector de archivos inteligente y sugiera archivos con los que interactuaron recientemente para agregarlos como datos adjuntos al redactar un mensaje. [Insights (versión preliminar)](/graph/api/resources/insights?view=graph-rest-beta) usa análisis avanzados para sugerir archivos con actividad reciente sobre un usuario, vistos o editados recientemente por el usuario, o compartidos con el usuario.


### <a name="store-app-data-in-a-resource-or-resource-instance"></a>Almacenar los datos de aplicaciones en un recurso o una instancia de recurso

Con frecuencia, las aplicaciones necesitan almacenar sus datos en un almacén de datos externos, lo que conlleva una sobrecarga al administrar y obtener acceso a los datos. Microsoft Graph permite incluir solo los datos de aplicación como encabezados de mensajes de Internet al [crear](/graph/api/user-post-messages?view=graph-rest-1.0#request-2) o [enviar](/graph/api/user-sendmail?view=graph-rest-1.0#request-2) un mensaje o una respuesta a un mensaje.

Si quiere agregar y posteriormente actualizar datos personalizados, puede [almacenar los datos en las instancias de recurso individual](extensibility-overview.md#open-extensions). Si corresponde, como alternativa, puede ampliar el esquema, agregar las propiedades personalizadas y almacenar los datos escritos en los recursos de Microsoft Graph. También puede hacer que esas [extensiones de esquema](extensibility-overview.md#schema-extensions) se puedan compartir y descubrir.

## <a name="api-reference"></a>Referencia de la API
¿Busca la referencia de la API para este servicio?

- [API de correo de Outlook en Microsoft Graph v1.0](/graph/api/resources/mail-api-overview?view=graph-rest-1.0)
- [API de correo de Outlook en Microsoft Graph beta](/graph/api/resources/mail-api-overview?view=graph-rest-beta)


## <a name="next-steps"></a>Pasos siguientes

- Seleccione y pruebe consultas de ejemplo de correo de Outlook en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fmessages&version=v1.0). Seleccione la opción **Mostrar más ejemplos** en la columna de la izquierda. Use el menú para activar el **Correo de Outlook**.
- Obtenga información sobre:

  - [Crear y enviar mensajes](outlook-create-send-messages.md)
  - Formas de [organizar mensajes](outlook-organize-messages.md)
  - Cómo [recibir mensajes compartidos](outlook-share-messages-folders.md)
  - [Obtener identificadores inmutables para recursos de Outlook](outlook-immutable-id.md)

- Obtenga más información sobre cómo [usar la API de correo](/graph/api/resources/mail-api-overview?view=graph-rest-1.0) y sus [casos de uso](/graph/api/resources/mail-api-overview?view=graph-rest-1.0#common-use-cases) en Microsoft Graph v1.0.


