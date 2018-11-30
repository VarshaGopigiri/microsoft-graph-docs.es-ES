---
title: Tipo de recurso domainDnsCnameRecord
description: Representa un registro CNAME agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
ms.openlocfilehash: 1c8df7148a4d843d5cd6278f5cbcc03358159424
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031085"
---
# <a name="domaindnscnamerecord-resource-type"></a><span data-ttu-id="f83e4-104">Tipo de recurso domainDnsCnameRecord</span><span class="sxs-lookup"><span data-stu-id="f83e4-104">domainDnsCnameRecord resource type</span></span>

<span data-ttu-id="f83e4-p102">Representa un registro CNAME agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="f83e4-p102">Represents a CNAME record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>


## <a name="methods"></a><span data-ttu-id="f83e4-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="f83e4-107">Methods</span></span>
<span data-ttu-id="f83e4-p103">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="f83e4-p103">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="f83e4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f83e4-110">Properties</span></span>
| <span data-ttu-id="f83e4-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f83e4-111">Property</span></span>     | <span data-ttu-id="f83e4-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="f83e4-112">Type</span></span>   |<span data-ttu-id="f83e4-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f83e4-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f83e4-114">canonicalName</span><span class="sxs-lookup"><span data-stu-id="f83e4-114">canonicalName</span></span>|<span data-ttu-id="f83e4-115">String</span><span class="sxs-lookup"><span data-stu-id="f83e4-115">String</span></span>| <span data-ttu-id="f83e4-p104">Nombre canónico del registro CNAME. Se usa para configurar el registro CNAME en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="f83e4-p104">The canonical name of the CNAME record. Used to configure the CNAME record at the DNS host.</span></span> |
|<span data-ttu-id="f83e4-118">id</span><span class="sxs-lookup"><span data-stu-id="f83e4-118">id</span></span>|<span data-ttu-id="f83e4-119">String</span><span class="sxs-lookup"><span data-stu-id="f83e4-119">String</span></span>| <span data-ttu-id="f83e4-p105">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f83e4-p105">Unique identifier assigned to this entity. Not nullable, Read-only</span></span>|
|<span data-ttu-id="f83e4-122">isOptional</span><span class="sxs-lookup"><span data-stu-id="f83e4-122">isOptional</span></span>|<span data-ttu-id="f83e4-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="f83e4-123">Boolean</span></span>| <span data-ttu-id="f83e4-p106">Si es false, el cliente debe configurar el registro CNAME en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="f83e4-p106">If false, the CNAME record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain. Not nullable</span></span> |
|<span data-ttu-id="f83e4-126">label</span><span class="sxs-lookup"><span data-stu-id="f83e4-126">label</span></span>|<span data-ttu-id="f83e4-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="f83e4-127">String</span></span>| <span data-ttu-id="f83e4-128">Valor que se usa al configurar el *alias/host/name* del registro CNAME en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="f83e4-128">Value used when configuring the *alias/host/name* of the CNAME record at the DNS host.</span></span> |
|<span data-ttu-id="f83e4-129">recordType</span><span class="sxs-lookup"><span data-stu-id="f83e4-129">recordType</span></span>|<span data-ttu-id="f83e4-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="f83e4-130">String</span></span>| <span data-ttu-id="f83e4-p107">Tipo de registro DNS. El valor es siempre *CName*. Clave</span><span class="sxs-lookup"><span data-stu-id="f83e4-p107">Type of DNS record. The value is always *CName*. Key</span></span>|
|<span data-ttu-id="f83e4-134">supportedService</span><span class="sxs-lookup"><span data-stu-id="f83e4-134">supportedService</span></span>|<span data-ttu-id="f83e4-135">String</span><span class="sxs-lookup"><span data-stu-id="f83e4-135">String</span></span>| <span data-ttu-id="f83e4-136">Servicio o función de Microsoft Online que tiene una dependencia en el registro CNAME.</span><span class="sxs-lookup"><span data-stu-id="f83e4-136">Microsoft Online Service or feature that has a dependency on this CNAME record.</span></span></br></br><span data-ttu-id="f83e4-137">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="f83e4-137">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span>|
|<span data-ttu-id="f83e4-138">ttl</span><span class="sxs-lookup"><span data-stu-id="f83e4-138">ttl</span></span>|<span data-ttu-id="f83e4-139">Int32</span><span class="sxs-lookup"><span data-stu-id="f83e4-139">Int32</span></span>| <span data-ttu-id="f83e4-p108">Valor que se debe usar al configurar la propiedad de período de vida (ttl) del registro CNAME en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="f83e4-p108">Value to use when configuring the time-to-live (ttl) property of the CNAME record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="f83e4-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f83e4-142">Relationships</span></span>
<span data-ttu-id="f83e4-143">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f83e4-143">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="f83e4-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f83e4-144">JSON representation</span></span>
<span data-ttu-id="f83e4-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f83e4-145">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsCnameRecord"
}-->

```json
{
  "canonicalName": "String",
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
  "description": "domainDnsCnameRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->