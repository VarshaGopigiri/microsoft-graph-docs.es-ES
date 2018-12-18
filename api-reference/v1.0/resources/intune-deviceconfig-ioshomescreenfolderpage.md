---
title: Tipo de recurso iosHomeScreenFolderPage
description: Una carpeta que contiene aplicaciones en la pantalla de inicio
author: tfitzmac
ms.openlocfilehash: 147504fc356f3a4092b2ffd1c7d03275ff7dea31
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353644"
---
# <a name="ioshomescreenfolderpage-resource-type"></a><span data-ttu-id="34e7b-103">Tipo de recurso iosHomeScreenFolderPage</span><span class="sxs-lookup"><span data-stu-id="34e7b-103">iosHomeScreenFolderPage resource type</span></span>

> <span data-ttu-id="34e7b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="34e7b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="34e7b-105">Una carpeta que contiene aplicaciones en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="34e7b-105">A folder containing apps on the Home Screen</span></span>
## <a name="properties"></a><span data-ttu-id="34e7b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34e7b-106">Properties</span></span>
|<span data-ttu-id="34e7b-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34e7b-107">Property</span></span>|<span data-ttu-id="34e7b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="34e7b-108">Type</span></span>|<span data-ttu-id="34e7b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="34e7b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="34e7b-110">displayName</span><span class="sxs-lookup"><span data-stu-id="34e7b-110">displayName</span></span>|<span data-ttu-id="34e7b-111">cadena</span><span class="sxs-lookup"><span data-stu-id="34e7b-111">String</span></span>|<span data-ttu-id="34e7b-112">Nombre de la página de la carpeta</span><span class="sxs-lookup"><span data-stu-id="34e7b-112">Name of the folder page</span></span>|
|<span data-ttu-id="34e7b-113">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="34e7b-113">apps</span></span>|<span data-ttu-id="34e7b-114">Colección [iosHomeScreenApp](../resources/intune-deviceconfig-ioshomescreenapp.md)</span><span class="sxs-lookup"><span data-stu-id="34e7b-114">[iosHomeScreenApp](../resources/intune-deviceconfig-ioshomescreenapp.md) collection</span></span>|<span data-ttu-id="34e7b-115">Una lista de aplicaciones que aparecen en una página dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="34e7b-115">A list of apps to appear on a page within a folder.</span></span> <span data-ttu-id="34e7b-116">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="34e7b-116">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="34e7b-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="34e7b-117">Relationships</span></span>
<span data-ttu-id="34e7b-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="34e7b-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="34e7b-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="34e7b-119">JSON Representation</span></span>
<span data-ttu-id="34e7b-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="34e7b-120">Here is a JSON representation of the resource.</span></span>
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



