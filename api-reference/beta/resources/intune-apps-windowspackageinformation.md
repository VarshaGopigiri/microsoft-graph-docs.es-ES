---
title: tipo de recurso windowsPackageInformation
description: Contiene las propiedades de la información del paquete para una línea de aplicación empresarial de Windows.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0f7f3cd593670e071ae62bdb287bcebeee01d555
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849535"
---
# <a name="windowspackageinformation-resource-type"></a><span data-ttu-id="a1314-103">tipo de recurso windowsPackageInformation</span><span class="sxs-lookup"><span data-stu-id="a1314-103">windowsPackageInformation resource type</span></span>

> <span data-ttu-id="a1314-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a1314-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a1314-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a1314-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a1314-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a1314-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a1314-107">Contiene las propiedades de la información del paquete para una línea de aplicación empresarial de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1314-107">Contains properties for the package information for a Windows line of business app.</span></span>
## <a name="properties"></a><span data-ttu-id="a1314-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1314-108">Properties</span></span>
|<span data-ttu-id="a1314-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a1314-109">Property</span></span>|<span data-ttu-id="a1314-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1314-110">Type</span></span>|<span data-ttu-id="a1314-111">Description</span><span class="sxs-lookup"><span data-stu-id="a1314-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a1314-112">applicableArchitecture</span><span class="sxs-lookup"><span data-stu-id="a1314-112">applicableArchitecture</span></span>|[<span data-ttu-id="a1314-113">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="a1314-113">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="a1314-114">La arquitectura de Windows para la que se puede ejecutar esta aplicación en.</span><span class="sxs-lookup"><span data-stu-id="a1314-114">The Windows architecture for which this app can run on.</span></span> <span data-ttu-id="a1314-115">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="a1314-115">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="a1314-116">displayName</span><span class="sxs-lookup"><span data-stu-id="a1314-116">displayName</span></span>|<span data-ttu-id="a1314-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="a1314-117">String</span></span>|<span data-ttu-id="a1314-118">El nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="a1314-118">The Display Name.</span></span>|
|<span data-ttu-id="a1314-119">identityName</span><span class="sxs-lookup"><span data-stu-id="a1314-119">identityName</span></span>|<span data-ttu-id="a1314-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="a1314-120">String</span></span>|<span data-ttu-id="a1314-121">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="a1314-121">The Identity Name.</span></span>|
|<span data-ttu-id="a1314-122">identityPublisher</span><span class="sxs-lookup"><span data-stu-id="a1314-122">identityPublisher</span></span>|<span data-ttu-id="a1314-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="a1314-123">String</span></span>|<span data-ttu-id="a1314-124">El publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="a1314-124">The Identity Publisher.</span></span>|
|<span data-ttu-id="a1314-125">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="a1314-125">identityResourceIdentifier</span></span>|<span data-ttu-id="a1314-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="a1314-126">String</span></span>|<span data-ttu-id="a1314-127">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="a1314-127">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="a1314-128">identityVersion</span><span class="sxs-lookup"><span data-stu-id="a1314-128">identityVersion</span></span>|<span data-ttu-id="a1314-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="a1314-129">String</span></span>|<span data-ttu-id="a1314-130">La versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="a1314-130">The Identity Version.</span></span>|
|<span data-ttu-id="a1314-131">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a1314-131">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="a1314-132">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a1314-132">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="a1314-133">El valor para el sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="a1314-133">The value for the minimum applicable operating system.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a1314-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a1314-134">Relationships</span></span>
<span data-ttu-id="a1314-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a1314-135">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a1314-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a1314-136">JSON Representation</span></span>
<span data-ttu-id="a1314-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a1314-137">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsPackageInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsPackageInformation",
  "applicableArchitecture": "String",
  "displayName": "String",
  "identityName": "String",
  "identityPublisher": "String",
  "identityResourceIdentifier": "String",
  "identityVersion": "String",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  }
}
```





