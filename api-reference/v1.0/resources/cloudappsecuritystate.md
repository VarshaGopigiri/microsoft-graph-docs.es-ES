---
title: tipo de recurso cloudAppSecurityState
description: Contiene información de estado acerca de la aplicación en la nube (destinationServiceName, destinationServiceIp).
ms.openlocfilehash: 915044c3084e3d9a9435d602ecc7ec809d2168f2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032365"
---
# <a name="cloudappsecuritystate-resource-type"></a><span data-ttu-id="a7878-103">tipo de recurso cloudAppSecurityState</span><span class="sxs-lookup"><span data-stu-id="a7878-103">cloudAppSecurityState resource type</span></span>

<span data-ttu-id="a7878-104">Contiene información de estado acerca de la aplicación en la nube (destinationServiceName, destinationServiceIp).</span><span class="sxs-lookup"><span data-stu-id="a7878-104">Contains stateful information about the cloud application (destinationServiceName, destinationServiceIp).</span></span>

## <a name="properties"></a><span data-ttu-id="a7878-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7878-105">Properties</span></span>

| <span data-ttu-id="a7878-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7878-106">Property</span></span>     | <span data-ttu-id="a7878-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7878-107">Type</span></span>        | <span data-ttu-id="a7878-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7878-108">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="a7878-109">destinationServiceIp</span><span class="sxs-lookup"><span data-stu-id="a7878-109">destinationServiceIp</span></span>|<span data-ttu-id="a7878-110">String</span><span class="sxs-lookup"><span data-stu-id="a7878-110">String</span></span>|<span data-ttu-id="a7878-111">Dirección IP de destino de la conexión a la aplicación o servicio de nube.</span><span class="sxs-lookup"><span data-stu-id="a7878-111">Destination IP Address of the connection to the cloud application/service.</span></span>|
|<span data-ttu-id="a7878-112">destinationServiceName</span><span class="sxs-lookup"><span data-stu-id="a7878-112">destinationServiceName</span></span>|<span data-ttu-id="a7878-113">String</span><span class="sxs-lookup"><span data-stu-id="a7878-113">String</span></span>|<span data-ttu-id="a7878-114">Nombre de aplicación o servicio de nube (por ejemplo "Fuerza de ventas", "Lista desplegable", etcetera).</span><span class="sxs-lookup"><span data-stu-id="a7878-114">Cloud application/service name (for example "Salesforce", "DropBox", etc.).</span></span>|
|<span data-ttu-id="a7878-115">riskScore</span><span class="sxs-lookup"><span data-stu-id="a7878-115">riskScore</span></span>|<span data-ttu-id="a7878-116">String</span><span class="sxs-lookup"><span data-stu-id="a7878-116">String</span></span>|<span data-ttu-id="a7878-117">Puntuación de proveedor generado/calculada en el riesgo de la aplicación o servicio de nube.</span><span class="sxs-lookup"><span data-stu-id="a7878-117">Provider-generated/calculated risk score of the Cloud Application/Service.</span></span> <span data-ttu-id="a7878-118">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="a7878-118">Recommended value range of 0-1, which equates to a percentage.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a7878-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a7878-119">JSON representation</span></span>

<span data-ttu-id="a7878-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a7878-120">The following is a JSON representation of the resource.</span></span>

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