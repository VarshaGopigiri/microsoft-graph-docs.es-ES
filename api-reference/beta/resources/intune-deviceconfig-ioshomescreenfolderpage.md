---
title: Tipo de recurso iosHomeScreenFolderPage
description: Una carpeta que contiene aplicaciones en la pantalla de inicio
ms.openlocfilehash: 7cf34cd3bbd4f196db70da3a88ba3768c3d4d630
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084610"
---
# <a name="ioshomescreenfolderpage-resource-type"></a><span data-ttu-id="c35de-103">Tipo de recurso iosHomeScreenFolderPage</span><span class="sxs-lookup"><span data-stu-id="c35de-103">iosHomeScreenFolderPage resource type</span></span>

> <span data-ttu-id="c35de-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c35de-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c35de-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c35de-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c35de-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c35de-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c35de-107">Una carpeta que contiene aplicaciones en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="c35de-107">A folder containing apps on the Home Screen</span></span>
## <a name="properties"></a><span data-ttu-id="c35de-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c35de-108">Properties</span></span>
|<span data-ttu-id="c35de-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c35de-109">Property</span></span>|<span data-ttu-id="c35de-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c35de-110">Type</span></span>|<span data-ttu-id="c35de-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c35de-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c35de-112">displayName</span><span class="sxs-lookup"><span data-stu-id="c35de-112">displayName</span></span>|<span data-ttu-id="c35de-113">cadena</span><span class="sxs-lookup"><span data-stu-id="c35de-113">String</span></span>|<span data-ttu-id="c35de-114">Nombre de la página de la carpeta</span><span class="sxs-lookup"><span data-stu-id="c35de-114">Name of the folder page</span></span>|
|<span data-ttu-id="c35de-115">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c35de-115">apps</span></span>|<span data-ttu-id="c35de-116">Colección [iosHomeScreenApp](../resources/intune-deviceconfig-ioshomescreenapp.md)</span><span class="sxs-lookup"><span data-stu-id="c35de-116">[iosHomeScreenApp](../resources/intune-deviceconfig-ioshomescreenapp.md) collection</span></span>|<span data-ttu-id="c35de-117">Una lista de aplicaciones que aparecen en una página dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c35de-117">A list of apps to appear on a page within a folder.</span></span> <span data-ttu-id="c35de-118">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="c35de-118">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c35de-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c35de-119">Relationships</span></span>
<span data-ttu-id="c35de-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c35de-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c35de-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c35de-121">JSON Representation</span></span>
<span data-ttu-id="c35de-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c35de-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosHomeScreenFolderPage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenFolderPage",
  "displayName": "String",
  "apps": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenApp",
      "displayName": "String",
      "bundleID": "String"
    }
  ]
}
```





