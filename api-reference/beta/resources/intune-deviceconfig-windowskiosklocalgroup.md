---
title: tipo de recurso windowsKioskLocalGroup
description: La clase que se usa para identificar un grupo local para la configuración de quiosco
ms.openlocfilehash: 456460e60bbf21130fc918f38922893e5430abe8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083621"
---
# <a name="windowskiosklocalgroup-resource-type"></a><span data-ttu-id="5453f-103">tipo de recurso windowsKioskLocalGroup</span><span class="sxs-lookup"><span data-stu-id="5453f-103">windowsKioskLocalGroup resource type</span></span>

> <span data-ttu-id="5453f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5453f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5453f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5453f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5453f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5453f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5453f-107">La clase que se usa para identificar un grupo local para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="5453f-107">The class used to identify a local group for the kiosk configuration</span></span>

<span data-ttu-id="5453f-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="5453f-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="5453f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5453f-109">Properties</span></span>
|<span data-ttu-id="5453f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5453f-110">Property</span></span>|<span data-ttu-id="5453f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="5453f-111">Type</span></span>|<span data-ttu-id="5453f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5453f-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5453f-113">groupName</span><span class="sxs-lookup"><span data-stu-id="5453f-113">groupName</span></span>|<span data-ttu-id="5453f-114">String</span><span class="sxs-lookup"><span data-stu-id="5453f-114">String</span></span>|<span data-ttu-id="5453f-115">El nombre del grupo local que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="5453f-115">The name of the local group that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="5453f-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5453f-116">Relationships</span></span>
<span data-ttu-id="5453f-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5453f-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5453f-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5453f-118">JSON Representation</span></span>
<span data-ttu-id="5453f-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5453f-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskLocalGroup"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskLocalGroup",
  "groupName": "String"
}
```





