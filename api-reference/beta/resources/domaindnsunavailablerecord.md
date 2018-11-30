---
title: Tipo de recurso domainDnsUnavailableRecord
description: Cuando realiza una consulta para la propiedad de navegación **serviceConfigurationRecords** para una entidad de dominio, es posible que obtenga una o varias entidades DomainDnsCnameRecord, DomainDnsMxRecord, DomainDnsSrvRecord o DomainDnsTxtRecord. Estas entidades indican qué registros DNS que se debe agregar el archivo de zona del dominio, antes de que el dominio se puede usar por Microsoft Online Services. Cuando no es posible generar este tipo de entidades, una entidad DomainDnsUnavailableRecord se devuelve en su lugar. Se hereda de entidad DomainDnsRecord.
ms.openlocfilehash: 0d920a2185cc84f5ca5cff571e1bb2c2d00400b5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083774"
---
# <a name="domaindnsunavailablerecord-resource-type"></a><span data-ttu-id="8d5ea-106">Tipo de recurso domainDnsUnavailableRecord</span><span class="sxs-lookup"><span data-stu-id="8d5ea-106">domainDnsUnavailableRecord resource type</span></span>

> <span data-ttu-id="8d5ea-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8d5ea-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8d5ea-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8d5ea-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8d5ea-p103">Al consultar la propiedad de navegación **serviceConfigurationRecords** para una entidad [Domain](domain.md), es posible que reciba una o varias entidades [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) o [DomainDnsTxtRecord](domaindnstxtrecord.md). Estas entidades indican qué registros DNS debe agregar al archivo de zona del dominio antes de que Microsoft Online Services pueda usar el dominio. Si no se pueden generar dichas entidades, se devuelve una entidad DomainDnsUnavailableRecord. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="8d5ea-p103">When you query for the navigation property **serviceConfigurationRecords** for a [Domain](domain.md) entity, you may get back one or more [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md), and/or [DomainDnsTxtRecord](domaindnstxtrecord.md) entities. These entities indicate what DNS records you must add to the zone file of the domain, before the domain can be used by Microsoft Online Services. When it is not possible to generate such entities, a DomainDnsUnavailableRecord Entity is returned instead. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="8d5ea-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8d5ea-113">Methods</span></span>
<span data-ttu-id="8d5ea-p104">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="8d5ea-p104">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="8d5ea-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d5ea-116">Properties</span></span>
| <span data-ttu-id="8d5ea-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d5ea-117">Property</span></span>     | <span data-ttu-id="8d5ea-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d5ea-118">Type</span></span>   |<span data-ttu-id="8d5ea-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d5ea-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8d5ea-120">description</span><span class="sxs-lookup"><span data-stu-id="8d5ea-120">description</span></span>|<span data-ttu-id="8d5ea-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="8d5ea-121">String</span></span>|<span data-ttu-id="8d5ea-122">Proporciona el motivo por el que se devuelve la entidad **DomainDnsUnavailableRecord**.</span><span class="sxs-lookup"><span data-stu-id="8d5ea-122">Provides the reason why the **DomainDnsUnavailableRecord** entity is returned.</span></span> |

## <a name="relationships"></a><span data-ttu-id="8d5ea-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8d5ea-123">Relationships</span></span>
<span data-ttu-id="8d5ea-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8d5ea-124">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="8d5ea-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d5ea-125">JSON representation</span></span>
<span data-ttu-id="8d5ea-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d5ea-126">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsUnavailableRecord"
}-->

```json
{
  "canonicalName": "String",
  "description": "String",
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "recordType": "String",
  "supportedService": "String",
  "text": "String",
  "ttl": 1024
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