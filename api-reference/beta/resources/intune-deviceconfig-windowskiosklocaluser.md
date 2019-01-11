---
title: tipo de recurso windowsKioskLocalUser
description: La clase que se usa para identificar una cuenta local para la configuración de quiosco
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7ab6a9dc0e3ea63ed5d9f60bb48b005aa98acab1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844558"
---
# <a name="windowskiosklocaluser-resource-type"></a><span data-ttu-id="787c3-103">tipo de recurso windowsKioskLocalUser</span><span class="sxs-lookup"><span data-stu-id="787c3-103">windowsKioskLocalUser resource type</span></span>

> <span data-ttu-id="787c3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="787c3-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="787c3-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="787c3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="787c3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="787c3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="787c3-107">La clase que se usa para identificar una cuenta local para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="787c3-107">The class used to identify a local account for the kiosk configuration</span></span>

<span data-ttu-id="787c3-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="787c3-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="787c3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="787c3-109">Properties</span></span>
|<span data-ttu-id="787c3-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="787c3-110">Property</span></span>|<span data-ttu-id="787c3-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="787c3-111">Type</span></span>|<span data-ttu-id="787c3-112">Description</span><span class="sxs-lookup"><span data-stu-id="787c3-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="787c3-113">userName</span><span class="sxs-lookup"><span data-stu-id="787c3-113">userName</span></span>|<span data-ttu-id="787c3-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="787c3-114">String</span></span>|<span data-ttu-id="787c3-115">El usuario local que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="787c3-115">The local user that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="787c3-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="787c3-116">Relationships</span></span>
<span data-ttu-id="787c3-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="787c3-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="787c3-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="787c3-118">JSON Representation</span></span>
<span data-ttu-id="787c3-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="787c3-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskLocalUser"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskLocalUser",
  "userName": "String"
}
```





