---
title: tipo de recurso windowsKioskLocalUser
description: La clase que se usa para identificar una cuenta local para la configuración de quiosco
author: tfitzmac
ms.openlocfilehash: 5ac98147172fd08fc9914a7d9302e3b074ca3246
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310825"
---
# <a name="windowskiosklocaluser-resource-type"></a><span data-ttu-id="3c41c-103">tipo de recurso windowsKioskLocalUser</span><span class="sxs-lookup"><span data-stu-id="3c41c-103">windowsKioskLocalUser resource type</span></span>

> <span data-ttu-id="3c41c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3c41c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3c41c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3c41c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3c41c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3c41c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3c41c-107">La clase que se usa para identificar una cuenta local para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="3c41c-107">The class used to identify a local account for the kiosk configuration</span></span>

<span data-ttu-id="3c41c-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="3c41c-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="3c41c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c41c-109">Properties</span></span>
|<span data-ttu-id="3c41c-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3c41c-110">Property</span></span>|<span data-ttu-id="3c41c-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c41c-111">Type</span></span>|<span data-ttu-id="3c41c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c41c-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3c41c-113">userName</span><span class="sxs-lookup"><span data-stu-id="3c41c-113">userName</span></span>|<span data-ttu-id="3c41c-114">String</span><span class="sxs-lookup"><span data-stu-id="3c41c-114">String</span></span>|<span data-ttu-id="3c41c-115">El usuario local que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="3c41c-115">The local user that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="3c41c-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3c41c-116">Relationships</span></span>
<span data-ttu-id="3c41c-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3c41c-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3c41c-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3c41c-118">JSON Representation</span></span>
<span data-ttu-id="3c41c-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3c41c-119">Here is a JSON representation of the resource.</span></span>
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





