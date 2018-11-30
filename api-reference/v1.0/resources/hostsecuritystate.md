---
title: tipo de recurso hostSecurityState
description: Contiene información de estado acerca del host (incluidos los dispositivos, equipos y así sucesivamente).
ms.openlocfilehash: 3649553ae0f96222a09825e8819dfd0d199f8454
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031391"
---
# <a name="hostsecuritystate-resource-type"></a><span data-ttu-id="2111e-103">tipo de recurso hostSecurityState</span><span class="sxs-lookup"><span data-stu-id="2111e-103">hostSecurityState resource type</span></span>

<span data-ttu-id="2111e-104">Contiene información de estado acerca del host (incluidos los dispositivos, equipos y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="2111e-104">Contains stateful information about the host (including devices, computers, and so on).</span></span>

## <a name="properties"></a><span data-ttu-id="2111e-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2111e-105">Properties</span></span>

| <span data-ttu-id="2111e-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2111e-106">Property</span></span>   | <span data-ttu-id="2111e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="2111e-107">Type</span></span>|<span data-ttu-id="2111e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2111e-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2111e-109">FQDN</span><span class="sxs-lookup"><span data-stu-id="2111e-109">fqdn</span></span>|<span data-ttu-id="2111e-110">String</span><span class="sxs-lookup"><span data-stu-id="2111e-110">String</span></span>|<span data-ttu-id="2111e-111">FQDN (nombre de dominio completo) de host (por ejemplo, `machine.company.com`).</span><span class="sxs-lookup"><span data-stu-id="2111e-111">Host FQDN (Fully Qualified Domain Name) (for example, `machine.company.com`).</span></span>|
|<span data-ttu-id="2111e-112">isAzureAadJoined</span><span class="sxs-lookup"><span data-stu-id="2111e-112">isAzureAadJoined</span></span>|<span data-ttu-id="2111e-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="2111e-113">Boolean</span></span>|<span data-ttu-id="2111e-114">Es True si el host es el dominio unido a Azure los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2111e-114">True if the host is domain joined to Azure Active Directory Domain Services.</span></span>|
|<span data-ttu-id="2111e-115">isAzureAadRegistered</span><span class="sxs-lookup"><span data-stu-id="2111e-115">isAzureAadRegistered</span></span>|<span data-ttu-id="2111e-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="2111e-116">Boolean</span></span>|<span data-ttu-id="2111e-117">Es True si el host registrado con Azure Active Directory dispositivo de registro (BYOD dispositivos - es decir, no totalmente administrados por empresa).</span><span class="sxs-lookup"><span data-stu-id="2111e-117">True if the host registered with Azure Active Directory Device Registration (BYOD devices - that is, not fully managed by enterprise).</span></span>|
|<span data-ttu-id="2111e-118">isHybridAzureDomainJoined</span><span class="sxs-lookup"><span data-stu-id="2111e-118">isHybridAzureDomainJoined</span></span>|<span data-ttu-id="2111e-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="2111e-119">Boolean</span></span>|<span data-ttu-id="2111e-120">Es True si el host está unido a un dominio de Active Directory local de dominio.</span><span class="sxs-lookup"><span data-stu-id="2111e-120">True if the host is domain joined to an on-premises Active Directory domain.</span></span>|
|<span data-ttu-id="2111e-121">nombreNetBIOS</span><span class="sxs-lookup"><span data-stu-id="2111e-121">netBiosName</span></span>|<span data-ttu-id="2111e-122">String</span><span class="sxs-lookup"><span data-stu-id="2111e-122">String</span></span>|<span data-ttu-id="2111e-123">El nombre de host local, sin el nombre de dominio DNS.</span><span class="sxs-lookup"><span data-stu-id="2111e-123">The local host name, without the DNS domain name.</span></span>|
|<span data-ttu-id="2111e-124">sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2111e-124">os</span></span>|<span data-ttu-id="2111e-125">String</span><span class="sxs-lookup"><span data-stu-id="2111e-125">String</span></span>|<span data-ttu-id="2111e-126">Sistema operativo del host.</span><span class="sxs-lookup"><span data-stu-id="2111e-126">Host Operating System.</span></span> <span data-ttu-id="2111e-127">(Por ejemplo, Windows10, Mac OS, RHEL, etcetera.).</span><span class="sxs-lookup"><span data-stu-id="2111e-127">(For example, Windows10, MacOS, RHEL, etc.).</span></span>|
|<span data-ttu-id="2111e-128">privateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2111e-128">privateIpAddress</span></span>|<span data-ttu-id="2111e-129">String</span><span class="sxs-lookup"><span data-stu-id="2111e-129">String</span></span>|<span data-ttu-id="2111e-130">Dirección de IPv4 o IPv6 (no enrutable) privada (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) en el momento de la alerta.</span><span class="sxs-lookup"><span data-stu-id="2111e-130">Private (not routable) IPv4 or IPv6 address (see [RFC 1918](https://tools.ietf.org/html/rfc1918)) at the time of the alert.</span></span>|
|<span data-ttu-id="2111e-131">publicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2111e-131">publicIpAddress</span></span>|<span data-ttu-id="2111e-132">String</span><span class="sxs-lookup"><span data-stu-id="2111e-132">String</span></span>|<span data-ttu-id="2111e-133">Dirección IPv4 o IPv6 enrutable públicamente (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) en el momento de la alerta.</span><span class="sxs-lookup"><span data-stu-id="2111e-133">Publicly routable IPv4 or IPv6 address (see [RFC 1918](https://tools.ietf.org/html/rfc1918)) at time of the alert.</span></span>|
|<span data-ttu-id="2111e-134">riskScore</span><span class="sxs-lookup"><span data-stu-id="2111e-134">riskScore</span></span>|<span data-ttu-id="2111e-135">String</span><span class="sxs-lookup"><span data-stu-id="2111e-135">String</span></span>|<span data-ttu-id="2111e-136">Puntuación de riesgo proveedor-generado/calculado del host.</span><span class="sxs-lookup"><span data-stu-id="2111e-136">Provider-generated/calculated risk score of the host.</span></span>  <span data-ttu-id="2111e-137">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="2111e-137">Recommended value range of 0-1, which equates to a percentage.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2111e-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2111e-138">JSON representation</span></span>

<span data-ttu-id="2111e-139">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2111e-139">The following is a JSON representation of the resource.</span></span>

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