---
title: Clonación de un equipo
description: Crear una copia de un equipo. Esta operación también crea una copia del grupo correspondiente.
author: nkramer
ms.openlocfilehash: 79ae6f770e009f262adbda4872ddc51af626688f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361932"
---
# <a name="clone-a-team"></a>Clonación de un equipo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Crear una copia de un [equipo](../resources/team.md). Esta operación también crea una copia del [grupo](../resources/group.md)correspondiente.
Puede especificar qué elementos del equipo que se debe clonar:

- **aplicaciones** : aplicaciones de los equipos de Microsoft de copias que se instalan en el equipo. 
- **canales de** – copia la estructura de canal (pero no los mensajes en el canal).
- **miembros** : copias de los miembros y propietarios del grupo.
- **configuración** – copia toda la configuración en el equipo, junto con la configuración de grupo de claves.
- **las fichas** – copias de las fichas dentro de los canales.

Cuando se clonarán las fichas, se ponen en un estado no configurado: se muestran en la barra de pestañas en Microsoft Teams, y la primera vez que se abren, se le dirigirá a través de la pantalla de configuración. (Si la persona que abre la ficha no tiene permiso para configurar aplicaciones, verán un mensaje que explica que no se ha configurado la ficha.)

La clonación es una operación de larga duración.
Después de que se devuelve el clon POST, debe obtener la [operación](../resources/teamsasyncoperation.md) para ver si es "que se está ejecutando" o "correcto" o "error". Se debe seguir GET hasta que el estado es no "en ejecución". El retraso entre obtiene recomendado es de 5 segundos.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | Group.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación                            | Group.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/clone
```

## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|classification|Cadena (opcional)|Describe una clasificación para el grupo (por ejemplo, el impacto de negocio bajo, medio o alto). Los valores válidos para esta propiedad se definen mediante la creación de un valor de [configuración](../resources/directorysetting.md) ClassificationList, basado en la [definición de plantilla](../resources/directorysettingtemplate.md). Si no se especifica la clasificación, la clasificación se copiarán desde el equipo original o grupo.|
|descripción|Cadena (opcional)|Una descripción opcional del grupo. Si no se especifica esta propiedad, se va a dejar en blanco.|
|displayName|String|El nombre para mostrar del grupo. Esta propiedad es necesaria cuando se crea un grupo y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.|
|mailNickname|String|El alias de correo para el grupo, único en la organización. Esta propiedad debe especificarse cuando se crea un grupo. Es compatible con $filter. Si no se especifica esta propiedad, se calculará de la propiedad displayName. Problema conocido: esta propiedad se omite actualmente.|
|partsToClone| [clonableTeamParts](../resources/clonableteamparts.md) |Una lista separados por comas de los elementos que se debe clonar. Los elementos legales son "aplicaciones, las fichas, configuración, canales, los miembros".|
|visibility|[teamVisibilityType](../resources/teamvisibilitytype.md) (opcional)| Especifica la visibilidad del grupo. Los valores posibles son: **privada**, **pública**. Si no se especifica la visibilidad, la visibilidad se copiarán desde el equipo original o grupo. Si el equipo que se está clonando es un equipo de **educationClass** , se omite el parámetro visibilidad y visibilidad del nuevo grupo se establecerá en HiddenMembership.|

## <a name="response"></a>Respuesta

Si tiene éxito, este método devolverá un `202 Accepted` código de respuesta con una ubicación: encabezado que señala hacia el recurso de la [operación](../resources/teamsasyncoperation.md) .
Una vez finalizada la operación, el recurso de la operación le indicará el identificador del equipo de creada.

## <a name="example"></a>Ejemplo
#### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "ignored",
  "name": "create_team"
}-->
```http
POST /teams/{id}/clone
Content-Type: application/json

{  
     "displayName": "Library Assist",
     "description": "Self help community for library",
     "mailNickname": "libassist",
     "partsToClone": "apps,tabs,settings,channels,members",
     "visibility": "public"
}
```

#### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán desde una llamada real.
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 202 Accepted
Location: /teams{id}/operations({opId})
Content-Type: text/plain
Content-Length: 0
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
