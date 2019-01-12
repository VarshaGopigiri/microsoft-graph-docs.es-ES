---
title: tipo de recurso vppTokenLicenseSummary
description: Resumen de la licencia de una aplicación determinada en un símbolo (token).
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0766fd4da996b57032154be98bbc22fd8c8a4a5b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939962"
---
# <a name="vpptokenlicensesummary-resource-type"></a><span data-ttu-id="f02f4-103">tipo de recurso vppTokenLicenseSummary</span><span class="sxs-lookup"><span data-stu-id="f02f4-103">vppTokenLicenseSummary resource type</span></span>

> <span data-ttu-id="f02f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f02f4-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f02f4-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f02f4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f02f4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f02f4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f02f4-107">Resumen de la licencia de una aplicación determinada en un símbolo (token).</span><span class="sxs-lookup"><span data-stu-id="f02f4-107">License summary of a given app in a token.</span></span>
## <a name="properties"></a><span data-ttu-id="f02f4-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f02f4-108">Properties</span></span>
|<span data-ttu-id="f02f4-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f02f4-109">Property</span></span>|<span data-ttu-id="f02f4-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f02f4-110">Type</span></span>|<span data-ttu-id="f02f4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f02f4-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f02f4-112">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="f02f4-112">vppTokenId</span></span>|<span data-ttu-id="f02f4-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="f02f4-113">String</span></span>|<span data-ttu-id="f02f4-114">Identificador del token VPP.</span><span class="sxs-lookup"><span data-stu-id="f02f4-114">Identifier of the VPP token.</span></span>|
|<span data-ttu-id="f02f4-115">Id. de Apple</span><span class="sxs-lookup"><span data-stu-id="f02f4-115">appleId</span></span>|<span data-ttu-id="f02f4-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="f02f4-116">String</span></span>|<span data-ttu-id="f02f4-117">Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="f02f4-117">The Apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="f02f4-118">organizationName</span><span class="sxs-lookup"><span data-stu-id="f02f4-118">organizationName</span></span>|<span data-ttu-id="f02f4-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="f02f4-119">String</span></span>|<span data-ttu-id="f02f4-120">La organización asociada con el Token de programa de compra de Apple por volumen.</span><span class="sxs-lookup"><span data-stu-id="f02f4-120">The organization associated with the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="f02f4-121">availableLicenseCount</span><span class="sxs-lookup"><span data-stu-id="f02f4-121">availableLicenseCount</span></span>|<span data-ttu-id="f02f4-122">Int32</span><span class="sxs-lookup"><span data-stu-id="f02f4-122">Int32</span></span>|<span data-ttu-id="f02f4-123">El número de licencias VPP disponibles.</span><span class="sxs-lookup"><span data-stu-id="f02f4-123">The number of VPP licenses available.</span></span>|
|<span data-ttu-id="f02f4-124">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="f02f4-124">usedLicenseCount</span></span>|<span data-ttu-id="f02f4-125">Int32</span><span class="sxs-lookup"><span data-stu-id="f02f4-125">Int32</span></span>|<span data-ttu-id="f02f4-126">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="f02f4-126">The number of VPP licenses in use.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f02f4-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f02f4-127">Relationships</span></span>
<span data-ttu-id="f02f4-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f02f4-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f02f4-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f02f4-129">JSON Representation</span></span>
<span data-ttu-id="f02f4-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f02f4-130">Here is a JSON representation of the resource.</span></span>
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





