---
title: Tipo de recurso domainDnsSrvRecord
description: Representa un registro SRV agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
ms.openlocfilehash: 1fd1123866d1674aec167de8bec8ef9a45be8d99
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030408"
---
# <a name="domaindnssrvrecord-resource-type"></a><span data-ttu-id="150d0-104">Tipo de recurso domainDnsSrvRecord</span><span class="sxs-lookup"><span data-stu-id="150d0-104">domainDnsSrvRecord resource type</span></span>

<span data-ttu-id="150d0-p102">Representa un registro SRV agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="150d0-p102">Represents a SRV record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="150d0-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="150d0-107">Methods</span></span>
<span data-ttu-id="150d0-p103">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="150d0-p103">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="150d0-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="150d0-110">Properties</span></span>
| <span data-ttu-id="150d0-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="150d0-111">Property</span></span>     | <span data-ttu-id="150d0-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="150d0-112">Type</span></span>   |<span data-ttu-id="150d0-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="150d0-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="150d0-114">id</span><span class="sxs-lookup"><span data-stu-id="150d0-114">id</span></span>|<span data-ttu-id="150d0-115">String</span><span class="sxs-lookup"><span data-stu-id="150d0-115">String</span></span>| <span data-ttu-id="150d0-p104">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="150d0-p104">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="150d0-118">isOptional</span><span class="sxs-lookup"><span data-stu-id="150d0-118">isOptional</span></span>|<span data-ttu-id="150d0-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="150d0-119">Boolean</span></span>| <span data-ttu-id="150d0-120">Si es false, el cliente debe configurar el registro SRV en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="150d0-120">If false, the SRV record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="150d0-121">label</span><span class="sxs-lookup"><span data-stu-id="150d0-121">label</span></span>|<span data-ttu-id="150d0-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="150d0-122">String</span></span>| <span data-ttu-id="150d0-123">Valor que se usa al configurar la propiedad *name* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="150d0-123">Value used when configuring the *name* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="150d0-124">nameTarget</span><span class="sxs-lookup"><span data-stu-id="150d0-124">nameTarget</span></span>|<span data-ttu-id="150d0-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="150d0-125">String</span></span>| <span data-ttu-id="150d0-126">Valor que se debe usar al configurar la propiedad *Target* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="150d0-126">Value to use when configuring the *Target* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="150d0-127">port</span><span class="sxs-lookup"><span data-stu-id="150d0-127">port</span></span>|<span data-ttu-id="150d0-128">Int32</span><span class="sxs-lookup"><span data-stu-id="150d0-128">Int32</span></span>| <span data-ttu-id="150d0-129">Valor que se debe usar al configurar la propiedad *port* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="150d0-129">Value to use when configuring the *port* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="150d0-130">priority</span><span class="sxs-lookup"><span data-stu-id="150d0-130">priority</span></span>|<span data-ttu-id="150d0-131">Int32</span><span class="sxs-lookup"><span data-stu-id="150d0-131">Int32</span></span>| <span data-ttu-id="150d0-132">Valor que se debe usar al configurar la propiedad *priority* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="150d0-132">Value to use when configuring the *priority* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="150d0-133">protocol</span><span class="sxs-lookup"><span data-stu-id="150d0-133">protocol</span></span>|<span data-ttu-id="150d0-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="150d0-134">String</span></span>| <span data-ttu-id="150d0-135">Valor que se debe usar al configurar la propiedad *protocol* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="150d0-135">Value to use when configuring the *protocol* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="150d0-136">recordType</span><span class="sxs-lookup"><span data-stu-id="150d0-136">recordType</span></span>|<span data-ttu-id="150d0-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="150d0-137">String</span></span>|  <span data-ttu-id="150d0-p105">Tipo de registro DNS. El valor es siempre *Srv*. Clave</span><span class="sxs-lookup"><span data-stu-id="150d0-p105">Type of DNS record. The value is always *Srv*. Key</span></span> |
|<span data-ttu-id="150d0-141">service</span><span class="sxs-lookup"><span data-stu-id="150d0-141">service</span></span>|<span data-ttu-id="150d0-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="150d0-142">String</span></span>| <span data-ttu-id="150d0-143">Valor que se debe usar al configurar la propiedad *service* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="150d0-143">Value to use when configuring the *service* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="150d0-144">supportedService</span><span class="sxs-lookup"><span data-stu-id="150d0-144">supportedService</span></span>|<span data-ttu-id="150d0-145">String</span><span class="sxs-lookup"><span data-stu-id="150d0-145">String</span></span>| <span data-ttu-id="150d0-146">Servicio o función de Microsoft Online que tiene una dependencia en el registro SRV.</span><span class="sxs-lookup"><span data-stu-id="150d0-146">Microsoft Online Service or feature that has a dependency on this SRV record.</span></span></br></br><span data-ttu-id="150d0-147">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="150d0-147">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span> |
|<span data-ttu-id="150d0-148">ttl</span><span class="sxs-lookup"><span data-stu-id="150d0-148">ttl</span></span>|<span data-ttu-id="150d0-149">Int32</span><span class="sxs-lookup"><span data-stu-id="150d0-149">Int32</span></span>| <span data-ttu-id="150d0-p106">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro SRV en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="150d0-p106">Value to use when configuring the *time-to-live (ttl)* property of the SRV record at the DNS host. Not nullable</span></span> |
|<span data-ttu-id="150d0-152">weight</span><span class="sxs-lookup"><span data-stu-id="150d0-152">weight</span></span>|<span data-ttu-id="150d0-153">Int32</span><span class="sxs-lookup"><span data-stu-id="150d0-153">Int32</span></span>| <span data-ttu-id="150d0-154">Valor que se debe usar al configurar la propiedad *weight* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="150d0-154">Value to use when configuring the *weight* property of the SRV record at the DNS host.</span></span> |

## <a name="relationships"></a><span data-ttu-id="150d0-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="150d0-155">Relationships</span></span>
<span data-ttu-id="150d0-156">Ninguno</span><span class="sxs-lookup"><span data-stu-id="150d0-156">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="150d0-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="150d0-157">JSON representation</span></span>
<span data-ttu-id="150d0-158">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="150d0-158">Here is a JSON representation of the resource.</span></span>

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