---
title: tipo de recurso win32LobAppMsiInformation
description: Contiene propiedades de la aplicación MSI para una aplicación de Win32.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e43b3dc9e46ed193b7547a7ce85863253445d30c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846518"
---
# <a name="win32lobappmsiinformation-resource-type"></a><span data-ttu-id="1db7f-103">tipo de recurso win32LobAppMsiInformation</span><span class="sxs-lookup"><span data-stu-id="1db7f-103">win32LobAppMsiInformation resource type</span></span>

> <span data-ttu-id="1db7f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1db7f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1db7f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1db7f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1db7f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1db7f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1db7f-107">Contiene propiedades de la aplicación MSI para una aplicación de Win32.</span><span class="sxs-lookup"><span data-stu-id="1db7f-107">Contains MSI app properties for a Win32 App.</span></span>
## <a name="properties"></a><span data-ttu-id="1db7f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1db7f-108">Properties</span></span>
|<span data-ttu-id="1db7f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1db7f-109">Property</span></span>|<span data-ttu-id="1db7f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="1db7f-110">Type</span></span>|<span data-ttu-id="1db7f-111">Description</span><span class="sxs-lookup"><span data-stu-id="1db7f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1db7f-112">productCode</span><span class="sxs-lookup"><span data-stu-id="1db7f-112">productCode</span></span>|<span data-ttu-id="1db7f-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="1db7f-113">String</span></span>|<span data-ttu-id="1db7f-114">El código de producto MSI.</span><span class="sxs-lookup"><span data-stu-id="1db7f-114">The MSI product code.</span></span>|
|<span data-ttu-id="1db7f-115">productVersion</span><span class="sxs-lookup"><span data-stu-id="1db7f-115">productVersion</span></span>|<span data-ttu-id="1db7f-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="1db7f-116">String</span></span>|<span data-ttu-id="1db7f-117">La versión del producto MSI.</span><span class="sxs-lookup"><span data-stu-id="1db7f-117">The MSI product version.</span></span>|
|<span data-ttu-id="1db7f-118">upgradeCode</span><span class="sxs-lookup"><span data-stu-id="1db7f-118">upgradeCode</span></span>|<span data-ttu-id="1db7f-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="1db7f-119">String</span></span>|<span data-ttu-id="1db7f-120">El código de actualización MSI.</span><span class="sxs-lookup"><span data-stu-id="1db7f-120">The MSI upgrade code.</span></span>|
|<span data-ttu-id="1db7f-121">requiresReboot</span><span class="sxs-lookup"><span data-stu-id="1db7f-121">requiresReboot</span></span>|<span data-ttu-id="1db7f-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="1db7f-122">Boolean</span></span>|<span data-ttu-id="1db7f-123">Si la aplicación MSI requiere que el equipo que reiniciar para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="1db7f-123">Whether the MSI app requires the machine to reboot to complete installation.</span></span>|
|<span data-ttu-id="1db7f-124">packageType</span><span class="sxs-lookup"><span data-stu-id="1db7f-124">packageType</span></span>|[<span data-ttu-id="1db7f-125">win32LobAppMsiPackageType</span><span class="sxs-lookup"><span data-stu-id="1db7f-125">win32LobAppMsiPackageType</span></span>](../resources/intune-apps-win32lobappmsipackagetype.md)|<span data-ttu-id="1db7f-126">El tipo de paquete MSI.</span><span class="sxs-lookup"><span data-stu-id="1db7f-126">The MSI package type.</span></span> <span data-ttu-id="1db7f-127">Los valores posibles son: `perMachine`, `perUser` y `dualPurpose`.</span><span class="sxs-lookup"><span data-stu-id="1db7f-127">Possible values are: `perMachine`, `perUser`, `dualPurpose`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="1db7f-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1db7f-128">Relationships</span></span>
<span data-ttu-id="1db7f-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1db7f-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="1db7f-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1db7f-130">JSON Representation</span></span>
<span data-ttu-id="1db7f-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1db7f-131">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppMsiInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppMsiInformation",
  "productCode": "String",
  "productVersion": "String",
  "upgradeCode": "String",
  "requiresReboot": true,
  "packageType": "String"
}
```





