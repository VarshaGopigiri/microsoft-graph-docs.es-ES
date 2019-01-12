---
title: Tipo de recurso edgeSearchEngineBase
description: Permite que los administradores de TI configuren un motor de búsqueda predeterminado para dispositivos controlados por MDM. Los usuarios pueden invalidarla y cambiar su motor de búsqueda predeterminado, siempre que no se establezca la directiva AllowSearchEngineCustomization.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ed27e057c6801bb1800f4ceb97bc74c779032dbe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969684"
---
# <a name="edgesearchenginebase-resource-type"></a><span data-ttu-id="53d5e-104">Tipo de recurso edgeSearchEngineBase</span><span class="sxs-lookup"><span data-stu-id="53d5e-104">edgeSearchEngineBase resource type</span></span>

> <span data-ttu-id="53d5e-105">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="53d5e-105">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53d5e-106">Permite a los administradores de TI configurar un motor de búsqueda predeterminado para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="53d5e-106">Allows IT admins to set a default search engine for MDM-Controlled devices.</span></span> <span data-ttu-id="53d5e-107">Los usuarios pueden invalidarlo y cambiar su motor de búsqueda predeterminado, siempre que no se establezca la directiva AllowSearchEngineCustomization.</span><span class="sxs-lookup"><span data-stu-id="53d5e-107">Users can override this and change their default search engine provided the AllowSearchEngineCustomization policy is not set.</span></span>
## <a name="properties"></a><span data-ttu-id="53d5e-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53d5e-108">Properties</span></span>
|<span data-ttu-id="53d5e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53d5e-109">Property</span></span>|<span data-ttu-id="53d5e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="53d5e-110">Type</span></span>|<span data-ttu-id="53d5e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="53d5e-111">Description</span></span>|
|:---|:---|:---|

## <a name="relationships"></a><span data-ttu-id="53d5e-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="53d5e-112">Relationships</span></span>
<span data-ttu-id="53d5e-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="53d5e-113">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="53d5e-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="53d5e-114">JSON Representation</span></span>
<span data-ttu-id="53d5e-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="53d5e-115">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.edgeSearchEngineBase"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.edgeSearchEngineBase"
}
```



