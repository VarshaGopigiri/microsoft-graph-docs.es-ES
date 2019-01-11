---
title: tipo de recurso windowsKioskAzureADGroup
description: La clase que se usa para identificar un grupo de AzureAD para la configuración de quiosco
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 16c2b17220a92f9f230b786238b1195e2af48d6b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849871"
---
# <a name="windowskioskazureadgroup-resource-type"></a><span data-ttu-id="b17a3-103">tipo de recurso windowsKioskAzureADGroup</span><span class="sxs-lookup"><span data-stu-id="b17a3-103">windowsKioskAzureADGroup resource type</span></span>

> <span data-ttu-id="b17a3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b17a3-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b17a3-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b17a3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b17a3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b17a3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b17a3-107">La clase que se usa para identificar un grupo de AzureAD para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="b17a3-107">The class used to identify an AzureAD group for the kiosk configuration</span></span>

<span data-ttu-id="b17a3-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="b17a3-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="b17a3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b17a3-109">Properties</span></span>
|<span data-ttu-id="b17a3-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b17a3-110">Property</span></span>|<span data-ttu-id="b17a3-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b17a3-111">Type</span></span>|<span data-ttu-id="b17a3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b17a3-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b17a3-113">displayName</span><span class="sxs-lookup"><span data-stu-id="b17a3-113">displayName</span></span>|<span data-ttu-id="b17a3-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="b17a3-114">String</span></span>|<span data-ttu-id="b17a3-115">El nombre para mostrar del grupo AzureAD que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="b17a3-115">The display name of the AzureAD group that will be locked to this kiosk configuration</span></span>|
|<span data-ttu-id="b17a3-116">groupId</span><span class="sxs-lookup"><span data-stu-id="b17a3-116">groupId</span></span>|<span data-ttu-id="b17a3-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="b17a3-117">String</span></span>|<span data-ttu-id="b17a3-118">El identificador del grupo AzureAD que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="b17a3-118">The ID of the AzureAD group that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="b17a3-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b17a3-119">Relationships</span></span>
<span data-ttu-id="b17a3-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b17a3-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b17a3-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b17a3-121">JSON Representation</span></span>
<span data-ttu-id="b17a3-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b17a3-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsKioskAzureADGroup"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsKioskAzureADGroup",
  "displayName": "String",
  "groupId": "String"
}
```





