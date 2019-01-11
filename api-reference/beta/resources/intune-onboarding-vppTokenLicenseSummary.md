---
title: tipo de recurso vppTokenLicenseSummary
description: Resumen de la licencia de una aplicación determinada en un símbolo (token).
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e5972341aa3b390ae226d19f7d85fe918345c627
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824867"
---
# <a name="vpptokenlicensesummary-resource-type"></a><span data-ttu-id="cde0a-103">tipo de recurso vppTokenLicenseSummary</span><span class="sxs-lookup"><span data-stu-id="cde0a-103">vppTokenLicenseSummary resource type</span></span>

> <span data-ttu-id="cde0a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cde0a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cde0a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cde0a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cde0a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cde0a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cde0a-107">Resumen de la licencia de una aplicación determinada en un símbolo (token).</span><span class="sxs-lookup"><span data-stu-id="cde0a-107">License summary of a given app in a token.</span></span>
## <a name="properties"></a><span data-ttu-id="cde0a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cde0a-108">Properties</span></span>
|<span data-ttu-id="cde0a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cde0a-109">Property</span></span>|<span data-ttu-id="cde0a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="cde0a-110">Type</span></span>|<span data-ttu-id="cde0a-111">Description</span><span class="sxs-lookup"><span data-stu-id="cde0a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cde0a-112">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="cde0a-112">vppTokenId</span></span>|<span data-ttu-id="cde0a-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="cde0a-113">String</span></span>|<span data-ttu-id="cde0a-114">Identificador del token VPP.</span><span class="sxs-lookup"><span data-stu-id="cde0a-114">Identifier of the VPP token.</span></span>|
|<span data-ttu-id="cde0a-115">Id. de Apple</span><span class="sxs-lookup"><span data-stu-id="cde0a-115">appleId</span></span>|<span data-ttu-id="cde0a-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="cde0a-116">String</span></span>|<span data-ttu-id="cde0a-117">Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="cde0a-117">The Apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="cde0a-118">organizationName</span><span class="sxs-lookup"><span data-stu-id="cde0a-118">organizationName</span></span>|<span data-ttu-id="cde0a-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="cde0a-119">String</span></span>|<span data-ttu-id="cde0a-120">La organización asociada con el Token de programa de compra de Apple por volumen.</span><span class="sxs-lookup"><span data-stu-id="cde0a-120">The organization associated with the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="cde0a-121">availableLicenseCount</span><span class="sxs-lookup"><span data-stu-id="cde0a-121">availableLicenseCount</span></span>|<span data-ttu-id="cde0a-122">Int32</span><span class="sxs-lookup"><span data-stu-id="cde0a-122">Int32</span></span>|<span data-ttu-id="cde0a-123">El número de licencias VPP disponibles.</span><span class="sxs-lookup"><span data-stu-id="cde0a-123">The number of VPP licenses available.</span></span>|
|<span data-ttu-id="cde0a-124">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="cde0a-124">usedLicenseCount</span></span>|<span data-ttu-id="cde0a-125">Int32</span><span class="sxs-lookup"><span data-stu-id="cde0a-125">Int32</span></span>|<span data-ttu-id="cde0a-126">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="cde0a-126">The number of VPP licenses in use.</span></span>|

## <a name="relationships"></a><span data-ttu-id="cde0a-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cde0a-127">Relationships</span></span>
<span data-ttu-id="cde0a-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cde0a-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="cde0a-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cde0a-129">JSON Representation</span></span>
<span data-ttu-id="cde0a-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cde0a-130">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vppTokenLicenseSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vppTokenLicenseSummary",
  "vppTokenId": "String",
  "appleId": "String",
  "organizationName": "String",
  "availableLicenseCount": 1024,
  "usedLicenseCount": 1024
}
```





