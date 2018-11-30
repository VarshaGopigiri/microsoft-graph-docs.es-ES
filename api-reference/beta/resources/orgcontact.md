---
title: tipo de recurso orgContact
description: Aquí tiene una representación JSON del recurso
ms.openlocfilehash: fb0970b2eb973e516761ba1145d66b3af7fdef5f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088656"
---
# <a name="orgcontact-resource-type"></a>tipo de recurso orgContact

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "directReports",
    "manager",
    "memberOf"
  ],
  "@odata.type": "microsoft.graph.orgcontact"
}-->

```json
{
  "businessPhones": ["string"],
  "city": "string",
  "companyName": "string",
  "country": "string",
  "department": "string",
  "displayName": "string",
  "givenName": "string",
  "id": "string (identifier)",
  "jobTitle": "string",
  "mail": "string",
  "mailNickname": "string",
  "mobilePhone": "string",
  "officeLocation": "string",
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesProvisioningErrors": [{"@odata.type": "microsoft.graph.onPremisesProvisioningError"}],
  "onPremisesSyncEnabled": true,
  "postalCode": "string",
  "proxyAddresses": ["string"],
  "state": "string",
  "streetAddress": "string",
  "surname": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|city|String| La ciudad donde se encuentra el contacto. |
|country|String| El país o región en el que se encuentra el contacto. |
|department|String| El nombre del departamento en el que trabaja el contacto. |
|onPremisesSyncEnabled|Booleano|**true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado).|
|displayName|String| El nombre para mostrar para el contacto. |
|givenName|String| El nombre dado (nombre) del contacto. |
|jobTitle|String| Título del trabajo del contacto. |
|onPremisesLastSyncDateTime|DateTimeOffset|Indica la última vez en que el objeto se ha sincronizado con el directorio local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|onPremisesProvisioningErrors|colección de [onPremisesProvisioningError](onpremisesprovisioningerror.md)| Errores al usar el producto de sincronización de Microsoft durante el aprovisionamiento. |
|mail|String| La dirección SMTP para el contacto, por ejemplo, "jeff@contoso.onmicrosoft.com". |
|mailNickname|String| El alias de correo para el contacto. |
|mobilePhone|String| El número de teléfono móvil principal del contacto. |
|id|String| El identificador único para el contacto. Solo lectura.|
|officeLocation|String| La ubicación de oficina en lugar del contacto de negocio. |
|postalCode|String| El código postal de dirección postal del contacto. El código postal es específico país o región del contacto. En los Estados Unidos de América, este atributo contiene el código postal. |
|proxyAddresses|Colección string| Por ejemplo: `["SMTP: bob@contoso.com", "smtp: bob@sales.contoso.com"]` el operador **any** es necesario para las expresiones de filtro en las propiedades multivalor. Solo lectura. No admite valores NULL. Es compatible con $filter. |
|estado|String| El estado o provincia de la dirección del contacto. |
|streetAddress|String| La dirección postal del domicilio del contacto. |
|surname|String| El apellido del contacto (familia de nombre o apellidos). |
|businessPhones|String| El número de teléfono principal del lugar del contacto de negocio. |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|directReports|Colección [directoryObject](directoryobject.md)| Informes de directos del contacto. (Los usuarios y contactos que tienen su propiedad administrador establecer a este contacto.)  Es de sólo lectura. Admite valores NULL.|
|manager|[directoryObject](directoryobject.md)| El usuario o el contacto que es administrador de este contacto. Solo lectura.|
|memberOf|Colección [directoryObject](directoryobject.md)| Grupos que este contacto es un miembro de. Solo lectura. Admite valores NULL.|

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener orgContact](../api/orgcontact-get.md) | [orgContact](orgcontact.md) |Leer las propiedades y las relaciones del objeto orgContact.|
|[Obtener el administrador](../api/orgcontact-get-manager.md) |[directoryObject](directoryobject.md)| Obtener el administrador del contacto.|
|[Enumerar directReports](../api/orgcontact-list-directreports.md) |Colección [directoryObject](directoryobject.md)| Lista de los informes directos del contacto.|
|[Enumerar memberOf](../api/orgcontact-list-memberof.md) |Colección [directoryObject](directoryobject.md)| Obtener una colección de objetos de miembro.|
|[Delete](../api/orgcontact-delete.md) | Ninguno |Eliminar el objeto orgContact. |
|[checkMemberGroups](../api/orgcontact-checkmembergroups.md)|Colección string| Comprueba la pertenencia a grupo. |
|[getMemberGroups](../api/orgcontact-getmembergroups.md)|Colección string| Devolver todos los grupos que el contacto especificado es un miembro de. |
|[getMemberObjects](../api/orgcontact-getmemberobjects.md)|Colección string| Devuelve una lista de directoryObjects de que el contacto es un miembro. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "orgContact resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->