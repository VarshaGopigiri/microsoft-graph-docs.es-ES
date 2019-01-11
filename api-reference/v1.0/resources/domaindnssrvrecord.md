---
title: Tipo de recurso domainDnsSrvRecord
description: Representa un registro SRV agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 655dc6fcbccdcb6e1794c94d97dd8e7fc4837f04
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835794"
---
# <a name="domaindnssrvrecord-resource-type"></a><span data-ttu-id="97e20-104">Tipo de recurso domainDnsSrvRecord</span><span class="sxs-lookup"><span data-stu-id="97e20-104">domainDnsSrvRecord resource type</span></span>

<span data-ttu-id="97e20-p102">Representa un registro SRV agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="97e20-p102">Represents a SRV record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="97e20-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="97e20-107">Methods</span></span>
<span data-ttu-id="97e20-p103">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="97e20-p103">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="97e20-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97e20-110">Properties</span></span>
| <span data-ttu-id="97e20-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="97e20-111">Property</span></span>     | <span data-ttu-id="97e20-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="97e20-112">Type</span></span>   |<span data-ttu-id="97e20-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="97e20-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="97e20-114">id</span><span class="sxs-lookup"><span data-stu-id="97e20-114">id</span></span>|<span data-ttu-id="97e20-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="97e20-115">String</span></span>| <span data-ttu-id="97e20-p104">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="97e20-p104">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="97e20-118">isOptional</span><span class="sxs-lookup"><span data-stu-id="97e20-118">isOptional</span></span>|<span data-ttu-id="97e20-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="97e20-119">Boolean</span></span>| <span data-ttu-id="97e20-120">Si es false, el cliente debe configurar el registro SRV en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="97e20-120">If false, the SRV record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="97e20-121">label</span><span class="sxs-lookup"><span data-stu-id="97e20-121">label</span></span>|<span data-ttu-id="97e20-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="97e20-122">String</span></span>| <span data-ttu-id="97e20-123">Valor que se usa al configurar la propiedad *name* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="97e20-123">Value used when configuring the *name* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="97e20-124">nameTarget</span><span class="sxs-lookup"><span data-stu-id="97e20-124">nameTarget</span></span>|<span data-ttu-id="97e20-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="97e20-125">String</span></span>| <span data-ttu-id="97e20-126">Valor que se debe usar al configurar la propiedad *Target* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="97e20-126">Value to use when configuring the *Target* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="97e20-127">port</span><span class="sxs-lookup"><span data-stu-id="97e20-127">port</span></span>|<span data-ttu-id="97e20-128">Int32</span><span class="sxs-lookup"><span data-stu-id="97e20-128">Int32</span></span>| <span data-ttu-id="97e20-129">Valor que se debe usar al configurar la propiedad *port* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="97e20-129">Value to use when configuring the *port* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="97e20-130">priority</span><span class="sxs-lookup"><span data-stu-id="97e20-130">priority</span></span>|<span data-ttu-id="97e20-131">Int32</span><span class="sxs-lookup"><span data-stu-id="97e20-131">Int32</span></span>| <span data-ttu-id="97e20-132">Valor que se debe usar al configurar la propiedad *priority* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="97e20-132">Value to use when configuring the *priority* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="97e20-133">protocol</span><span class="sxs-lookup"><span data-stu-id="97e20-133">protocol</span></span>|<span data-ttu-id="97e20-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="97e20-134">String</span></span>| <span data-ttu-id="97e20-135">Valor que se debe usar al configurar la propiedad *protocol* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="97e20-135">Value to use when configuring the *protocol* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="97e20-136">recordType</span><span class="sxs-lookup"><span data-stu-id="97e20-136">recordType</span></span>|<span data-ttu-id="97e20-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="97e20-137">String</span></span>|  <span data-ttu-id="97e20-p105">Tipo de registro DNS. El valor es siempre *Srv*. Clave</span><span class="sxs-lookup"><span data-stu-id="97e20-p105">Type of DNS record. The value is always *Srv*. Key</span></span> |
|<span data-ttu-id="97e20-141">service</span><span class="sxs-lookup"><span data-stu-id="97e20-141">service</span></span>|<span data-ttu-id="97e20-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="97e20-142">String</span></span>| <span data-ttu-id="97e20-143">Valor que se debe usar al configurar la propiedad *service* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="97e20-143">Value to use when configuring the *service* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="97e20-144">supportedService</span><span class="sxs-lookup"><span data-stu-id="97e20-144">supportedService</span></span>|<span data-ttu-id="97e20-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="97e20-145">String</span></span>| <span data-ttu-id="97e20-146">Servicio o función de Microsoft Online que tiene una dependencia en el registro SRV.</span><span class="sxs-lookup"><span data-stu-id="97e20-146">Microsoft Online Service or feature that has a dependency on this SRV record.</span></span></br></br><span data-ttu-id="97e20-147">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="97e20-147">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span> |
|<span data-ttu-id="97e20-148">ttl</span><span class="sxs-lookup"><span data-stu-id="97e20-148">ttl</span></span>|<span data-ttu-id="97e20-149">Int32</span><span class="sxs-lookup"><span data-stu-id="97e20-149">Int32</span></span>| <span data-ttu-id="97e20-p106">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro SRV en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="97e20-p106">Value to use when configuring the *time-to-live (ttl)* property of the SRV record at the DNS host. Not nullable</span></span> |
|<span data-ttu-id="97e20-152">weight</span><span class="sxs-lookup"><span data-stu-id="97e20-152">weight</span></span>|<span data-ttu-id="97e20-153">Int32</span><span class="sxs-lookup"><span data-stu-id="97e20-153">Int32</span></span>| <span data-ttu-id="97e20-154">Valor que se debe usar al configurar la propiedad *weight* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="97e20-154">Value to use when configuring the *weight* property of the SRV record at the DNS host.</span></span> |

## <a name="relationships"></a><span data-ttu-id="97e20-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="97e20-155">Relationships</span></span>
<span data-ttu-id="97e20-156">Ninguno</span><span class="sxs-lookup"><span data-stu-id="97e20-156">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="97e20-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="97e20-157">JSON representation</span></span>
<span data-ttu-id="97e20-158">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="97e20-158">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsSrvRecord"
}-->

```json
{
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
