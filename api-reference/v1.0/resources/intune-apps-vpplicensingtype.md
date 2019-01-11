---
title: Tipo de recurso vppLicensingType
description: Contiene las propiedades del tipo de licencia del Programa de Compras por Volumen (VPP) de iOS.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bbc52cfd4e14b2010dd133e4fa08e61a30fb63df
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814115"
---
# <a name="vpplicensingtype-resource-type"></a><span data-ttu-id="816b8-103">Tipo de recurso vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="816b8-103">vppLicensingType resource type</span></span>

> <span data-ttu-id="816b8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="816b8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="816b8-105">Contiene las propiedades del tipo de licencia del Programa de Compras por Volumen (VPP) de iOS.</span><span class="sxs-lookup"><span data-stu-id="816b8-105">Contains properties for iOS Volume-Purchased Program (Vpp) Licensing Type.</span></span>
## <a name="properties"></a><span data-ttu-id="816b8-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="816b8-106">Properties</span></span>
|<span data-ttu-id="816b8-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="816b8-107">Property</span></span>|<span data-ttu-id="816b8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="816b8-108">Type</span></span>|<span data-ttu-id="816b8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="816b8-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="816b8-110">supportsUserLicensing</span><span class="sxs-lookup"><span data-stu-id="816b8-110">supportsUserLicensing</span></span>|<span data-ttu-id="816b8-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="816b8-111">Boolean</span></span>|<span data-ttu-id="816b8-112">Si el programa es compatible con el tipo de licencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="816b8-112">Whether the program supports the user licensing type.</span></span>|
|<span data-ttu-id="816b8-113">supportsDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="816b8-113">supportsDeviceLicensing</span></span>|<span data-ttu-id="816b8-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="816b8-114">Boolean</span></span>|<span data-ttu-id="816b8-115">Si el programa es compatible con el tipo de licencia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="816b8-115">Whether the program supports the device licensing type.</span></span>|

## <a name="relationships"></a><span data-ttu-id="816b8-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="816b8-116">Relationships</span></span>
<span data-ttu-id="816b8-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="816b8-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="816b8-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="816b8-118">JSON Representation</span></span>
<span data-ttu-id="816b8-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="816b8-119">Here is a JSON representation of the resource.</span></span>
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



