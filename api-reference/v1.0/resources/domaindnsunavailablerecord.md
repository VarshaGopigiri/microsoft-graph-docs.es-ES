---
title: Tipo de recurso domainDnsUnavailableRecord
description: Cuando realiza una consulta para la propiedad de navegación **serviceConfigurationRecords** para una entidad de dominio, es posible que obtenga una o varias entidades DomainDnsCnameRecord, DomainDnsMxRecord, DomainDnsSrvRecord o DomainDnsTxtRecord. Estas entidades indican qué registros DNS que se debe agregar el archivo de zona del dominio, antes de que el dominio se puede usar por Microsoft Online Services. Cuando no es posible generar este tipo de entidades, una entidad DomainDnsUnavailableRecord se devuelve en su lugar. Se hereda de entidad DomainDnsRecord.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 5f033c39c9cf8dc11c2a41b0cedb0b8de5ce7736
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968179"
---
# <a name="domaindnsunavailablerecord-resource-type"></a><span data-ttu-id="33c96-106">Tipo de recurso domainDnsUnavailableRecord</span><span class="sxs-lookup"><span data-stu-id="33c96-106">domainDnsUnavailableRecord resource type</span></span>

<span data-ttu-id="33c96-p102">Al consultar la propiedad de navegación **serviceConfigurationRecords** para una entidad [Domain](domain.md), es posible que reciba una o varias entidades [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) o [DomainDnsTxtRecord](domaindnstxtrecord.md). Estas entidades indican qué registros DNS debe agregar al archivo de zona del dominio antes de que Microsoft Online Services pueda usar el dominio. Si no se pueden generar dichas entidades, se devuelve una entidad DomainDnsUnavailableRecord. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="33c96-p102">When you query for the navigation property **serviceConfigurationRecords** for a [Domain](domain.md) entity, you may get back one or more [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md), and/or [DomainDnsTxtRecord](domaindnstxtrecord.md) entities. These entities indicate what DNS records you must add to the zone file of the domain, before the domain can be used by Microsoft Online Services. When it is not possible to generate such entities, a DomainDnsUnavailableRecord Entity is returned instead. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="33c96-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="33c96-111">Methods</span></span>
<span data-ttu-id="33c96-p103">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="33c96-p103">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="33c96-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33c96-114">Properties</span></span>
| <span data-ttu-id="33c96-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33c96-115">Property</span></span>     | <span data-ttu-id="33c96-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="33c96-116">Type</span></span>   |<span data-ttu-id="33c96-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="33c96-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="33c96-118">description</span><span class="sxs-lookup"><span data-stu-id="33c96-118">description</span></span>|<span data-ttu-id="33c96-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="33c96-119">String</span></span>|<span data-ttu-id="33c96-120">Proporciona el motivo por el que se devuelve la entidad **DomainDnsUnavailableRecord**.</span><span class="sxs-lookup"><span data-stu-id="33c96-120">Provides the reason why the **DomainDnsUnavailableRecord** entity is returned.</span></span> |

## <a name="relationships"></a><span data-ttu-id="33c96-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="33c96-121">Relationships</span></span>
<span data-ttu-id="33c96-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="33c96-122">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="33c96-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="33c96-123">JSON representation</span></span>
<span data-ttu-id="33c96-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="33c96-124">Here is a JSON representation of the resource.</span></span>

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
