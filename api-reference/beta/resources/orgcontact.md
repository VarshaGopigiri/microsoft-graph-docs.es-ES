---
title: tipo de recurso orgContact
description: Aquí tiene una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: bdf63762a4bb632dccc3578963f42b91d7127fe1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832973"
---
# <a name="orgcontact-resource-type"></a>tipo de recurso orgContact

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
| addresses                    | [physicalOfficeAddress](physicalofficeaddress.md)            | Direcciones postales para este contacto de la organización. Por ahora un contacto sólo puede tener una dirección física. |
| companyName                  | String                                                    | Nombre de la compañía que este contacto organizativa pertenecen a.                                                                                                                                                                                                                                                                                                                 |
| department                   | Cadena                                                     | El nombre del departamento en el que trabaja el contacto.                                                                                                                                                                                                                                                                                                                                |
| displayName                  | Cadena                                                     | Nombre para mostrar para este contacto de la organización.                                                                                                                                                                                                                                                                                                                                   |
| givenName                    | Cadena                                                     | Nombre para este contacto de la organización.                                                                                                                                                                                                                                                                                                                                     |
| id                           | Cadena                                                     | Identificador único para este contacto de la organización.                                                                                                                                                                                                                                                                                                                             |
| imAddresses                  | Colección String                          | Lista de direcciones de mensajería instantánea para este contacto de la organización. Por ahora un contacto sólo puede tener una dirección SIP.                                                                                                                                                                                                                        |
| jobTitle                     | Cadena                                                     | Título del trabajo para este contacto de la organización.                                                                                                                                                                                                                                                                                                                                      |
|mail|Cadena| La dirección SMTP para el contacto, por ejemplo, "jeff@contoso.onmicrosoft.com". |
| mailNickname                 | Cadena                                                     | Alias de correo electrónico (parte de la dirección de correo electrónico pendiente previamente el símbolo @) para este contacto de la organización.                                                                                                                                                                                                                                                                                |
| onPremisesLastSyncDateTime   | DateTimeOffset                                             | Fecha y hora cuando este contacto organizativa por última sincronizan desde AD local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 tendrá este aspecto: ' 2014-01-01T00:00:00Z'.   |
| onPremisesProvisioningErrors |colección de [onPremisesProvisioningError](onpremisesprovisioningerror.md)       | Lista de cualquier sincronización de aprovisionamiento de errores para este contacto de la organización.                                                                                                                                                                                                                                                                                                |
|onPremisesSyncEnabled|Booleano|**es true** si este objeto se sincroniza de un directorio local; **false** si este objeto se ha originalmente sincronizado desde un directorio local, pero es ya no sincronizado y ahora definirlas en Exchange; **null** si este objeto nunca se sincronizaron desde un directorio local (valor predeterminado).|
| phones                       | Colección [phone](phone.md)                            | Lista de teléfonos para este contacto de la organización. Pueden ser tipos de teléfono móvil, empresarial y businessFax. Sólo uno de cada tipo de nunca puede estar presente en la colección.                                                                                                                       |
| proxyAddresses               | Colección string                                         | Por ejemplo: ["SMTP: bob@contoso.com", "smtp: bob@sales.contoso.com"]. El operador **any** es necesario para las expresiones de filtro en las propiedades multivalor. Compatible con \$filtro.                                                                                                                                                                               |
| surname                      | Cadena                                                     | Apellidos para este contacto de la organización.                          |

## <a name="relationships"></a>Relaciones

| Relación | Tipo   |Description|
|:---------------|:--------|:----------|
|directReports|Colección [directoryObject](directoryobject.md)| Informes de directos del contacto. (Los usuarios y contactos que tienen su propiedad administrador establecer a este contacto.)  Es de sólo lectura. Admite valores NULL.|
|manager|[directoryObject](directoryobject.md)| El usuario o el contacto que es administrador de este contacto. Solo lectura.|
|memberOf|Colección [directoryObject](directoryobject.md)| Grupos que este contacto es un miembro de. Solo lectura. Admite valores NULL.|

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
  "addresses": [{"@odata.type": "microsoft.graph.physicalOfficeAddress"}],
  "companyName": "string",
  "department": "string",
  "displayName": "string",
  "givenName": "string",
  "id": "string (identifier)",
  "jobTitle": "string",
  "mail": "string",
  "mailNickname": "string",
  "onPremisesLastSyncDateTime": "string (timestamp)",
  "onPremisesProvisioningErrors": [{"@odata.type": "microsoft.graph.onPremisesProvisioningError"}],
  "onPremisesSyncEnabled": true,
  "phones": [{"@odata.type": "microsoft.graph.phone"}],
  "proxyAddresses": ["string"],
  "surname": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "orgContact resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
