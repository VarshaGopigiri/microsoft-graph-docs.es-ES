---
title: Tipo de recurso edgeSearchEngineBase
description: Permite que los administradores de TI configuren un motor de búsqueda predeterminado para dispositivos controlados por MDM. Los usuarios pueden invalidarla y cambiar su motor de búsqueda predeterminado, siempre que no se establezca la directiva AllowSearchEngineCustomization.
ms.openlocfilehash: b6f006d1bdedc2b6fafaf29565fff6b3dcbb0a5b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088362"
---
# <a name="edgesearchenginebase-resource-type"></a><span data-ttu-id="7719d-104">Tipo de recurso edgeSearchEngineBase</span><span class="sxs-lookup"><span data-stu-id="7719d-104">edgeSearchEngineBase resource type</span></span>

> <span data-ttu-id="7719d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7719d-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7719d-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7719d-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7719d-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7719d-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7719d-108">Permite a los administradores de TI configurar un motor de búsqueda predeterminado para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="7719d-108">Allows IT admins to set a default search engine for MDM-Controlled devices.</span></span> <span data-ttu-id="7719d-109">Los usuarios pueden invalidarlo y cambiar su motor de búsqueda predeterminado, siempre que no se establezca la directiva AllowSearchEngineCustomization.</span><span class="sxs-lookup"><span data-stu-id="7719d-109">Users can override this and change their default search engine provided the AllowSearchEngineCustomization policy is not set.</span></span>
## <a name="properties"></a><span data-ttu-id="7719d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7719d-110">Properties</span></span>
|<span data-ttu-id="7719d-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7719d-111">Property</span></span>|<span data-ttu-id="7719d-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="7719d-112">Type</span></span>|<span data-ttu-id="7719d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="7719d-113">Description</span></span>|
|:---|:---|:---|

## <a name="relationships"></a><span data-ttu-id="7719d-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7719d-114">Relationships</span></span>
<span data-ttu-id="7719d-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7719d-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7719d-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7719d-116">JSON Representation</span></span>
<span data-ttu-id="7719d-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7719d-117">Here is a JSON representation of the resource.</span></span>
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





