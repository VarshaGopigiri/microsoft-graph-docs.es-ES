---
title: tipo de recurso cloudAppSecurityState
description: Contiene información de estado acerca de la aplicación en la nube (destinationServiceName, destinationServiceIp).
localization_priority: Normal
ms.openlocfilehash: ff76adf1d3879c3dac3f19ae122d82c9523d5193
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850872"
---
# <a name="cloudappsecuritystate-resource-type"></a><span data-ttu-id="378b8-103">tipo de recurso cloudAppSecurityState</span><span class="sxs-lookup"><span data-stu-id="378b8-103">cloudAppSecurityState resource type</span></span>

<span data-ttu-id="378b8-104">Contiene información de estado acerca de la aplicación en la nube (destinationServiceName, destinationServiceIp).</span><span class="sxs-lookup"><span data-stu-id="378b8-104">Contains stateful information about the cloud application (destinationServiceName, destinationServiceIp).</span></span>

## <a name="properties"></a><span data-ttu-id="378b8-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="378b8-105">Properties</span></span>

| <span data-ttu-id="378b8-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="378b8-106">Property</span></span>     | <span data-ttu-id="378b8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="378b8-107">Type</span></span>        | <span data-ttu-id="378b8-108">Description</span><span class="sxs-lookup"><span data-stu-id="378b8-108">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="378b8-109">destinationServiceIp</span><span class="sxs-lookup"><span data-stu-id="378b8-109">destinationServiceIp</span></span>|<span data-ttu-id="378b8-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="378b8-110">String</span></span>|<span data-ttu-id="378b8-111">Dirección IP de destino de la conexión a la aplicación o servicio de nube.</span><span class="sxs-lookup"><span data-stu-id="378b8-111">Destination IP Address of the connection to the cloud application/service.</span></span>|
|<span data-ttu-id="378b8-112">destinationServiceName</span><span class="sxs-lookup"><span data-stu-id="378b8-112">destinationServiceName</span></span>|<span data-ttu-id="378b8-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="378b8-113">String</span></span>|<span data-ttu-id="378b8-114">Nombre de aplicación o servicio de nube (por ejemplo "Fuerza de ventas", "Lista desplegable", etcetera).</span><span class="sxs-lookup"><span data-stu-id="378b8-114">Cloud application/service name (for example "Salesforce", "DropBox", etc.).</span></span>|
|<span data-ttu-id="378b8-115">riskScore</span><span class="sxs-lookup"><span data-stu-id="378b8-115">riskScore</span></span>|<span data-ttu-id="378b8-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="378b8-116">String</span></span>|<span data-ttu-id="378b8-117">Puntuación de proveedor generado/calculada en el riesgo de la aplicación o servicio de nube.</span><span class="sxs-lookup"><span data-stu-id="378b8-117">Provider-generated/calculated risk score of the Cloud Application/Service.</span></span> <span data-ttu-id="378b8-118">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="378b8-118">Recommended value range of 0-1, which equates to a percentage.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="378b8-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="378b8-119">JSON representation</span></span>

<span data-ttu-id="378b8-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="378b8-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.cloudAppSecurityState"
}-->

```json
{
  "destinationServiceIp": "String",
  "destinationServiceName": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "cloudAppSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
