---
title: tipo de recurso windowsKioskAzureADGroup
description: La clase que se usa para identificar un grupo de AzureAD para la configuración de quiosco
ms.openlocfilehash: 4853013c9c1e9d4c276ee5e2ba83cb8b36afd06c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083618"
---
# <a name="windowskioskazureadgroup-resource-type"></a><span data-ttu-id="ff2f7-103">tipo de recurso windowsKioskAzureADGroup</span><span class="sxs-lookup"><span data-stu-id="ff2f7-103">windowsKioskAzureADGroup resource type</span></span>

> <span data-ttu-id="ff2f7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff2f7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ff2f7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ff2f7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ff2f7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ff2f7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ff2f7-107">La clase que se usa para identificar un grupo de AzureAD para la configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="ff2f7-107">The class used to identify an AzureAD group for the kiosk configuration</span></span>

<span data-ttu-id="ff2f7-108">Hereda de [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span><span class="sxs-lookup"><span data-stu-id="ff2f7-108">Inherits from [windowsKioskUser](../resources/intune-deviceconfig-windowskioskuser.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ff2f7-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff2f7-109">Properties</span></span>
|<span data-ttu-id="ff2f7-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff2f7-110">Property</span></span>|<span data-ttu-id="ff2f7-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff2f7-111">Type</span></span>|<span data-ttu-id="ff2f7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff2f7-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ff2f7-113">displayName</span><span class="sxs-lookup"><span data-stu-id="ff2f7-113">displayName</span></span>|<span data-ttu-id="ff2f7-114">String</span><span class="sxs-lookup"><span data-stu-id="ff2f7-114">String</span></span>|<span data-ttu-id="ff2f7-115">El nombre para mostrar del grupo AzureAD que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="ff2f7-115">The display name of the AzureAD group that will be locked to this kiosk configuration</span></span>|
|<span data-ttu-id="ff2f7-116">groupId</span><span class="sxs-lookup"><span data-stu-id="ff2f7-116">groupId</span></span>|<span data-ttu-id="ff2f7-117">String</span><span class="sxs-lookup"><span data-stu-id="ff2f7-117">String</span></span>|<span data-ttu-id="ff2f7-118">El identificador del grupo AzureAD que se bloqueará a esta configuración de quiosco</span><span class="sxs-lookup"><span data-stu-id="ff2f7-118">The ID of the AzureAD group that will be locked to this kiosk configuration</span></span>|

## <a name="relationships"></a><span data-ttu-id="ff2f7-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ff2f7-119">Relationships</span></span>
<span data-ttu-id="ff2f7-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ff2f7-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ff2f7-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ff2f7-121">JSON Representation</span></span>
<span data-ttu-id="ff2f7-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ff2f7-122">Here is a JSON representation of the resource.</span></span>
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





