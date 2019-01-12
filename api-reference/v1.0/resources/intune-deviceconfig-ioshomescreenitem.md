---
title: Tipo de recurso iosHomeScreenItem
description: Representa un elemento en la pantalla principal de iOS
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ff573a6f7ae0d78113a32514bc312c3920b216f1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987625"
---
# <a name="ioshomescreenitem-resource-type"></a><span data-ttu-id="751fb-103">Tipo de recurso iosHomeScreenItem</span><span class="sxs-lookup"><span data-stu-id="751fb-103">iosHomeScreenItem resource type</span></span>

> <span data-ttu-id="751fb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="751fb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="751fb-105">Representa un elemento en la pantalla principal de iOS</span><span class="sxs-lookup"><span data-stu-id="751fb-105">Represents an item on the iOS Home Screen</span></span>
## <a name="properties"></a><span data-ttu-id="751fb-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="751fb-106">Properties</span></span>
|<span data-ttu-id="751fb-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="751fb-107">Property</span></span>|<span data-ttu-id="751fb-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="751fb-108">Type</span></span>|<span data-ttu-id="751fb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="751fb-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="751fb-110">displayName</span><span class="sxs-lookup"><span data-stu-id="751fb-110">displayName</span></span>|<span data-ttu-id="751fb-111">cadena</span><span class="sxs-lookup"><span data-stu-id="751fb-111">String</span></span>|<span data-ttu-id="751fb-112">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="751fb-112">Name of the app</span></span>|

## <a name="relationships"></a><span data-ttu-id="751fb-113">Relaciones</span><span class="sxs-lookup"><span data-stu-id="751fb-113">Relationships</span></span>
<span data-ttu-id="751fb-114">Ninguna</span><span class="sxs-lookup"><span data-stu-id="751fb-114">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="751fb-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="751fb-115">JSON Representation</span></span>
<span data-ttu-id="751fb-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="751fb-116">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosHomeScreenItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenItem",
  "displayName": "String"
}
```



