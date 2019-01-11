---
title: Tipo de recurso domainDnsSrvRecord
description: Representa un registro SRV agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: c06682753b752980530bf8cfd8f6a32b9bbd569a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810440"
---
# <a name="domaindnssrvrecord-resource-type"></a>Tipo de recurso domainDnsSrvRecord

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un registro SRV agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).

## <a name="methods"></a>Métodos
No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.|
|isOptional|Booleano| Si es false, el cliente debe configurar el registro SRV en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio. |
|label|Cadena| Valor que se usa al configurar la propiedad *name* del registro SRV en el host DNS. |
|nameTarget|Cadena| Valor que se debe usar al configurar la propiedad *Target* del registro SRV en el host DNS. |
|port|Int32| Valor que se debe usar al configurar la propiedad *port* del registro SRV en el host DNS. |
|priority|Int32| Valor que se debe usar al configurar la propiedad *priority* del registro SRV en el host DNS. |
|protocol|Cadena| Valor que se debe usar al configurar la propiedad *protocol* del registro SRV en el host DNS. |
|recordType|Cadena|  Tipo de registro DNS. El valor es siempre *Srv*. Clave |
|service|Cadena| Valor que se debe usar al configurar la propiedad *service* del registro SRV en el host DNS. |
|supportedService|Cadena| Servicio o función de Microsoft Online que tiene una dependencia en el registro SRV.</br></br>Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune* |
|ttl|Int32| Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro SRV en el host DNS. No admite valores NULL |
|weight|Int32| Valor que se debe usar al configurar la propiedad *weight* del registro SRV en el host DNS. |

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsSrvRecord"
}-->

```json
{
  "canonicalName": "String",
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "nameTarget": "String",
  "port": 1024,
  "priority": 1024,
  "protocol": "String",
  "recordType": "String",
  "service": "String",
  "supportedService": "String",
  "ttl": 1024,
  "weight": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsSrvRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
