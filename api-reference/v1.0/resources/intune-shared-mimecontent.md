---
title: Tipo de recurso mimeContent
description: Contiene las propiedades de un contenido MIME genérico.
ms.openlocfilehash: 7f25a1c16b86a45886cd763c1a8a3aa6142c47e2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030202"
---
# <a name="mimecontent-resource-type"></a><span data-ttu-id="d33d6-103">Tipo de recurso mimeContent</span><span class="sxs-lookup"><span data-stu-id="d33d6-103">mimeContent resource type</span></span>

> <span data-ttu-id="d33d6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d33d6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d33d6-105">Contiene las propiedades de un contenido MIME genérico.</span><span class="sxs-lookup"><span data-stu-id="d33d6-105">Contains properties for a generic mime content.</span></span>
## <a name="properties"></a><span data-ttu-id="d33d6-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d33d6-106">Properties</span></span>
|<span data-ttu-id="d33d6-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d33d6-107">Property</span></span>|<span data-ttu-id="d33d6-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d33d6-108">Type</span></span>|<span data-ttu-id="d33d6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d33d6-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d33d6-110">type</span><span class="sxs-lookup"><span data-stu-id="d33d6-110">type</span></span>|<span data-ttu-id="d33d6-111">String</span><span class="sxs-lookup"><span data-stu-id="d33d6-111">String</span></span>|<span data-ttu-id="d33d6-112">Indica el tipo de contenido MIME.</span><span class="sxs-lookup"><span data-stu-id="d33d6-112">Indicates the content mime type.</span></span>|
|<span data-ttu-id="d33d6-113">valor</span><span class="sxs-lookup"><span data-stu-id="d33d6-113">value</span></span>|<span data-ttu-id="d33d6-114">Binario</span><span class="sxs-lookup"><span data-stu-id="d33d6-114">Binary</span></span>|<span data-ttu-id="d33d6-115">Matriz de bytes que contiene el contenido real.</span><span class="sxs-lookup"><span data-stu-id="d33d6-115">The byte array that contains the actual content.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d33d6-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d33d6-116">Relationships</span></span>
<span data-ttu-id="d33d6-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d33d6-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d33d6-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d33d6-118">JSON Representation</span></span>
<span data-ttu-id="d33d6-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d33d6-119">Here is a JSON representation of the resource.</span></span>
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



