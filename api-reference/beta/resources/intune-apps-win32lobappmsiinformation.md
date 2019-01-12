---
title: tipo de recurso win32LobAppMsiInformation
description: Contiene propiedades de la aplicación MSI para una aplicación de Win32.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 04972e9e7fa909c220fe55ca6337be3ac44138ad
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967878"
---
# <a name="win32lobappmsiinformation-resource-type"></a><span data-ttu-id="11152-103">tipo de recurso win32LobAppMsiInformation</span><span class="sxs-lookup"><span data-stu-id="11152-103">win32LobAppMsiInformation resource type</span></span>

> <span data-ttu-id="11152-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11152-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11152-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11152-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="11152-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11152-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11152-107">Contiene propiedades de la aplicación MSI para una aplicación de Win32.</span><span class="sxs-lookup"><span data-stu-id="11152-107">Contains MSI app properties for a Win32 App.</span></span>
## <a name="properties"></a><span data-ttu-id="11152-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11152-108">Properties</span></span>
|<span data-ttu-id="11152-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11152-109">Property</span></span>|<span data-ttu-id="11152-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="11152-110">Type</span></span>|<span data-ttu-id="11152-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="11152-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11152-112">productCode</span><span class="sxs-lookup"><span data-stu-id="11152-112">productCode</span></span>|<span data-ttu-id="11152-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="11152-113">String</span></span>|<span data-ttu-id="11152-114">El código de producto MSI.</span><span class="sxs-lookup"><span data-stu-id="11152-114">The MSI product code.</span></span>|
|<span data-ttu-id="11152-115">productVersion</span><span class="sxs-lookup"><span data-stu-id="11152-115">productVersion</span></span>|<span data-ttu-id="11152-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="11152-116">String</span></span>|<span data-ttu-id="11152-117">La versión del producto MSI.</span><span class="sxs-lookup"><span data-stu-id="11152-117">The MSI product version.</span></span>|
|<span data-ttu-id="11152-118">upgradeCode</span><span class="sxs-lookup"><span data-stu-id="11152-118">upgradeCode</span></span>|<span data-ttu-id="11152-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="11152-119">String</span></span>|<span data-ttu-id="11152-120">El código de actualización MSI.</span><span class="sxs-lookup"><span data-stu-id="11152-120">The MSI upgrade code.</span></span>|
|<span data-ttu-id="11152-121">requiresReboot</span><span class="sxs-lookup"><span data-stu-id="11152-121">requiresReboot</span></span>|<span data-ttu-id="11152-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="11152-122">Boolean</span></span>|<span data-ttu-id="11152-123">Si la aplicación MSI requiere que el equipo que reiniciar para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="11152-123">Whether the MSI app requires the machine to reboot to complete installation.</span></span>|
|<span data-ttu-id="11152-124">packageType</span><span class="sxs-lookup"><span data-stu-id="11152-124">packageType</span></span>|[<span data-ttu-id="11152-125">win32LobAppMsiPackageType</span><span class="sxs-lookup"><span data-stu-id="11152-125">win32LobAppMsiPackageType</span></span>](../resources/intune-apps-win32lobappmsipackagetype.md)|<span data-ttu-id="11152-126">El tipo de paquete MSI.</span><span class="sxs-lookup"><span data-stu-id="11152-126">The MSI package type.</span></span> <span data-ttu-id="11152-127">Los valores posibles son: `perMachine`, `perUser` y `dualPurpose`.</span><span class="sxs-lookup"><span data-stu-id="11152-127">Possible values are: `perMachine`, `perUser`, `dualPurpose`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="11152-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="11152-128">Relationships</span></span>
<span data-ttu-id="11152-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="11152-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="11152-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="11152-130">JSON Representation</span></span>
<span data-ttu-id="11152-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="11152-131">Here is a JSON representation of the resource.</span></span>
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





