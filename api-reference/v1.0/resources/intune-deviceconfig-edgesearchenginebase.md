---
title: Tipo de recurso edgeSearchEngineBase
description: Permite que los administradores de TI configuren un motor de búsqueda predeterminado para dispositivos controlados por MDM. Los usuarios pueden invalidarla y cambiar su motor de búsqueda predeterminado, siempre que no se establezca la directiva AllowSearchEngineCustomization.
ms.openlocfilehash: 505816652890cd72c61b91001dbce2061b76fc11
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029079"
---
# <a name="edgesearchenginebase-resource-type"></a><span data-ttu-id="d4c8f-104">Tipo de recurso edgeSearchEngineBase</span><span class="sxs-lookup"><span data-stu-id="d4c8f-104">edgeSearchEngineBase resource type</span></span>

> <span data-ttu-id="d4c8f-105">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d4c8f-105">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d4c8f-106">Permite a los administradores de TI configurar un motor de búsqueda predeterminado para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="d4c8f-106">Allows IT admins to set a default search engine for MDM-Controlled devices.</span></span> <span data-ttu-id="d4c8f-107">Los usuarios pueden invalidarlo y cambiar su motor de búsqueda predeterminado, siempre que no se establezca la directiva AllowSearchEngineCustomization.</span><span class="sxs-lookup"><span data-stu-id="d4c8f-107">Users can override this and change their default search engine provided the AllowSearchEngineCustomization policy is not set.</span></span>
## <a name="properties"></a><span data-ttu-id="d4c8f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4c8f-108">Properties</span></span>
|<span data-ttu-id="d4c8f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4c8f-109">Property</span></span>|<span data-ttu-id="d4c8f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4c8f-110">Type</span></span>|<span data-ttu-id="d4c8f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4c8f-111">Description</span></span>|
|:---|:---|:---|

## <a name="relationships"></a><span data-ttu-id="d4c8f-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d4c8f-112">Relationships</span></span>
<span data-ttu-id="d4c8f-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d4c8f-113">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d4c8f-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d4c8f-114">JSON Representation</span></span>
<span data-ttu-id="d4c8f-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d4c8f-115">Here is a JSON representation of the resource.</span></span>
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



