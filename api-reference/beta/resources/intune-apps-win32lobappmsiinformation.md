---
title: tipo de recurso win32LobAppMsiInformation
description: Contiene propiedades de la aplicación MSI para una aplicación de Win32.
ms.openlocfilehash: a5563d369d68a881f1b519c50dd9722ad864d7cf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090346"
---
# <a name="win32lobappmsiinformation-resource-type"></a><span data-ttu-id="7ca3e-103">tipo de recurso win32LobAppMsiInformation</span><span class="sxs-lookup"><span data-stu-id="7ca3e-103">win32LobAppMsiInformation resource type</span></span>

> <span data-ttu-id="7ca3e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7ca3e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7ca3e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7ca3e-107">Contiene propiedades de la aplicación MSI para una aplicación de Win32.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-107">Contains MSI app properties for a Win32 App.</span></span>
## <a name="properties"></a><span data-ttu-id="7ca3e-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ca3e-108">Properties</span></span>
|<span data-ttu-id="7ca3e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7ca3e-109">Property</span></span>|<span data-ttu-id="7ca3e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ca3e-110">Type</span></span>|<span data-ttu-id="7ca3e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ca3e-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7ca3e-112">productCode</span><span class="sxs-lookup"><span data-stu-id="7ca3e-112">productCode</span></span>|<span data-ttu-id="7ca3e-113">String</span><span class="sxs-lookup"><span data-stu-id="7ca3e-113">String</span></span>|<span data-ttu-id="7ca3e-114">El código de producto MSI.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-114">The MSI product code.</span></span>|
|<span data-ttu-id="7ca3e-115">productVersion</span><span class="sxs-lookup"><span data-stu-id="7ca3e-115">productVersion</span></span>|<span data-ttu-id="7ca3e-116">String</span><span class="sxs-lookup"><span data-stu-id="7ca3e-116">String</span></span>|<span data-ttu-id="7ca3e-117">La versión del producto MSI.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-117">The MSI product version.</span></span>|
|<span data-ttu-id="7ca3e-118">upgradeCode</span><span class="sxs-lookup"><span data-stu-id="7ca3e-118">upgradeCode</span></span>|<span data-ttu-id="7ca3e-119">String</span><span class="sxs-lookup"><span data-stu-id="7ca3e-119">String</span></span>|<span data-ttu-id="7ca3e-120">El código de actualización MSI.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-120">The MSI upgrade code.</span></span>|
|<span data-ttu-id="7ca3e-121">requiresReboot</span><span class="sxs-lookup"><span data-stu-id="7ca3e-121">requiresReboot</span></span>|<span data-ttu-id="7ca3e-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="7ca3e-122">Boolean</span></span>|<span data-ttu-id="7ca3e-123">Si la aplicación MSI requiere que el equipo que reiniciar para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-123">Whether the MSI app requires the machine to reboot to complete installation.</span></span>|
|<span data-ttu-id="7ca3e-124">packageType</span><span class="sxs-lookup"><span data-stu-id="7ca3e-124">packageType</span></span>|[<span data-ttu-id="7ca3e-125">win32LobAppMsiPackageType</span><span class="sxs-lookup"><span data-stu-id="7ca3e-125">win32LobAppMsiPackageType</span></span>](../resources/intune-apps-win32lobappmsipackagetype.md)|<span data-ttu-id="7ca3e-126">El tipo de paquete MSI.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-126">The MSI package type.</span></span> <span data-ttu-id="7ca3e-127">Los valores posibles son: `perMachine`, `perUser` y `dualPurpose`.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-127">Possible values are: `perMachine`, `perUser`, `dualPurpose`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7ca3e-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7ca3e-128">Relationships</span></span>
<span data-ttu-id="7ca3e-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7ca3e-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7ca3e-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7ca3e-130">JSON Representation</span></span>
<span data-ttu-id="7ca3e-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-131">Here is a JSON representation of the resource.</span></span>
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





