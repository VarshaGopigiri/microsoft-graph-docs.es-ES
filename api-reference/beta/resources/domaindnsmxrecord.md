---
title: Tipo de recurso domainDnsMxRecord
description: Representa un registro MX agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
ms.openlocfilehash: 51a99efbb9929064809bbd00364c72ffe2ed8651
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083162"
---
# <a name="domaindnsmxrecord-resource-type"></a><span data-ttu-id="1c799-104">Tipo de recurso domainDnsMxRecord</span><span class="sxs-lookup"><span data-stu-id="1c799-104">domainDnsMxRecord resource type</span></span>

> <span data-ttu-id="1c799-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1c799-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1c799-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1c799-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1c799-p103">Representa un registro MX agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="1c799-p103">Represents a MX record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="1c799-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c799-109">Methods</span></span>
<span data-ttu-id="1c799-p104">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="1c799-p104">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="1c799-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c799-112">Properties</span></span>
| <span data-ttu-id="1c799-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1c799-113">Property</span></span>     | <span data-ttu-id="1c799-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c799-114">Type</span></span>   |<span data-ttu-id="1c799-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c799-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1c799-116">id</span><span class="sxs-lookup"><span data-stu-id="1c799-116">id</span></span>|<span data-ttu-id="1c799-117">String</span><span class="sxs-lookup"><span data-stu-id="1c799-117">String</span></span>| <span data-ttu-id="1c799-p105">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1c799-p105">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="1c799-120">isOptional</span><span class="sxs-lookup"><span data-stu-id="1c799-120">isOptional</span></span>|<span data-ttu-id="1c799-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="1c799-121">Boolean</span></span>| <span data-ttu-id="1c799-122">Si es false, el cliente debe configurar el registro MX en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="1c799-122">If false, the MX record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="1c799-123">label</span><span class="sxs-lookup"><span data-stu-id="1c799-123">label</span></span>|<span data-ttu-id="1c799-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="1c799-124">String</span></span>| <span data-ttu-id="1c799-125">Valor que se usa al configurar la propiedad *alias/host/name* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="1c799-125">Value used when configuring the *alias/host/name* property of the MX record at the DNS host.</span></span> |
|<span data-ttu-id="1c799-126">mailExchange</span><span class="sxs-lookup"><span data-stu-id="1c799-126">mailExchange</span></span>|<span data-ttu-id="1c799-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="1c799-127">String</span></span>| <span data-ttu-id="1c799-128">Valor que se usa al configurar la propiedad *answer/destination/value* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="1c799-128">Value used when configuring the *answer/destination/value* of the MX record at the DNS host.</span></span>|
|<span data-ttu-id="1c799-129">preference</span><span class="sxs-lookup"><span data-stu-id="1c799-129">preference</span></span>|<span data-ttu-id="1c799-130">Int32</span><span class="sxs-lookup"><span data-stu-id="1c799-130">Int32</span></span>| <span data-ttu-id="1c799-131">Valor que se usa al configurar la propiedad *Preference/Priority* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="1c799-131">Value used when configuring the *Preference/Priority* property of the MX record at the DNS host.</span></span> |
|<span data-ttu-id="1c799-132">recordType</span><span class="sxs-lookup"><span data-stu-id="1c799-132">recordType</span></span>|<span data-ttu-id="1c799-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="1c799-133">String</span></span>| <span data-ttu-id="1c799-p106">Tipo de registro DNS. El valor es siempre *Mx*. Clave</span><span class="sxs-lookup"><span data-stu-id="1c799-p106">Type of DNS record. The value is always *Mx*. Key</span></span> |
|<span data-ttu-id="1c799-137">supportedService</span><span class="sxs-lookup"><span data-stu-id="1c799-137">supportedService</span></span>|<span data-ttu-id="1c799-138">String</span><span class="sxs-lookup"><span data-stu-id="1c799-138">String</span></span>| <span data-ttu-id="1c799-139">Servicio o función de Microsoft Online que tiene una dependencia en el registro MX.</span><span class="sxs-lookup"><span data-stu-id="1c799-139">Microsoft Online Service or feature that has a dependency on this MX record.</span></span></br></br><span data-ttu-id="1c799-140">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="1c799-140">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span> |
|<span data-ttu-id="1c799-141">ttl</span><span class="sxs-lookup"><span data-stu-id="1c799-141">ttl</span></span>|<span data-ttu-id="1c799-142">Int32</span><span class="sxs-lookup"><span data-stu-id="1c799-142">Int32</span></span>| <span data-ttu-id="1c799-p107">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro MX en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="1c799-p107">Value to use when configuring the *time-to-live (ttl)* property of the MX record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="1c799-145">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1c799-145">Relationships</span></span>
<span data-ttu-id="1c799-146">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1c799-146">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="1c799-147">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1c799-147">JSON representation</span></span>
<span data-ttu-id="1c799-148">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1c799-148">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsMxRecord"
}-->

```json
{
  "canonicalName": "String",
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