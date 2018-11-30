---
title: Tipo de recurso mimeContent
description: Contiene las propiedades de un contenido MIME genérico.
ms.openlocfilehash: cc0d024c814588479e641114ad33d19a5e609ecd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088862"
---
# <a name="mimecontent-resource-type"></a><span data-ttu-id="e48ef-103">Tipo de recurso mimeContent</span><span class="sxs-lookup"><span data-stu-id="e48ef-103">mimeContent resource type</span></span>

> <span data-ttu-id="e48ef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e48ef-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e48ef-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e48ef-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e48ef-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e48ef-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e48ef-107">Contiene las propiedades de un contenido MIME genérico.</span><span class="sxs-lookup"><span data-stu-id="e48ef-107">Contains properties for a generic mime content.</span></span>
## <a name="properties"></a><span data-ttu-id="e48ef-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e48ef-108">Properties</span></span>
|<span data-ttu-id="e48ef-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e48ef-109">Property</span></span>|<span data-ttu-id="e48ef-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e48ef-110">Type</span></span>|<span data-ttu-id="e48ef-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e48ef-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e48ef-112">type</span><span class="sxs-lookup"><span data-stu-id="e48ef-112">type</span></span>|<span data-ttu-id="e48ef-113">String</span><span class="sxs-lookup"><span data-stu-id="e48ef-113">String</span></span>|<span data-ttu-id="e48ef-114">Indica el tipo de contenido MIME.</span><span class="sxs-lookup"><span data-stu-id="e48ef-114">Indicates the content mime type.</span></span>|
|<span data-ttu-id="e48ef-115">valor</span><span class="sxs-lookup"><span data-stu-id="e48ef-115">value</span></span>|<span data-ttu-id="e48ef-116">Binario</span><span class="sxs-lookup"><span data-stu-id="e48ef-116">Binary</span></span>|<span data-ttu-id="e48ef-117">Matriz de bytes que contiene el contenido real.</span><span class="sxs-lookup"><span data-stu-id="e48ef-117">The byte array that contains the actual content.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e48ef-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e48ef-118">Relationships</span></span>
<span data-ttu-id="e48ef-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e48ef-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e48ef-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e48ef-120">JSON Representation</span></span>
<span data-ttu-id="e48ef-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e48ef-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mimeContent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mimeContent",
  "type": "String",
  "value": "binary"
}
```





