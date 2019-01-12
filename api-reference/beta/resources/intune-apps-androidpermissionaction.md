---
title: tipo de recurso androidPermissionAction
description: Asignación entre un permiso de aplicación de Android y la acción Android debe realizar cuando se solicita ese permiso.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5ad7b438951b947cc515f1472dd1eae8caf472f2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977125"
---
# <a name="androidpermissionaction-resource-type"></a><span data-ttu-id="177a0-103">tipo de recurso androidPermissionAction</span><span class="sxs-lookup"><span data-stu-id="177a0-103">androidPermissionAction resource type</span></span>

> <span data-ttu-id="177a0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="177a0-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="177a0-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="177a0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="177a0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="177a0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="177a0-107">Asignación entre un permiso de aplicación de Android y la acción Android debe realizar cuando se solicita ese permiso.</span><span class="sxs-lookup"><span data-stu-id="177a0-107">Mapping between an Android app permission and the action Android should take when that permission is requested.</span></span>
## <a name="properties"></a><span data-ttu-id="177a0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="177a0-108">Properties</span></span>
|<span data-ttu-id="177a0-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="177a0-109">Property</span></span>|<span data-ttu-id="177a0-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="177a0-110">Type</span></span>|<span data-ttu-id="177a0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="177a0-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="177a0-112">permiso</span><span class="sxs-lookup"><span data-stu-id="177a0-112">permission</span></span>|<span data-ttu-id="177a0-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="177a0-113">String</span></span>|<span data-ttu-id="177a0-114">Cadena de permiso Android, definida en la documentación oficial de Android.</span><span class="sxs-lookup"><span data-stu-id="177a0-114">Android permission string, defined in the official Android documentation.</span></span>  <span data-ttu-id="177a0-115">Ejemplo 'android.permission.READ_CONTACTS'.</span><span class="sxs-lookup"><span data-stu-id="177a0-115">Example 'android.permission.READ_CONTACTS'.</span></span>|
|<span data-ttu-id="177a0-116">action</span><span class="sxs-lookup"><span data-stu-id="177a0-116">action</span></span>|[<span data-ttu-id="177a0-117">androidPermissionActionType</span><span class="sxs-lookup"><span data-stu-id="177a0-117">androidPermissionActionType</span></span>](../resources/intune-apps-androidpermissionactiontype.md)|<span data-ttu-id="177a0-118">Tipo de acción de permiso Android.</span><span class="sxs-lookup"><span data-stu-id="177a0-118">Type of Android permission action.</span></span> <span data-ttu-id="177a0-119">Los valores posibles son: `prompt`, `autoGrant` y `autoDeny`.</span><span class="sxs-lookup"><span data-stu-id="177a0-119">Possible values are: `prompt`, `autoGrant`, `autoDeny`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="177a0-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="177a0-120">Relationships</span></span>
<span data-ttu-id="177a0-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="177a0-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="177a0-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="177a0-122">JSON Representation</span></span>
<span data-ttu-id="177a0-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="177a0-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidPermissionAction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidPermissionAction",
  "permission": "String",
  "action": "String"
}
```





