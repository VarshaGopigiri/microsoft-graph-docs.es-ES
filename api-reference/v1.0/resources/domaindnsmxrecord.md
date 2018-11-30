---
title: Tipo de recurso domainDnsMxRecord
description: Representa un registro MX agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
ms.openlocfilehash: 54a72f8e420d0313303b0787e803933888fb1e57
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030139"
---
# <a name="domaindnsmxrecord-resource-type"></a><span data-ttu-id="909bf-104">Tipo de recurso domainDnsMxRecord</span><span class="sxs-lookup"><span data-stu-id="909bf-104">domainDnsMxRecord resource type</span></span>

<span data-ttu-id="909bf-p102">Representa un registro MX agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="909bf-p102">Represents a MX record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="909bf-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="909bf-107">Methods</span></span>
<span data-ttu-id="909bf-p103">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="909bf-p103">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="909bf-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="909bf-110">Properties</span></span>
| <span data-ttu-id="909bf-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="909bf-111">Property</span></span>     | <span data-ttu-id="909bf-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="909bf-112">Type</span></span>   |<span data-ttu-id="909bf-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="909bf-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="909bf-114">id</span><span class="sxs-lookup"><span data-stu-id="909bf-114">id</span></span>|<span data-ttu-id="909bf-115">String</span><span class="sxs-lookup"><span data-stu-id="909bf-115">String</span></span>| <span data-ttu-id="909bf-p104">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="909bf-p104">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="909bf-118">isOptional</span><span class="sxs-lookup"><span data-stu-id="909bf-118">isOptional</span></span>|<span data-ttu-id="909bf-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="909bf-119">Boolean</span></span>| <span data-ttu-id="909bf-120">Si es false, el cliente debe configurar el registro MX en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="909bf-120">If false, the MX record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="909bf-121">label</span><span class="sxs-lookup"><span data-stu-id="909bf-121">label</span></span>|<span data-ttu-id="909bf-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="909bf-122">String</span></span>| <span data-ttu-id="909bf-123">Valor que se usa al configurar la propiedad *alias/host/name* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="909bf-123">Value used when configuring the *alias/host/name* property of the MX record at the DNS host.</span></span> |
|<span data-ttu-id="909bf-124">mailExchange</span><span class="sxs-lookup"><span data-stu-id="909bf-124">mailExchange</span></span>|<span data-ttu-id="909bf-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="909bf-125">String</span></span>| <span data-ttu-id="909bf-126">Valor que se usa al configurar la propiedad *answer/destination/value* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="909bf-126">Value used when configuring the *answer/destination/value* of the MX record at the DNS host.</span></span>|
|<span data-ttu-id="909bf-127">preference</span><span class="sxs-lookup"><span data-stu-id="909bf-127">preference</span></span>|<span data-ttu-id="909bf-128">Int32</span><span class="sxs-lookup"><span data-stu-id="909bf-128">Int32</span></span>| <span data-ttu-id="909bf-129">Valor que se usa al configurar la propiedad *Preference/Priority* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="909bf-129">Value used when configuring the *Preference/Priority* property of the MX record at the DNS host.</span></span> |
|<span data-ttu-id="909bf-130">recordType</span><span class="sxs-lookup"><span data-stu-id="909bf-130">recordType</span></span>|<span data-ttu-id="909bf-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="909bf-131">String</span></span>| <span data-ttu-id="909bf-p105">Tipo de registro DNS. El valor es siempre *Mx*. Clave</span><span class="sxs-lookup"><span data-stu-id="909bf-p105">Type of DNS record. The value is always *Mx*. Key</span></span> |
|<span data-ttu-id="909bf-135">supportedService</span><span class="sxs-lookup"><span data-stu-id="909bf-135">supportedService</span></span>|<span data-ttu-id="909bf-136">String</span><span class="sxs-lookup"><span data-stu-id="909bf-136">String</span></span>| <span data-ttu-id="909bf-137">Servicio o función de Microsoft Online que tiene una dependencia en el registro MX.</span><span class="sxs-lookup"><span data-stu-id="909bf-137">Microsoft Online Service or feature that has a dependency on this MX record.</span></span></br></br><span data-ttu-id="909bf-138">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="909bf-138">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span> |
|<span data-ttu-id="909bf-139">ttl</span><span class="sxs-lookup"><span data-stu-id="909bf-139">ttl</span></span>|<span data-ttu-id="909bf-140">Int32</span><span class="sxs-lookup"><span data-stu-id="909bf-140">Int32</span></span>| <span data-ttu-id="909bf-p106">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro MX en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="909bf-p106">Value to use when configuring the *time-to-live (ttl)* property of the MX record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="909bf-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="909bf-143">Relationships</span></span>
<span data-ttu-id="909bf-144">Ninguno</span><span class="sxs-lookup"><span data-stu-id="909bf-144">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="909bf-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="909bf-145">JSON representation</span></span>
<span data-ttu-id="909bf-146">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="909bf-146">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsMxRecord"
}-->

```json
{
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