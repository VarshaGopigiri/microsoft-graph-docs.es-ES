---
title: Tipo de recurso iosHomeScreenItem
description: Representa un elemento en la pantalla principal de iOS
author: tfitzmac
ms.openlocfilehash: 6a8d71e01ca8f2c284bcc3eddd7eb39b87c025d7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27328192"
---
# <a name="ioshomescreenitem-resource-type"></a><span data-ttu-id="8d725-103">Tipo de recurso iosHomeScreenItem</span><span class="sxs-lookup"><span data-stu-id="8d725-103">iosHomeScreenItem resource type</span></span>

> <span data-ttu-id="8d725-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8d725-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8d725-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8d725-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8d725-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d725-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d725-107">Representa un elemento en la pantalla principal de iOS</span><span class="sxs-lookup"><span data-stu-id="8d725-107">Represents an item on the iOS Home Screen</span></span>
## <a name="properties"></a><span data-ttu-id="8d725-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d725-108">Properties</span></span>
|<span data-ttu-id="8d725-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d725-109">Property</span></span>|<span data-ttu-id="8d725-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d725-110">Type</span></span>|<span data-ttu-id="8d725-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d725-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d725-112">displayName</span><span class="sxs-lookup"><span data-stu-id="8d725-112">displayName</span></span>|<span data-ttu-id="8d725-113">cadena</span><span class="sxs-lookup"><span data-stu-id="8d725-113">String</span></span>|<span data-ttu-id="8d725-114">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8d725-114">Name of the app</span></span>|

## <a name="relationships"></a><span data-ttu-id="8d725-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8d725-115">Relationships</span></span>
<span data-ttu-id="8d725-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8d725-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8d725-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d725-117">JSON Representation</span></span>
<span data-ttu-id="8d725-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d725-118">Here is a JSON representation of the resource.</span></span>
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





