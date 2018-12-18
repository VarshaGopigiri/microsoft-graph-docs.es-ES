---
title: Tipo de recurso domainDnsTxtRecord
description: Representa un registro TXT agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
author: lleonard-msft
ms.openlocfilehash: b7714555a9d88a6af201d81083efea3eb20c660c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313527"
---
# <a name="domaindnstxtrecord-resource-type"></a><span data-ttu-id="a275d-104">Tipo de recurso domainDnsTxtRecord</span><span class="sxs-lookup"><span data-stu-id="a275d-104">domainDnsTxtRecord resource type</span></span>

<span data-ttu-id="a275d-p102">Representa un registro TXT agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="a275d-p102">Represents a TXT record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="a275d-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a275d-107">Methods</span></span>
<span data-ttu-id="a275d-p103">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="a275d-p103">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="a275d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a275d-110">Properties</span></span>
| <span data-ttu-id="a275d-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a275d-111">Property</span></span>     | <span data-ttu-id="a275d-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="a275d-112">Type</span></span>   |<span data-ttu-id="a275d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a275d-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a275d-114">id</span><span class="sxs-lookup"><span data-stu-id="a275d-114">id</span></span>|<span data-ttu-id="a275d-115">String</span><span class="sxs-lookup"><span data-stu-id="a275d-115">String</span></span>| <span data-ttu-id="a275d-p104">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a275d-p104">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span> |
|<span data-ttu-id="a275d-118">isOptional</span><span class="sxs-lookup"><span data-stu-id="a275d-118">isOptional</span></span>|<span data-ttu-id="a275d-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="a275d-119">Boolean</span></span>| <span data-ttu-id="a275d-120">Si es false, el cliente debe configurar el registro TXT en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="a275d-120">If false, the TXT record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="a275d-121">label</span><span class="sxs-lookup"><span data-stu-id="a275d-121">label</span></span>|<span data-ttu-id="a275d-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="a275d-122">String</span></span>| <span data-ttu-id="a275d-123">Valor que se debe usar al configurar la propiedad *name* del registro TXT en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="a275d-123">Value to use when configuring the *name* property of the TXT record at the DNS host.</span></span>|
|<span data-ttu-id="a275d-124">recordType</span><span class="sxs-lookup"><span data-stu-id="a275d-124">recordType</span></span>|<span data-ttu-id="a275d-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="a275d-125">String</span></span>| <span data-ttu-id="a275d-p105">Tipo de registro DNS. El valor es siempre *Txt*. Clave</span><span class="sxs-lookup"><span data-stu-id="a275d-p105">Type of DNS record. The value is always *Txt*. Key</span></span> |
|<span data-ttu-id="a275d-129">supportedService</span><span class="sxs-lookup"><span data-stu-id="a275d-129">supportedService</span></span>|<span data-ttu-id="a275d-130">String</span><span class="sxs-lookup"><span data-stu-id="a275d-130">String</span></span>| <span data-ttu-id="a275d-131">Servicio o función de Microsoft Online que tiene una dependencia en el registro TXT.</span><span class="sxs-lookup"><span data-stu-id="a275d-131">Microsoft Online Service or feature that has a dependency on this TXT record.</span></span></br></br><span data-ttu-id="a275d-132">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="a275d-132">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span> |
|<span data-ttu-id="a275d-133">text</span><span class="sxs-lookup"><span data-stu-id="a275d-133">text</span></span>|<span data-ttu-id="a275d-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a275d-134">String</span></span>| <span data-ttu-id="a275d-135">Valor que se usa al configurar la propiedad *text* en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="a275d-135">Value used when configuring the *text* property at the DNS host.</span></span> |
|<span data-ttu-id="a275d-136">ttl</span><span class="sxs-lookup"><span data-stu-id="a275d-136">ttl</span></span>|<span data-ttu-id="a275d-137">Int32</span><span class="sxs-lookup"><span data-stu-id="a275d-137">Int32</span></span>| <span data-ttu-id="a275d-p106">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro MX en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="a275d-p106">Value to use when configuring the *time-to-live (ttl)* property of the MX record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="a275d-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a275d-140">Relationships</span></span>
<span data-ttu-id="a275d-141">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a275d-141">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="a275d-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a275d-142">JSON representation</span></span>
<span data-ttu-id="a275d-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a275d-143">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsTxtRecord"
}-->

```json
{
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