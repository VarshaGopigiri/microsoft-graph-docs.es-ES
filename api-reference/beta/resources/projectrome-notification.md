---
title: tipo de recurso de notificación
description: 'Representa una notificación que se publica en un servidor de aplicación que se dirige a un usuario especificado. La notificación se almacena en Microsoft Graph y se distribuye a los extremos de otro dispositivo que pertenecen al usuario. '
localization_priority: Normal
ms.prod: project-rome
ms.openlocfilehash: e920645e0d526893eff197b42ed5d6ef7f7c7b93
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973079"
---
# <a name="notification-resource-type"></a>tipo de recurso de notificación
> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una notificación que se publica en un servidor de aplicación que se dirige a un usuario especificado. La notificación se almacena en Microsoft Graph y se distribuye a los extremos de otro dispositivo que pertenecen al usuario. 

Una notificación puede ser una carga de notificación visual que pueda ser interpretada por el sistema operativo, incluidas las plataformas Windows, Android y iOS. También puede ser una carga de datos que se ha entregado al y controlan por los clientes de la aplicación, que, a continuación, determinar el usuario correspondiente experiencia en cada dispositivo – normalmente, una notificación visual de la interfaz de usuario que se corresponde con el contenido de la carga de datos original que se genera localmente. 

Cuando un usuario actúa en una notificación visual, el cliente de la aplicación, a continuación, puede usar SDK de Roma de proyecto de cliente para actualizar el estado de la notificación correspondiente fuente en Microsoft Graph - por ejemplo, marcando una notificación como descartados. La actualización se distribuirá a todos los otros extremos de cliente de aplicación, y los clientes controlen el cambio en consecuencia, por ejemplo mediante al descartar la notificación para evitar que el usuario vea información redundante. Los clientes de la aplicación pueden tener acceso al mismo recurso de notificación en un momento posterior antes de que expire (incluso después de que se marca como descartados), como historial de notificación, mediante el [SDK de Project Roma](https://github.com/Microsoft/project-rome). 

## <a name="methods"></a>Métodos
|Método | Tipo de valor devuelto | Descripción|
|:------|:------------|:-----------|
|[Creación de notificación](../api/projectrome-notification-post.md) | [notificación](projectrome-notification.md) |Crear y enviar una notificación. |

## <a name="properties"></a>Propiedades
|Nombre | Tipo | Descripción|
|:----|:-----|:-----------|
| targetHostName | Cadena | Representa el nombre de host de la aplicación a la que desea que el servicio de llamadas registrar la notificación para el usuario determinado. |
| appNotificationId | Cadena | Identificador único establecido por el servidor de aplicaciones de una notificación que se usa para identificar y dirigir una notificación individual. |
| expirationDateTime | DateTimeOffset | Establece un tiempo de expiración UTC en una notificación de usuario - cuando es tiempo de copia de seguridad, la notificación se quita completamente desde el almacén de notificación de fuente de Microsoft Graph y ya no forma parte del historial de notificaciones. El valor máximo es de 30 días. |
| carga útil | Edm.ComplexType, objeto JSON | Este es el contenido de datos de una notificación de usuario sin procesar o visual que se entrega a y consumido por el cliente de app recibir esta notificación. |
| payload.rawContent | Cadena | El contenido de la notificación de una notificación de usuario original que se entrega a y consumido por el cliente de app recibir esta notificación. Al menos uno de los Payload.RawContent y Payload.VisualContent debe ser válida para una solicitud de notificación de entrada. |
| Payload.Visual | Edm.ComplexType, objeto JSON | El contenido visual de una notificación de usuario visual, que se consumidos por la plataforma de notificación en cada plataforma móvil y presenta para los usuarios. Al menos uno de contenido y VisualContent debe ser válida para una solicitud de notificación de entrada. |
| Payload.Visual.Title | Cadena | El título de una notificación de usuario visual. Debe tener el título o el cuerpo. |
| Payload.Visual.Body | Cadena | El cuerpo de una notificación de usuario visual. Debe tener el título o el cuerpo. |
| displayTimeToLive | Int | Establece cuánto tiempo (en segundos) que se mantendrá este contenido de la notificación en el Visor de notificación de la plataforma. Por ejemplo, cuando se envía la notificación a un dispositivo de Windows, el valor de esta propiedad se pasa a ToastNotification.ExpirationTime, que determina cuánto se mantendrá la notificación del sistema en el centro de actividades de Windows del usuario. |
| prioridad | EnumType | Indica la prioridad de una notificación de usuario sin procesar. Se envían notificaciones visuales con prioridad alta de forma predeterminada. Los valores válidos son alta y baja. |
| groupName | Cadena | El nombre del grupo al que pertenece esta notificación. Se establece por el programador con el fin de la agrupación de las notificaciones. |
| targetPolicy | Edm.ComplexType, objeto JSON | Objeto de directiva de destino controla la directiva de la entrega de notificación en dos niveles diferentes - tipos de extremo (Windows, iOS y Android) que deben dirigirse y extremos específicos (identificados por los identificadores de suscripción) que deben dirigirse. |
| targetPolicy.platformTypes | Edm.ComplexType, colección (EnumType) | Se usa para filtrar la distribución de notificaciones para una plataforma específica o plataformas. De forma predeterminada, se habilitan todos los tipos de extremo de inserción (iOS, Windows y Android). |

## <a name="relationships"></a>Relaciones
Ninguna.

## <a name="json-representation"></a>Representación JSON
La siguiente es una representación JSON del recurso cuando se publica una notificación visual directa que se entrega en el sistema operativo de destino.

```json
{   
  "targetHostName": "String",
  "appNotificationId": "String",
  "expirationDateTime": "DateTimeOffset",
  "payload":  
  {
    "visualContent": 
    {
      "title": "String",
      "body": "String"
    },
  },
  "displayTimeToLive": "Int",
  "priority": "Enum",
  "groupName": "String",
  "targetPolicy":
  {
    "platformTypes": [ 
      "Enum"
    ]
  }
}
```

La siguiente es una representación JSON del recurso cuando se publica una notificación de datos sin procesar que se entrega a los clientes de la aplicación.
```json
{   
  "targetHostName": "String",
  "appNotificationId": "String",
  "expirationDateTime": "DateTimeOffset",
  "payload":  
  {
    "rawContent": "String"
  },
  "displayTimeToLive": "Int",
  "priority": "Enum",
  "groupName": "String",
  "targetPolicy":
  {
    "platformTypes": [ 
      "Enum"
    ]
  }
}
```
