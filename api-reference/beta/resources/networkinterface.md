---
title: tipo de recurso networkInterface
description: Representa una tarjeta de interfaz de red (NIC) asociado con este host.
localization_priority: Normal
ms.openlocfilehash: 92ea26b76de8fa6ffbcdcf0bc64b85a08d0f51af
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823306"
---
# <a name="networkinterface-resource-type"></a><span data-ttu-id="9a356-103">tipo de recurso networkInterface</span><span class="sxs-lookup"><span data-stu-id="9a356-103">networkInterface resource type</span></span>

<span data-ttu-id="9a356-104">Representa una tarjeta de interfaz de red (NIC) asociado con este host.</span><span class="sxs-lookup"><span data-stu-id="9a356-104">Represents a Network Interface Card (NIC) associated with this host.</span></span>

## <a name="properties"></a><span data-ttu-id="9a356-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a356-105">Properties</span></span>

| <span data-ttu-id="9a356-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9a356-106">Property</span></span>   | <span data-ttu-id="9a356-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a356-107">Type</span></span> |<span data-ttu-id="9a356-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a356-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a356-109">description</span><span class="sxs-lookup"><span data-stu-id="9a356-109">description</span></span>|<span data-ttu-id="9a356-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="9a356-110">String</span></span>|<span data-ttu-id="9a356-111">Descripción de la NIC (por ejemplo, adaptador Ethernet, conexión de área Local del adaptador de red LAN inalámbrica \* <> #, etcetera.).</span><span class="sxs-lookup"><span data-stu-id="9a356-111">Description of the NIC (e.g. Ethernet adapter, Wireless LAN adapter Local Area Connection \*<#>, etc.).</span></span>|
|<span data-ttu-id="9a356-112">ipV4Address</span><span class="sxs-lookup"><span data-stu-id="9a356-112">ipV4Address</span></span>|<span data-ttu-id="9a356-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="9a356-113">String</span></span>|<span data-ttu-id="9a356-114">Última dirección IPv4 asociado con esta NIC.</span><span class="sxs-lookup"><span data-stu-id="9a356-114">Last IPv4 address associated with this NIC.</span></span>|
|<span data-ttu-id="9a356-115">ipV6Address</span><span class="sxs-lookup"><span data-stu-id="9a356-115">ipV6Address</span></span>|<span data-ttu-id="9a356-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="9a356-116">String</span></span>|<span data-ttu-id="9a356-117">Última pública (también conocido como) dirección IPv6 global asociado con esta NIC.</span><span class="sxs-lookup"><span data-stu-id="9a356-117">Last Public (aka global) IPv6 address associated with this NIC.</span></span>|
|<span data-ttu-id="9a356-118">localIpV6Address</span><span class="sxs-lookup"><span data-stu-id="9a356-118">localIpV6Address</span></span>|<span data-ttu-id="9a356-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="9a356-119">String</span></span>|<span data-ttu-id="9a356-120">Última local (local de vínculo o local del sitio) dirección IPv6 asociada con esta NIC.</span><span class="sxs-lookup"><span data-stu-id="9a356-120">Last local (link-local or site-local) IPv6 address associated with this NIC.</span></span>|
|<span data-ttu-id="9a356-121">dirección MAC</span><span class="sxs-lookup"><span data-stu-id="9a356-121">macAddress</span></span>|<span data-ttu-id="9a356-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="9a356-122">String</span></span>|<span data-ttu-id="9a356-123">Dirección MAC de la NIC en este host.</span><span class="sxs-lookup"><span data-stu-id="9a356-123">MAC address of the NIC on this host.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9a356-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9a356-124">JSON representation</span></span>

<span data-ttu-id="9a356-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9a356-125">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.networkInterface"
}-->

```json
{
  "description": "String",
  "ipV4Address": "String",
  "ipV6Address": "String",
  "localIpV6Address": "String",
  "macAddress": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "networkInterface resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
