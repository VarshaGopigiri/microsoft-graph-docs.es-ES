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
# <a name="domaindnssrvrecord-resource-type"></a><span data-ttu-id="50e56-104">Tipo de recurso domainDnsSrvRecord</span><span class="sxs-lookup"><span data-stu-id="50e56-104">domainDnsSrvRecord resource type</span></span>

> <span data-ttu-id="50e56-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="50e56-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="50e56-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="50e56-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="50e56-p103">Representa un registro SRV agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="50e56-p103">Represents a SRV record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="50e56-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="50e56-109">Methods</span></span>
<span data-ttu-id="50e56-p104">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="50e56-p104">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="50e56-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50e56-112">Properties</span></span>
| <span data-ttu-id="50e56-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50e56-113">Property</span></span>     | <span data-ttu-id="50e56-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="50e56-114">Type</span></span>   |<span data-ttu-id="50e56-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="50e56-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="50e56-116">id</span><span class="sxs-lookup"><span data-stu-id="50e56-116">id</span></span>|<span data-ttu-id="50e56-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="50e56-117">String</span></span>| <span data-ttu-id="50e56-p105">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="50e56-p105">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="50e56-120">isOptional</span><span class="sxs-lookup"><span data-stu-id="50e56-120">isOptional</span></span>|<span data-ttu-id="50e56-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="50e56-121">Boolean</span></span>| <span data-ttu-id="50e56-122">Si es false, el cliente debe configurar el registro SRV en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="50e56-122">If false, the SRV record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="50e56-123">label</span><span class="sxs-lookup"><span data-stu-id="50e56-123">label</span></span>|<span data-ttu-id="50e56-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="50e56-124">String</span></span>| <span data-ttu-id="50e56-125">Valor que se usa al configurar la propiedad *name* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="50e56-125">Value used when configuring the *name* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="50e56-126">nameTarget</span><span class="sxs-lookup"><span data-stu-id="50e56-126">nameTarget</span></span>|<span data-ttu-id="50e56-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="50e56-127">String</span></span>| <span data-ttu-id="50e56-128">Valor que se debe usar al configurar la propiedad *Target* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="50e56-128">Value to use when configuring the *Target* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="50e56-129">port</span><span class="sxs-lookup"><span data-stu-id="50e56-129">port</span></span>|<span data-ttu-id="50e56-130">Int32</span><span class="sxs-lookup"><span data-stu-id="50e56-130">Int32</span></span>| <span data-ttu-id="50e56-131">Valor que se debe usar al configurar la propiedad *port* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="50e56-131">Value to use when configuring the *port* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="50e56-132">priority</span><span class="sxs-lookup"><span data-stu-id="50e56-132">priority</span></span>|<span data-ttu-id="50e56-133">Int32</span><span class="sxs-lookup"><span data-stu-id="50e56-133">Int32</span></span>| <span data-ttu-id="50e56-134">Valor que se debe usar al configurar la propiedad *priority* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="50e56-134">Value to use when configuring the *priority* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="50e56-135">protocol</span><span class="sxs-lookup"><span data-stu-id="50e56-135">protocol</span></span>|<span data-ttu-id="50e56-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="50e56-136">String</span></span>| <span data-ttu-id="50e56-137">Valor que se debe usar al configurar la propiedad *protocol* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="50e56-137">Value to use when configuring the *protocol* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="50e56-138">recordType</span><span class="sxs-lookup"><span data-stu-id="50e56-138">recordType</span></span>|<span data-ttu-id="50e56-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="50e56-139">String</span></span>|  <span data-ttu-id="50e56-p106">Tipo de registro DNS. El valor es siempre *Srv*. Clave</span><span class="sxs-lookup"><span data-stu-id="50e56-p106">Type of DNS record. The value is always *Srv*. Key</span></span> |
|<span data-ttu-id="50e56-143">service</span><span class="sxs-lookup"><span data-stu-id="50e56-143">service</span></span>|<span data-ttu-id="50e56-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="50e56-144">String</span></span>| <span data-ttu-id="50e56-145">Valor que se debe usar al configurar la propiedad *service* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="50e56-145">Value to use when configuring the *service* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="50e56-146">supportedService</span><span class="sxs-lookup"><span data-stu-id="50e56-146">supportedService</span></span>|<span data-ttu-id="50e56-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="50e56-147">String</span></span>| <span data-ttu-id="50e56-148">Servicio o función de Microsoft Online que tiene una dependencia en el registro SRV.</span><span class="sxs-lookup"><span data-stu-id="50e56-148">Microsoft Online Service or feature that has a dependency on this SRV record.</span></span></br></br><span data-ttu-id="50e56-149">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="50e56-149">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span> |
|<span data-ttu-id="50e56-150">ttl</span><span class="sxs-lookup"><span data-stu-id="50e56-150">ttl</span></span>|<span data-ttu-id="50e56-151">Int32</span><span class="sxs-lookup"><span data-stu-id="50e56-151">Int32</span></span>| <span data-ttu-id="50e56-p107">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro SRV en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="50e56-p107">Value to use when configuring the *time-to-live (ttl)* property of the SRV record at the DNS host. Not nullable</span></span> |
|<span data-ttu-id="50e56-154">weight</span><span class="sxs-lookup"><span data-stu-id="50e56-154">weight</span></span>|<span data-ttu-id="50e56-155">Int32</span><span class="sxs-lookup"><span data-stu-id="50e56-155">Int32</span></span>| <span data-ttu-id="50e56-156">Valor que se debe usar al configurar la propiedad *weight* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="50e56-156">Value to use when configuring the *weight* property of the SRV record at the DNS host.</span></span> |

## <a name="relationships"></a><span data-ttu-id="50e56-157">Relaciones</span><span class="sxs-lookup"><span data-stu-id="50e56-157">Relationships</span></span>
<span data-ttu-id="50e56-158">Ninguno</span><span class="sxs-lookup"><span data-stu-id="50e56-158">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="50e56-159">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="50e56-159">JSON representation</span></span>
<span data-ttu-id="50e56-160">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="50e56-160">Here is a JSON representation of the resource.</span></span>

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
