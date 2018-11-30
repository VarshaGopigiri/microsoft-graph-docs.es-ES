---
title: tipo de recurso androidPermissionAction
description: Asignación entre un permiso de aplicación de Android y la acción Android debe realizar cuando se solicita ese permiso.
ms.openlocfilehash: e65f9b28169e231e34b5a7a46316821f77639233
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085175"
---
# <a name="androidpermissionaction-resource-type"></a><span data-ttu-id="6d227-103">tipo de recurso androidPermissionAction</span><span class="sxs-lookup"><span data-stu-id="6d227-103">androidPermissionAction resource type</span></span>

> <span data-ttu-id="6d227-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6d227-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6d227-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6d227-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6d227-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6d227-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6d227-107">Asignación entre un permiso de aplicación de Android y la acción Android debe realizar cuando se solicita ese permiso.</span><span class="sxs-lookup"><span data-stu-id="6d227-107">Mapping between an Android app permission and the action Android should take when that permission is requested.</span></span>
## <a name="properties"></a><span data-ttu-id="6d227-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6d227-108">Properties</span></span>
|<span data-ttu-id="6d227-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6d227-109">Property</span></span>|<span data-ttu-id="6d227-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d227-110">Type</span></span>|<span data-ttu-id="6d227-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d227-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6d227-112">permiso</span><span class="sxs-lookup"><span data-stu-id="6d227-112">permission</span></span>|<span data-ttu-id="6d227-113">String</span><span class="sxs-lookup"><span data-stu-id="6d227-113">String</span></span>|<span data-ttu-id="6d227-114">Cadena de permiso Android, definida en la documentación oficial de Android.</span><span class="sxs-lookup"><span data-stu-id="6d227-114">Android permission string, defined in the official Android documentation.</span></span>  <span data-ttu-id="6d227-115">Ejemplo 'android.permission.READ_CONTACTS'.</span><span class="sxs-lookup"><span data-stu-id="6d227-115">Example 'android.permission.READ_CONTACTS'.</span></span>|
|<span data-ttu-id="6d227-116">action</span><span class="sxs-lookup"><span data-stu-id="6d227-116">action</span></span>|[<span data-ttu-id="6d227-117">androidPermissionActionType</span><span class="sxs-lookup"><span data-stu-id="6d227-117">androidPermissionActionType</span></span>](../resources/intune-apps-androidpermissionactiontype.md)|<span data-ttu-id="6d227-118">Tipo de acción de permiso Android.</span><span class="sxs-lookup"><span data-stu-id="6d227-118">Type of Android permission action.</span></span> <span data-ttu-id="6d227-119">Los valores posibles son: `prompt`, `autoGrant` y `autoDeny`.</span><span class="sxs-lookup"><span data-stu-id="6d227-119">Possible values are: `prompt`, `autoGrant`, `autoDeny`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6d227-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6d227-120">Relationships</span></span>
<span data-ttu-id="6d227-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6d227-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6d227-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6d227-122">JSON Representation</span></span>
<span data-ttu-id="6d227-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6d227-123">Here is a JSON representation of the resource.</span></span>
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





