---
title: Tipo de recurso domainDnsTxtRecord
description: Representa un registro TXT agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
author: lleonard-msft
ms.openlocfilehash: caefb97b39219c282c45949b504c3d0b91cdada9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27349017"
---
# <a name="domaindnstxtrecord-resource-type"></a><span data-ttu-id="0b226-104">Tipo de recurso domainDnsTxtRecord</span><span class="sxs-lookup"><span data-stu-id="0b226-104">domainDnsTxtRecord resource type</span></span>

> <span data-ttu-id="0b226-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0b226-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0b226-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0b226-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0b226-p103">Representa un registro TXT agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="0b226-p103">Represents a TXT record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="0b226-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b226-109">Methods</span></span>
<span data-ttu-id="0b226-p104">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="0b226-p104">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="0b226-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b226-112">Properties</span></span>
| <span data-ttu-id="0b226-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b226-113">Property</span></span>     | <span data-ttu-id="0b226-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b226-114">Type</span></span>   |<span data-ttu-id="0b226-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b226-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0b226-116">id</span><span class="sxs-lookup"><span data-stu-id="0b226-116">id</span></span>|<span data-ttu-id="0b226-117">String</span><span class="sxs-lookup"><span data-stu-id="0b226-117">String</span></span>| <span data-ttu-id="0b226-p105">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0b226-p105">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span> |
|<span data-ttu-id="0b226-120">isOptional</span><span class="sxs-lookup"><span data-stu-id="0b226-120">isOptional</span></span>|<span data-ttu-id="0b226-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b226-121">Boolean</span></span>| <span data-ttu-id="0b226-122">Si es false, el cliente debe configurar el registro TXT en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="0b226-122">If false, the TXT record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="0b226-123">label</span><span class="sxs-lookup"><span data-stu-id="0b226-123">label</span></span>|<span data-ttu-id="0b226-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="0b226-124">String</span></span>| <span data-ttu-id="0b226-125">Valor que se debe usar al configurar la propiedad *name* del registro TXT en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="0b226-125">Value to use when configuring the *name* property of the TXT record at the DNS host.</span></span>|
|<span data-ttu-id="0b226-126">recordType</span><span class="sxs-lookup"><span data-stu-id="0b226-126">recordType</span></span>|<span data-ttu-id="0b226-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="0b226-127">String</span></span>| <span data-ttu-id="0b226-p106">Tipo de registro DNS. El valor es siempre *Txt*. Clave</span><span class="sxs-lookup"><span data-stu-id="0b226-p106">Type of DNS record. The value is always *Txt*. Key</span></span> |
|<span data-ttu-id="0b226-131">supportedService</span><span class="sxs-lookup"><span data-stu-id="0b226-131">supportedService</span></span>|<span data-ttu-id="0b226-132">String</span><span class="sxs-lookup"><span data-stu-id="0b226-132">String</span></span>| <span data-ttu-id="0b226-133">Servicio o función de Microsoft Online que tiene una dependencia en el registro TXT.</span><span class="sxs-lookup"><span data-stu-id="0b226-133">Microsoft Online Service or feature that has a dependency on this TXT record.</span></span></br></br><span data-ttu-id="0b226-134">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="0b226-134">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span> |
|<span data-ttu-id="0b226-135">text</span><span class="sxs-lookup"><span data-stu-id="0b226-135">text</span></span>|<span data-ttu-id="0b226-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="0b226-136">String</span></span>| <span data-ttu-id="0b226-137">Valor que se usa al configurar la propiedad *text* en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="0b226-137">Value used when configuring the *text* property at the DNS host.</span></span> |
|<span data-ttu-id="0b226-138">ttl</span><span class="sxs-lookup"><span data-stu-id="0b226-138">ttl</span></span>|<span data-ttu-id="0b226-139">Int32</span><span class="sxs-lookup"><span data-stu-id="0b226-139">Int32</span></span>| <span data-ttu-id="0b226-p107">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro MX en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="0b226-p107">Value to use when configuring the *time-to-live (ttl)* property of the MX record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="0b226-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0b226-142">Relationships</span></span>
<span data-ttu-id="0b226-143">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0b226-143">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="0b226-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0b226-144">JSON representation</span></span>
<span data-ttu-id="0b226-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0b226-145">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsTxtRecord"
}-->

```json
{
  "canonicalName": "String",
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
  "description": "domainDnsTxtRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->