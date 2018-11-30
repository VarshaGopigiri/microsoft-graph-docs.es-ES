---
title: Tipo de recurso domainDnsRecord
description: Para cada dominio en el inquilino, puede ser necesario para agregar los registros DNS en el archivo de la zona DNS del dominio antes de que el dominio se puede usar por Microsoft Online Services. La entidad **DomainDnsRecord** se usa para presentar estos registros DNS. Entidad base para las entidades de DomainDnsCnameRecord, DomainDnsMxRecord, DomainDnsSrvRecord y DomainDnsSrvRecord.
ms.openlocfilehash: 766e3b241550ac1b0c7abdecaa22fe010955d05a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083874"
---
# <a name="domaindnsrecord-resource-type"></a><span data-ttu-id="8a426-105">Tipo de recurso domainDnsRecord</span><span class="sxs-lookup"><span data-stu-id="8a426-105">domainDnsRecord resource type</span></span>

> <span data-ttu-id="8a426-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8a426-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8a426-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8a426-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8a426-p103">En cada dominio del inquilino es posible que deba agregar registros DNS al archivo de zona DNS del dominio antes de que Microsoft Online Services pueda usar el dominio. La entidad **DomainDnsRecord** se usa para presentar dichos registros DNS. Entidad base de las entidades [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) y [DomainDnsSrvRecord](domaindnssrvrecord.md).</span><span class="sxs-lookup"><span data-stu-id="8a426-p103">For each domain in the tenant, you may be required to add DNS record(s) to the DNS zone file of the domain before the domain can be used by Microsoft Online Services. The **DomainDnsRecord** entity is used to present such DNS records. Base entity for [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) and [DomainDnsSrvRecord](domaindnssrvrecord.md) entities.</span></span>

## <a name="methods"></a><span data-ttu-id="8a426-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a426-111">Methods</span></span>
<span data-ttu-id="8a426-p104">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="8a426-p104">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="8a426-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a426-114">Properties</span></span>
| <span data-ttu-id="8a426-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8a426-115">Property</span></span>     | <span data-ttu-id="8a426-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a426-116">Type</span></span>   |<span data-ttu-id="8a426-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a426-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8a426-118">id</span><span class="sxs-lookup"><span data-stu-id="8a426-118">id</span></span>|<span data-ttu-id="8a426-119">String</span><span class="sxs-lookup"><span data-stu-id="8a426-119">String</span></span>| <span data-ttu-id="8a426-p105">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8a426-p105">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="8a426-122">isOptional</span><span class="sxs-lookup"><span data-stu-id="8a426-122">isOptional</span></span>|<span data-ttu-id="8a426-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a426-123">Boolean</span></span>| <span data-ttu-id="8a426-124">Si es false, el cliente debe configurar este registro en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="8a426-124">If false, this record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="8a426-125">label</span><span class="sxs-lookup"><span data-stu-id="8a426-125">label</span></span>|<span data-ttu-id="8a426-126">String</span><span class="sxs-lookup"><span data-stu-id="8a426-126">String</span></span>| <span data-ttu-id="8a426-127">Valor que se usa al configurar el nombre del registro DNS en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="8a426-127">Value used when configuring the name of the DNS record at the DNS host.</span></span> |
|<span data-ttu-id="8a426-128">recordType</span><span class="sxs-lookup"><span data-stu-id="8a426-128">recordType</span></span>|<span data-ttu-id="8a426-129">String</span><span class="sxs-lookup"><span data-stu-id="8a426-129">String</span></span>| <span data-ttu-id="8a426-130">Indica qué tipo de registro DNS representa esta entidad.</span><span class="sxs-lookup"><span data-stu-id="8a426-130">Indicates what type of DNS record this entity represents.</span></span></br></br><span data-ttu-id="8a426-131">El valor puede ser uno de los siguientes: *CName*, *Mx*, *Srv*, *Txt*</span><span class="sxs-lookup"><span data-stu-id="8a426-131">The value can be one of the following: *CName*, *Mx*, *Srv*, *Txt*</span></span></br></br><span data-ttu-id="8a426-132">Clave</span><span class="sxs-lookup"><span data-stu-id="8a426-132">Key</span></span> |
|<span data-ttu-id="8a426-133">supportedService</span><span class="sxs-lookup"><span data-stu-id="8a426-133">supportedService</span></span>|<span data-ttu-id="8a426-134">String</span><span class="sxs-lookup"><span data-stu-id="8a426-134">String</span></span>| <span data-ttu-id="8a426-135">Servicio o función de Microsoft Online que tiene una dependencia en el registro DNS.</span><span class="sxs-lookup"><span data-stu-id="8a426-135">Microsoft Online Service or feature that has a dependency on this DNS record.</span></span></br></br><span data-ttu-id="8a426-136">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="8a426-136">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span>|
|<span data-ttu-id="8a426-137">ttl</span><span class="sxs-lookup"><span data-stu-id="8a426-137">ttl</span></span>|<span data-ttu-id="8a426-138">Int32</span><span class="sxs-lookup"><span data-stu-id="8a426-138">Int32</span></span>| <span data-ttu-id="8a426-p106">Valor que se debe usar al configurar la propiedad de período de vida (ttl) del registro DNS en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="8a426-p106">Value to use when configuring the time-to-live (ttl) property of the DNS record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="8a426-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8a426-141">Relationships</span></span>
<span data-ttu-id="8a426-142">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8a426-142">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="8a426-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8a426-143">JSON representation</span></span>
<span data-ttu-id="8a426-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8a426-144">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsRecord"
}-->

```json
{
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "recordType": "String",
  "supportedService": "String",
  "ttl": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->