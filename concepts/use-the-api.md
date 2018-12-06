---
title: Usar la API de Microsoft Graph
description: Microsoft Graph es una API para web REST que permite tener acceso a los recursos del servicio Microsoft Cloud. Después de registrar su aplicación y obtener tokens de autenticación para un usuario o servicio, puede realizar solicitudes a la API de Microsoft Graph.
ms.openlocfilehash: 1a9d9bcefdfb302a9de602aa15aa642a0c57a793
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092906"
---
# <a name="use-the-microsoft-graph-api"></a>Usar la API de Microsoft Graph

Microsoft Graph es una API para web REST que permite tener acceso a los recursos del servicio Microsoft Cloud. Después de [registrar su aplicación](auth-register-app-v2.md) y [obtener tokens de autenticación para un usuario](auth-v2-user.md) o [servicio](auth-v2-service.md), puede realizar solicitudes a la API de Microsoft Graph.

> **Importante:** Cómo se aplican las directivas de acceso condicional a Microsoft Graph es algo que está cambiando. Las aplicaciones deben actualizarse para administrar los escenarios donde se configuran las directivas de acceso condicional. Para obtener más información y directrices, vea [Instrucciones para desarrolladores para Acceso condicional de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-conditional-access-developer).

Para leer o escribir en recursos como usuarios o mensajes de correo electrónico, se construye una solicitud similar a la siguiente.

```http
https://graph.microsoft.com/{version}/{resource}?query-parameters
```

Los componentes de una solicitud incluyen:

* [Método HTTP](#http-methods): método HTTP utilizado en la solicitud a Microsoft Graph.
* [`{version}`](#version): la versión de la API de Microsoft Graph utilizada por la aplicación.
* [`{resource}`](#resource): el recurso de Microsoft Graph al que se hace referencia.
* [query-parameters](#query-parameters-optional): un conjunto opcional de parámetros para modificar la solicitud o la respuesta.

Después de realizar una solicitud, se devuelve una respuesta que incluye: 

* Código de estado: un código de estado HTTP que indica correcto o incorrecto. Para obtener más información sobre los códigos de error HTTP, consulte [Errores](errors.md).
* Mensaje de respuesta: los datos que ha solicitado o el resultado de la operación. Con algunas operaciones, el mensaje de respuesta puede estar vacío.
* Vínculo **Siguiente**: si su solicitud devuelve una gran cantidad de datos, debe recorrer las páginas usando **Siguiente**. Para más información, consulte [Paginación](paging.md).

## <a name="http-methods"></a>Métodos HTTP

Microsoft Graph utiliza el método HTTP en la solicitud para determinar lo que está haciendo la solicitud. La API admite los siguientes métodos.


|**Método** |**Descripción**                             |
| :----- | :------------------------------------------- |
| GET    | Lee datos de un recurso.                   |
| POST   | Crea un nuevo recurso o realiza una acción. |
| PATCH  | Actualiza un recurso con nuevos valores.           |
| PUT    | Reemplaza un recurso por otro nuevo.           |
| DELETE | Elimina un recurso.                           |

* Para los métodos **GET** y **DELETE**, no es necesario un cuerpo de solicitud.
* Los métodos **POST**, **PATCH** y **PUT** requieren un cuerpo de la solicitud —generalmente especificado en formato JSON— que contiene información adicional, como los valores de las propiedades del recurso.

## <a name="version"></a>Versión

Microsoft Graph admite actualmente dos versiones: `v1.0` y `beta`.

* `v1.0` incluye las API que por lo general están disponibles. Utilice la versión v1.0 para todas las aplicaciones de producción.
* `beta` incluye las API que todavía están en versión preliminar. Debido a que podríamos introducir cambios importantes en nuestras API beta, recomendamos que utilice la versión beta solo para probar aplicaciones que están en desarrollo, y no en sus aplicaciones de producción.

Siempre agradecemos los comentarios sobre nuestras API beta. Para dar su opinión o solicitar características, visite nuestra página [UserVoice](https://officespdev.uservoice.com/).

Para obtener más información sobre las versiones de API, consulte [Control de versiones y soporte](versioning-and-support.md).

## <a name="resource"></a>Recurso

La dirección URL incluirá el recurso o los recursos con los que interactúa en la solicitud, como `me`, `users`, `groups`, `drives` y `sites`. Cada uno de los recursos de nivel superior también incluye **relaciones** que se pueden usar para tener acceso a recursos adicionales, como `me/messages` o `me/drive`. También puede interactuar con los recursos mediante **métodos**, por ejemplo, para enviar un correo electrónico, utilice `me/sendMail`.

Para obtener más información sobre cómo desplazarse por los métodos y relaciones de recursos, consulte [Recorrido por Microsoft Graph](traverse-the-graph.md). 

Cada recurso podría necesitar diferentes permisos de acceso. A menudo necesitará un nivel de permisos mayor para crear o actualizar un recurso que para leerlo. Para obtener más información sobre los permisos necesarios, consulte el tema de referencia del método. 

Para obtener más información acerca de los permisos, consulte [Referencia de permisos](permissions-reference.md).

## <a name="query-parameters-optional"></a>Parámetros de consulta (opcional)

Puede usar parámetros de consulta opcionales para personalizar la respuesta de la aplicación Microsoft Graph. Use parámetros de consulta para incluir más o menos propiedades que la respuesta predeterminada, filtrar la respuesta según los elementos que coincidan con una consulta personalizada o proporcionar parámetros adicionales para un método.

Por ejemplo, agregar el siguiente parámetro de filtro restringe los mensajes devueltos solo a aquellos que tengan la propiedad `emailAddress` de `jon@contoso.com`.

```http
https://graph.microsoft.com/v1.0/me/messages?filter=emailAddress eq 'jon@contoso.com'
```

Para obtener más información sobre los parámetros de consulta, vea [Personalizar respuestas](query-parameters.md).

## <a name="next-steps"></a>Pasos siguientes

Está listo para poner en funcionamiento Microsoft Graph. Para obtener más información, vaya a [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer) y pruebe algunas solicitudes y el [Inicio rápido](https://developer.microsoft.com/graph/quick-start), o comience con uno de nuestros [ejemplos de código y SDK](https://developer.microsoft.com/graph/code-samples-and-sdks).
