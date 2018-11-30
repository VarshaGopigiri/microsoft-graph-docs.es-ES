---
title: tipo de recurso vppTokenLicenseSummary
description: Resumen de la licencia de una aplicación determinada en un símbolo (token).
ms.openlocfilehash: fba888c706b21a796615bf9bc2ea79968d5ad6d0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084800"
---
# <a name="vpptokenlicensesummary-resource-type"></a><span data-ttu-id="553d7-103">tipo de recurso vppTokenLicenseSummary</span><span class="sxs-lookup"><span data-stu-id="553d7-103">vppTokenLicenseSummary resource type</span></span>

> <span data-ttu-id="553d7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="553d7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="553d7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="553d7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="553d7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="553d7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="553d7-107">Resumen de la licencia de una aplicación determinada en un símbolo (token).</span><span class="sxs-lookup"><span data-stu-id="553d7-107">License summary of a given app in a token.</span></span>
## <a name="properties"></a><span data-ttu-id="553d7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="553d7-108">Properties</span></span>
|<span data-ttu-id="553d7-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="553d7-109">Property</span></span>|<span data-ttu-id="553d7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="553d7-110">Type</span></span>|<span data-ttu-id="553d7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="553d7-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="553d7-112">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="553d7-112">vppTokenId</span></span>|<span data-ttu-id="553d7-113">String</span><span class="sxs-lookup"><span data-stu-id="553d7-113">String</span></span>|<span data-ttu-id="553d7-114">Identificador del token VPP.</span><span class="sxs-lookup"><span data-stu-id="553d7-114">Identifier of the VPP token.</span></span>|
|<span data-ttu-id="553d7-115">Id. de Apple</span><span class="sxs-lookup"><span data-stu-id="553d7-115">appleId</span></span>|<span data-ttu-id="553d7-116">String</span><span class="sxs-lookup"><span data-stu-id="553d7-116">String</span></span>|<span data-ttu-id="553d7-117">Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="553d7-117">The Apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="553d7-118">organizationName</span><span class="sxs-lookup"><span data-stu-id="553d7-118">organizationName</span></span>|<span data-ttu-id="553d7-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="553d7-119">String</span></span>|<span data-ttu-id="553d7-120">La organización asociada con el Token de programa de compra de Apple por volumen.</span><span class="sxs-lookup"><span data-stu-id="553d7-120">The organization associated with the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="553d7-121">availableLicenseCount</span><span class="sxs-lookup"><span data-stu-id="553d7-121">availableLicenseCount</span></span>|<span data-ttu-id="553d7-122">Int32</span><span class="sxs-lookup"><span data-stu-id="553d7-122">Int32</span></span>|<span data-ttu-id="553d7-123">El número de licencias VPP disponibles.</span><span class="sxs-lookup"><span data-stu-id="553d7-123">The number of VPP licenses available.</span></span>|
|<span data-ttu-id="553d7-124">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="553d7-124">usedLicenseCount</span></span>|<span data-ttu-id="553d7-125">Int32</span><span class="sxs-lookup"><span data-stu-id="553d7-125">Int32</span></span>|<span data-ttu-id="553d7-126">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="553d7-126">The number of VPP licenses in use.</span></span>|

## <a name="relationships"></a><span data-ttu-id="553d7-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="553d7-127">Relationships</span></span>
<span data-ttu-id="553d7-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="553d7-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="553d7-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="553d7-129">JSON Representation</span></span>
<span data-ttu-id="553d7-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="553d7-130">Here is a JSON representation of the resource.</span></span>
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





