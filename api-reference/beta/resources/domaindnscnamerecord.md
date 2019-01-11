---
title: Tipo de recurso domainDnsCnameRecord
description: Representa un registro CNAME agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad DomainDnsRecord.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 86ce0a1e5336414ef87fb78752e8c252015f724c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856591"
---
# <a name="domaindnscnamerecord-resource-type"></a><span data-ttu-id="11899-104">Tipo de recurso domainDnsCnameRecord</span><span class="sxs-lookup"><span data-stu-id="11899-104">domainDnsCnameRecord resource type</span></span>

> <span data-ttu-id="11899-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11899-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11899-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11899-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="11899-p103">Representa un registro CNAME agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="11899-p103">Represents a CNAME record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>


## <a name="methods"></a><span data-ttu-id="11899-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="11899-109">Methods</span></span>
<span data-ttu-id="11899-p104">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="11899-p104">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="11899-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11899-112">Properties</span></span>
| <span data-ttu-id="11899-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11899-113">Property</span></span>     | <span data-ttu-id="11899-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="11899-114">Type</span></span>   |<span data-ttu-id="11899-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="11899-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="11899-116">canonicalName</span><span class="sxs-lookup"><span data-stu-id="11899-116">canonicalName</span></span>|<span data-ttu-id="11899-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="11899-117">String</span></span>| <span data-ttu-id="11899-p105">Nombre canónico del registro CNAME. Se usa para configurar el registro CNAME en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="11899-p105">The canonical name of the CNAME record. Used to configure the CNAME record at the DNS host.</span></span> |
|<span data-ttu-id="11899-120">id</span><span class="sxs-lookup"><span data-stu-id="11899-120">id</span></span>|<span data-ttu-id="11899-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="11899-121">String</span></span>| <span data-ttu-id="11899-p106">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="11899-p106">Unique identifier assigned to this entity. Not nullable, Read-only</span></span>|
|<span data-ttu-id="11899-124">isOptional</span><span class="sxs-lookup"><span data-stu-id="11899-124">isOptional</span></span>|<span data-ttu-id="11899-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="11899-125">Boolean</span></span>| <span data-ttu-id="11899-p107">Si es false, el cliente debe configurar el registro CNAME en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="11899-p107">If false, the CNAME record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain. Not nullable</span></span> |
|<span data-ttu-id="11899-128">label</span><span class="sxs-lookup"><span data-stu-id="11899-128">label</span></span>|<span data-ttu-id="11899-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="11899-129">String</span></span>| <span data-ttu-id="11899-130">Valor que se usa al configurar el *alias/host/name* del registro CNAME en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="11899-130">Value used when configuring the *alias/host/name* of the CNAME record at the DNS host.</span></span> |
|<span data-ttu-id="11899-131">recordType</span><span class="sxs-lookup"><span data-stu-id="11899-131">recordType</span></span>|<span data-ttu-id="11899-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="11899-132">String</span></span>| <span data-ttu-id="11899-p108">Tipo de registro DNS. El valor es siempre *CName*. Clave</span><span class="sxs-lookup"><span data-stu-id="11899-p108">Type of DNS record. The value is always *CName*. Key</span></span>|
|<span data-ttu-id="11899-136">supportedService</span><span class="sxs-lookup"><span data-stu-id="11899-136">supportedService</span></span>|<span data-ttu-id="11899-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="11899-137">String</span></span>| <span data-ttu-id="11899-138">Servicio o función de Microsoft Online que tiene una dependencia en el registro CNAME.</span><span class="sxs-lookup"><span data-stu-id="11899-138">Microsoft Online Service or feature that has a dependency on this CNAME record.</span></span></br></br><span data-ttu-id="11899-139">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="11899-139">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span>|
|<span data-ttu-id="11899-140">ttl</span><span class="sxs-lookup"><span data-stu-id="11899-140">ttl</span></span>|<span data-ttu-id="11899-141">Int32</span><span class="sxs-lookup"><span data-stu-id="11899-141">Int32</span></span>| <span data-ttu-id="11899-p109">Valor que se debe usar al configurar la propiedad de período de vida (ttl) del registro CNAME en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="11899-p109">Value to use when configuring the time-to-live (ttl) property of the CNAME record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="11899-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="11899-144">Relationships</span></span>
<span data-ttu-id="11899-145">Ninguno</span><span class="sxs-lookup"><span data-stu-id="11899-145">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="11899-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="11899-146">JSON representation</span></span>
<span data-ttu-id="11899-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="11899-147">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
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
