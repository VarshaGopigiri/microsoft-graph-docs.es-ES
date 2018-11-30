---
title: Tipo de recurso domainDnsUnavailableRecord
description: Cuando realiza una consulta para la propiedad de navegación **serviceConfigurationRecords** para una entidad de dominio, es posible que obtenga una o varias entidades DomainDnsCnameRecord, DomainDnsMxRecord, DomainDnsSrvRecord o DomainDnsTxtRecord. Estas entidades indican qué registros DNS que se debe agregar el archivo de zona del dominio, antes de que el dominio se puede usar por Microsoft Online Services. Cuando no es posible generar este tipo de entidades, una entidad DomainDnsUnavailableRecord se devuelve en su lugar. Se hereda de entidad DomainDnsRecord.
ms.openlocfilehash: 3eee5a814e7629ae603dc41670429fa82b85495f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032508"
---
# <a name="domaindnsunavailablerecord-resource-type"></a>Tipo de recurso domainDnsUnavailableRecord

Al consultar la propiedad de navegación **serviceConfigurationRecords** para una entidad [Domain](domain.md), es posible que reciba una o varias entidades [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) o [DomainDnsTxtRecord](domaindnstxtrecord.md). Estas entidades indican qué registros DNS debe agregar al archivo de zona del dominio antes de que Microsoft Online Services pueda usar el dominio. Si no se pueden generar dichas entidades, se devuelve una entidad DomainDnsUnavailableRecord. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).

## <a name="methods"></a>Métodos
No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|Cadena|Proporciona el motivo por el que se devuelve la entidad **DomainDnsUnavailableRecord**. |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsUnavailableRecord"
}-->

```json
{
  "description": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsUnavailableRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->