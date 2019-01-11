---
title: Tipo de recurso domainDnsRecord
description: Para cada dominio en el inquilino, puede ser necesario para agregar los registros DNS en el archivo de la zona DNS del dominio antes de que el dominio se puede usar por Microsoft Online Services. La entidad **DomainDnsRecord** se usa para presentar estos registros DNS. Entidad base para las entidades de DomainDnsCnameRecord, DomainDnsMxRecord, DomainDnsSrvRecord y DomainDnsSrvRecord.
localization_priority: Normal
ms.openlocfilehash: 30c5f63f4ecac2c716f7884ccf82fd129125c8b1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822347"
---
# <a name="domaindnsrecord-resource-type"></a><span data-ttu-id="091fb-105">Tipo de recurso domainDnsRecord</span><span class="sxs-lookup"><span data-stu-id="091fb-105">domainDnsRecord resource type</span></span>

<span data-ttu-id="091fb-p102">En cada dominio del inquilino es posible que deba agregar registros DNS al archivo de zona DNS del dominio antes de que Microsoft Online Services pueda usar el dominio. La entidad **DomainDnsRecord** se usa para presentar dichos registros DNS. Entidad base de las entidades [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) y [DomainDnsSrvRecord](domaindnssrvrecord.md).</span><span class="sxs-lookup"><span data-stu-id="091fb-p102">For each domain in the tenant, you may be required to add DNS record(s) to the DNS zone file of the domain before the domain can be used by Microsoft Online Services. The **DomainDnsRecord** entity is used to present such DNS records. Base entity for [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) and [DomainDnsSrvRecord](domaindnssrvrecord.md) entities.</span></span>

## <a name="methods"></a><span data-ttu-id="091fb-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="091fb-109">Methods</span></span>
<span data-ttu-id="091fb-p103">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="091fb-p103">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="091fb-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="091fb-112">Properties</span></span>
| <span data-ttu-id="091fb-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="091fb-113">Property</span></span>     | <span data-ttu-id="091fb-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="091fb-114">Type</span></span>   |<span data-ttu-id="091fb-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="091fb-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="091fb-116">id</span><span class="sxs-lookup"><span data-stu-id="091fb-116">id</span></span>|<span data-ttu-id="091fb-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="091fb-117">String</span></span>| <span data-ttu-id="091fb-p104">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="091fb-p104">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="091fb-120">isOptional</span><span class="sxs-lookup"><span data-stu-id="091fb-120">isOptional</span></span>|<span data-ttu-id="091fb-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="091fb-121">Boolean</span></span>| <span data-ttu-id="091fb-122">Si es false, el cliente debe configurar este registro en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="091fb-122">If false, this record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="091fb-123">label</span><span class="sxs-lookup"><span data-stu-id="091fb-123">label</span></span>|<span data-ttu-id="091fb-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="091fb-124">String</span></span>| <span data-ttu-id="091fb-125">Valor que se usa al configurar el nombre del registro DNS en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="091fb-125">Value used when configuring the name of the DNS record at the DNS host.</span></span> |
|<span data-ttu-id="091fb-126">recordType</span><span class="sxs-lookup"><span data-stu-id="091fb-126">recordType</span></span>|<span data-ttu-id="091fb-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="091fb-127">String</span></span>| <span data-ttu-id="091fb-128">Indica qué tipo de registro DNS representa esta entidad.</span><span class="sxs-lookup"><span data-stu-id="091fb-128">Indicates what type of DNS record this entity represents.</span></span></br></br><span data-ttu-id="091fb-129">El valor puede ser uno de los siguientes: *CName*, *Mx*, *Srv*, *Txt*</span><span class="sxs-lookup"><span data-stu-id="091fb-129">The value can be one of the following: *CName*, *Mx*, *Srv*, *Txt*</span></span></br></br><span data-ttu-id="091fb-130">Clave</span><span class="sxs-lookup"><span data-stu-id="091fb-130">Key</span></span> |
|<span data-ttu-id="091fb-131">supportedService</span><span class="sxs-lookup"><span data-stu-id="091fb-131">supportedService</span></span>|<span data-ttu-id="091fb-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="091fb-132">String</span></span>| <span data-ttu-id="091fb-133">Servicio o función de Microsoft Online que tiene una dependencia en el registro DNS.</span><span class="sxs-lookup"><span data-stu-id="091fb-133">Microsoft Online Service or feature that has a dependency on this DNS record.</span></span></br></br><span data-ttu-id="091fb-134">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="091fb-134">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span>|
|<span data-ttu-id="091fb-135">ttl</span><span class="sxs-lookup"><span data-stu-id="091fb-135">ttl</span></span>|<span data-ttu-id="091fb-136">Int32</span><span class="sxs-lookup"><span data-stu-id="091fb-136">Int32</span></span>| <span data-ttu-id="091fb-p105">Valor que se debe usar al configurar la propiedad de período de vida (ttl) del registro DNS en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="091fb-p105">Value to use when configuring the time-to-live (ttl) property of the DNS record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="091fb-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="091fb-139">Relationships</span></span>
<span data-ttu-id="091fb-140">Ninguno</span><span class="sxs-lookup"><span data-stu-id="091fb-140">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="091fb-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="091fb-141">JSON representation</span></span>
<span data-ttu-id="091fb-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="091fb-142">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
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
