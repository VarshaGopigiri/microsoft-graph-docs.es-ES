---
title: tipo de recurso hostSecurityState
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 1ae1436dd9771d34c37542eb756f81a4f8f0306a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853378"
---
# <a name="hostsecuritystate-resource-type"></a><span data-ttu-id="70c29-104">tipo de recurso hostSecurityState</span><span class="sxs-lookup"><span data-stu-id="70c29-104">hostSecurityState resource type</span></span>

 > <span data-ttu-id="70c29-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="70c29-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="70c29-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="70c29-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="70c29-107">Contiene información de estado acerca del host (incluidos los dispositivos, equipos y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="70c29-107">Contains stateful information about the host (including devices, computers, and so on).</span></span>

## <a name="properties"></a><span data-ttu-id="70c29-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70c29-108">Properties</span></span>

| <span data-ttu-id="70c29-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="70c29-109">Property</span></span>   | <span data-ttu-id="70c29-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="70c29-110">Type</span></span>|<span data-ttu-id="70c29-111">Description</span><span class="sxs-lookup"><span data-stu-id="70c29-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="70c29-112">FQDN</span><span class="sxs-lookup"><span data-stu-id="70c29-112">fqdn</span></span>|<span data-ttu-id="70c29-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="70c29-113">String</span></span>|<span data-ttu-id="70c29-114">Host FQDN (nombre de dominio completo) (por ejemplo, machine.company.com).</span><span class="sxs-lookup"><span data-stu-id="70c29-114">Host FQDN (Fully Qualified Domain Name) (for example, machine.company.com).</span></span>|
|<span data-ttu-id="70c29-115">isAzureAadJoined</span><span class="sxs-lookup"><span data-stu-id="70c29-115">isAzureAadJoined</span></span>|<span data-ttu-id="70c29-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="70c29-116">Boolean</span></span>|<span data-ttu-id="70c29-117">Es True si el host es el dominio unido a Azure los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="70c29-117">True if the host is domain joined to Azure Active Directory Domain Services.</span></span>|
|<span data-ttu-id="70c29-118">isAzureAadRegistered</span><span class="sxs-lookup"><span data-stu-id="70c29-118">isAzureAadRegistered</span></span>|<span data-ttu-id="70c29-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="70c29-119">Boolean</span></span>|<span data-ttu-id="70c29-120">Es True si el host registrado con Azure Active Directory dispositivo de registro (BYOD dispositivos - es decir, no totalmente administrados por empresa).</span><span class="sxs-lookup"><span data-stu-id="70c29-120">True if the host registered with Azure Active Directory Device Registration (BYOD devices - that is, not fully managed by enterprise).</span></span>|
|<span data-ttu-id="70c29-121">isHybridAzureDomainJoined</span><span class="sxs-lookup"><span data-stu-id="70c29-121">isHybridAzureDomainJoined</span></span>|<span data-ttu-id="70c29-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="70c29-122">Boolean</span></span>|<span data-ttu-id="70c29-123">Es True si el host está unido a un dominio de Active Directory local de dominio.</span><span class="sxs-lookup"><span data-stu-id="70c29-123">True if the host is domain joined to an on-premises Active Directory domain.</span></span>|
|<span data-ttu-id="70c29-124">nombreNetBIOS</span><span class="sxs-lookup"><span data-stu-id="70c29-124">netBiosName</span></span>|<span data-ttu-id="70c29-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="70c29-125">String</span></span>|<span data-ttu-id="70c29-126">El nombre de host local, sin el nombre de dominio DNS.</span><span class="sxs-lookup"><span data-stu-id="70c29-126">The local host name, without the DNS domain name.</span></span>|
|<span data-ttu-id="70c29-127">sistema operativo</span><span class="sxs-lookup"><span data-stu-id="70c29-127">os</span></span>|<span data-ttu-id="70c29-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="70c29-128">String</span></span>|<span data-ttu-id="70c29-129">Sistema operativo del host.</span><span class="sxs-lookup"><span data-stu-id="70c29-129">Host Operating System.</span></span> <span data-ttu-id="70c29-130">(Por ejemplo, Windows10, Mac OS, RHEL, etcetera.).</span><span class="sxs-lookup"><span data-stu-id="70c29-130">(For example, Windows10, MacOS, RHEL, etc.).</span></span>|
|<span data-ttu-id="70c29-131">privateIpAddress</span><span class="sxs-lookup"><span data-stu-id="70c29-131">privateIpAddress</span></span>|<span data-ttu-id="70c29-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="70c29-132">String</span></span>|<span data-ttu-id="70c29-133">Dirección de IPv4 o IPv6 (no enrutable) privada (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) en el momento de la alerta.</span><span class="sxs-lookup"><span data-stu-id="70c29-133">Private (not routable) IPv4 or IPv6 address (see [RFC 1918](https://tools.ietf.org/html/rfc1918)) at the time of the alert.</span></span>|
|<span data-ttu-id="70c29-134">publicIpAddress</span><span class="sxs-lookup"><span data-stu-id="70c29-134">publicIpAddress</span></span>|<span data-ttu-id="70c29-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="70c29-135">String</span></span>|<span data-ttu-id="70c29-136">Dirección IPv4 o IPv6 enrutable públicamente (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) en el momento de la alerta.</span><span class="sxs-lookup"><span data-stu-id="70c29-136">Publicly routable IPv4 or IPv6 address (see [RFC 1918](https://tools.ietf.org/html/rfc1918)) at time of the alert.</span></span>|
|<span data-ttu-id="70c29-137">riskScore</span><span class="sxs-lookup"><span data-stu-id="70c29-137">riskScore</span></span>|<span data-ttu-id="70c29-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="70c29-138">String</span></span>|<span data-ttu-id="70c29-139">Puntuación de riesgo proveedor-generado/calculado del host.</span><span class="sxs-lookup"><span data-stu-id="70c29-139">Provider-generated/calculated risk score of the host.</span></span>  <span data-ttu-id="70c29-140">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="70c29-140">Recommended value range of 0-1, which equates to a percentage.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="70c29-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="70c29-141">JSON representation</span></span>

<span data-ttu-id="70c29-142">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="70c29-142">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.hostSecurityState"
}-->

```json
{
  "fqdn": "String",
  "isAzureAadJoined": true,
  "isAzureAadRegistered": true,
  "isHybridAzureDomainJoined": true,
  "netBiosName": "String",
  "os": "String",
  "privateIpAddress": "String",
  "publicIpAddress": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "hostSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
