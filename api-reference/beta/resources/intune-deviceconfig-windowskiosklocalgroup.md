---
title: tipo de recurso windowsKioskLocalGroup
description: La clase que se usa para identificar un grupo local para la configuración de quiosco
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f9c5d467e70b4e2e7f60bc4898be35a2e9fefadc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964756"
---
# <a name="windowskiosklocalgroup-resource-type"></a><span data-ttu-id="1a46f-103">tipo de recurso windowsKioskLocalGroup</span><span class="sxs-lookup"><span data-stu-id="1a46f-103">windowsKioskLocalGroup resource type</span></span>

> <span data-ttu-id="1a46f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1a46f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1a46f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1a46f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1a46f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1a46f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1a46f-107">La clase que se usa para identificar un grupo local para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="1a46f-107">The class used to identify a local group for the kiosk configuration</span></span>

<span data-ttu-id="1a46f-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="1a46f-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="1a46f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a46f-109">Properties</span></span>
|<span data-ttu-id="1a46f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1a46f-110">Property</span></span>|<span data-ttu-id="1a46f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1a46f-111">Type</span></span>|<span data-ttu-id="1a46f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a46f-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1a46f-113">groupName</span><span class="sxs-lookup"><span data-stu-id="1a46f-113">groupName</span></span>|<span data-ttu-id="1a46f-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a46f-114">String</span></span>|<span data-ttu-id="1a46f-115">El nombre del grupo local que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="1a46f-115">The name of the local group that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="1a46f-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1a46f-116">Relationships</span></span>
<span data-ttu-id="1a46f-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1a46f-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="1a46f-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1a46f-118">JSON Representation</span></span>
<span data-ttu-id="1a46f-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1a46f-119">Here is a JSON representation of the resource.</span></span>
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





