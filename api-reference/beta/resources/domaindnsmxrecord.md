---
title: Tipo de recurso domainDnsMxRecord
description: Representa un registro MX agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 90744a9a800fd3a330b9df41299e335c5852446a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923512"
---
# <a name="domaindnsmxrecord-resource-type"></a>Tipo de recurso domainDnsMxRecord

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un registro MX agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).

## <a name="methods"></a>Métodos
No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.|
|isOptional|Booleano| Si es false, el cliente debe configurar el registro MX en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio. |
|label|Cadena| Valor que se usa al configurar la propiedad *alias/host/name* del registro MX en el host DNS. |
|mailExchange|Cadena| Valor que se usa al configurar la propiedad *answer/destination/value* del registro MX en el host DNS.|
|preference|Int32| Valor que se usa al configurar la propiedad *Preference/Priority* del registro MX en el host DNS. |
|recordType|Cadena| Tipo de registro DNS. El valor es siempre *Mx*. Clave |
|supportedService|Cadena| Servicio o función de Microsoft Online que tiene una dependencia en el registro MX.</br></br>Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune* |
|ttl|Int32| Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro MX en el host DNS. No admite valores NULL |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsMxRecord"
}-->

```json
{
  "canonicalName": "String",
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "mailExchange": "String",
  "preference": 1024,
  "recordType": "String",
  "supportedService": "String",
  "ttl": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsMxRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
