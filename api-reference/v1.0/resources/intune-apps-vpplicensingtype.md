---
title: Tipo de recurso vppLicensingType
description: Contiene las propiedades del tipo de licencia del Programa de Compras por Volumen (VPP) de iOS.
author: tfitzmac
ms.openlocfilehash: 7958266fe208e0a04bc72ab658291c58455c763b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27322564"
---
# <a name="vpplicensingtype-resource-type"></a><span data-ttu-id="8128a-103">Tipo de recurso vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="8128a-103">vppLicensingType resource type</span></span>

> <span data-ttu-id="8128a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8128a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8128a-105">Contiene las propiedades del tipo de licencia del Programa de Compras por Volumen (VPP) de iOS.</span><span class="sxs-lookup"><span data-stu-id="8128a-105">Contains properties for iOS Volume-Purchased Program (Vpp) Licensing Type.</span></span>
## <a name="properties"></a><span data-ttu-id="8128a-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8128a-106">Properties</span></span>
|<span data-ttu-id="8128a-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8128a-107">Property</span></span>|<span data-ttu-id="8128a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8128a-108">Type</span></span>|<span data-ttu-id="8128a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8128a-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8128a-110">supportsUserLicensing</span><span class="sxs-lookup"><span data-stu-id="8128a-110">supportsUserLicensing</span></span>|<span data-ttu-id="8128a-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="8128a-111">Boolean</span></span>|<span data-ttu-id="8128a-112">Si el programa es compatible con el tipo de licencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="8128a-112">Whether the program supports the user licensing type.</span></span>|
|<span data-ttu-id="8128a-113">supportsDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="8128a-113">supportsDeviceLicensing</span></span>|<span data-ttu-id="8128a-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="8128a-114">Boolean</span></span>|<span data-ttu-id="8128a-115">Si el programa es compatible con el tipo de licencia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8128a-115">Whether the program supports the device licensing type.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8128a-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8128a-116">Relationships</span></span>
<span data-ttu-id="8128a-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8128a-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8128a-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8128a-118">JSON Representation</span></span>
<span data-ttu-id="8128a-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8128a-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vppLicensingType"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vppLicensingType",
  "supportsUserLicensing": true,
  "supportsDeviceLicensing": true
}
```



