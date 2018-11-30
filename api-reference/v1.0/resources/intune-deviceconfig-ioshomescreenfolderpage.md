---
title: Tipo de recurso iosHomeScreenFolderPage
description: Una carpeta que contiene aplicaciones en la pantalla de inicio
ms.openlocfilehash: ce8332435f55ac4941c80ed60fdbf17f417e1008
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028609"
---
# <a name="ioshomescreenfolderpage-resource-type"></a><span data-ttu-id="78535-103">Tipo de recurso iosHomeScreenFolderPage</span><span class="sxs-lookup"><span data-stu-id="78535-103">iosHomeScreenFolderPage resource type</span></span>

> <span data-ttu-id="78535-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="78535-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="78535-105">Una carpeta que contiene aplicaciones en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="78535-105">A folder containing apps on the Home Screen</span></span>
## <a name="properties"></a><span data-ttu-id="78535-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78535-106">Properties</span></span>
|<span data-ttu-id="78535-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78535-107">Property</span></span>|<span data-ttu-id="78535-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="78535-108">Type</span></span>|<span data-ttu-id="78535-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="78535-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="78535-110">displayName</span><span class="sxs-lookup"><span data-stu-id="78535-110">displayName</span></span>|<span data-ttu-id="78535-111">cadena</span><span class="sxs-lookup"><span data-stu-id="78535-111">String</span></span>|<span data-ttu-id="78535-112">Nombre de la página de la carpeta</span><span class="sxs-lookup"><span data-stu-id="78535-112">Name of the folder page</span></span>|
|<span data-ttu-id="78535-113">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="78535-113">apps</span></span>|<span data-ttu-id="78535-114">Colección [iosHomeScreenApp](../resources/intune-deviceconfig-ioshomescreenapp.md)</span><span class="sxs-lookup"><span data-stu-id="78535-114">[iosHomeScreenApp](../resources/intune-deviceconfig-ioshomescreenapp.md) collection</span></span>|<span data-ttu-id="78535-115">Una lista de aplicaciones que aparecen en una página dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="78535-115">A list of apps to appear on a page within a folder.</span></span> <span data-ttu-id="78535-116">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="78535-116">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="78535-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="78535-117">Relationships</span></span>
<span data-ttu-id="78535-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="78535-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="78535-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="78535-119">JSON Representation</span></span>
<span data-ttu-id="78535-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="78535-120">Here is a JSON representation of the resource.</span></span>
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



