---
title: Tipo de recurso domainDnsMxRecord
description: Representa un registro MX agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 90744a9a800fd3a330b9df41299e335c5852446a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923512"
---
# <a name="domaindnsmxrecord-resource-type"></a><span data-ttu-id="d2a6b-104">Tipo de recurso domainDnsMxRecord</span><span class="sxs-lookup"><span data-stu-id="d2a6b-104">domainDnsMxRecord resource type</span></span>

> <span data-ttu-id="d2a6b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d2a6b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d2a6b-p103">Representa un registro MX agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="d2a6b-p103">Represents a MX record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="d2a6b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2a6b-109">Methods</span></span>
<span data-ttu-id="d2a6b-p104">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-p104">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="d2a6b-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2a6b-112">Properties</span></span>
| <span data-ttu-id="d2a6b-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2a6b-113">Property</span></span>     | <span data-ttu-id="d2a6b-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2a6b-114">Type</span></span>   |<span data-ttu-id="d2a6b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2a6b-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d2a6b-116">id</span><span class="sxs-lookup"><span data-stu-id="d2a6b-116">id</span></span>|<span data-ttu-id="d2a6b-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2a6b-117">String</span></span>| <span data-ttu-id="d2a6b-p105">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-p105">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="d2a6b-120">isOptional</span><span class="sxs-lookup"><span data-stu-id="d2a6b-120">isOptional</span></span>|<span data-ttu-id="d2a6b-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="d2a6b-121">Boolean</span></span>| <span data-ttu-id="d2a6b-122">Si es false, el cliente debe configurar el registro MX en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-122">If false, the MX record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="d2a6b-123">label</span><span class="sxs-lookup"><span data-stu-id="d2a6b-123">label</span></span>|<span data-ttu-id="d2a6b-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2a6b-124">String</span></span>| <span data-ttu-id="d2a6b-125">Valor que se usa al configurar la propiedad *alias/host/name* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-125">Value used when configuring the *alias/host/name* property of the MX record at the DNS host.</span></span> |
|<span data-ttu-id="d2a6b-126">mailExchange</span><span class="sxs-lookup"><span data-stu-id="d2a6b-126">mailExchange</span></span>|<span data-ttu-id="d2a6b-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2a6b-127">String</span></span>| <span data-ttu-id="d2a6b-128">Valor que se usa al configurar la propiedad *answer/destination/value* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-128">Value used when configuring the *answer/destination/value* of the MX record at the DNS host.</span></span>|
|<span data-ttu-id="d2a6b-129">preference</span><span class="sxs-lookup"><span data-stu-id="d2a6b-129">preference</span></span>|<span data-ttu-id="d2a6b-130">Int32</span><span class="sxs-lookup"><span data-stu-id="d2a6b-130">Int32</span></span>| <span data-ttu-id="d2a6b-131">Valor que se usa al configurar la propiedad *Preference/Priority* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-131">Value used when configuring the *Preference/Priority* property of the MX record at the DNS host.</span></span> |
|<span data-ttu-id="d2a6b-132">recordType</span><span class="sxs-lookup"><span data-stu-id="d2a6b-132">recordType</span></span>|<span data-ttu-id="d2a6b-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2a6b-133">String</span></span>| <span data-ttu-id="d2a6b-p106">Tipo de registro DNS. El valor es siempre *Mx*. Clave</span><span class="sxs-lookup"><span data-stu-id="d2a6b-p106">Type of DNS record. The value is always *Mx*. Key</span></span> |
|<span data-ttu-id="d2a6b-137">supportedService</span><span class="sxs-lookup"><span data-stu-id="d2a6b-137">supportedService</span></span>|<span data-ttu-id="d2a6b-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2a6b-138">String</span></span>| <span data-ttu-id="d2a6b-139">Servicio o función de Microsoft Online que tiene una dependencia en el registro MX.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-139">Microsoft Online Service or feature that has a dependency on this MX record.</span></span></br></br><span data-ttu-id="d2a6b-140">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="d2a6b-140">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span> |
|<span data-ttu-id="d2a6b-141">ttl</span><span class="sxs-lookup"><span data-stu-id="d2a6b-141">ttl</span></span>|<span data-ttu-id="d2a6b-142">Int32</span><span class="sxs-lookup"><span data-stu-id="d2a6b-142">Int32</span></span>| <span data-ttu-id="d2a6b-p107">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro MX en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="d2a6b-p107">Value to use when configuring the *time-to-live (ttl)* property of the MX record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="d2a6b-145">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d2a6b-145">Relationships</span></span>
<span data-ttu-id="d2a6b-146">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d2a6b-146">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="d2a6b-147">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d2a6b-147">JSON representation</span></span>
<span data-ttu-id="d2a6b-148">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d2a6b-148">Here is a JSON representation of the resource.</span></span>

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
