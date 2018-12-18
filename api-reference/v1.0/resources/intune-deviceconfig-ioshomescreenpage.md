---
title: Tipo de recurso iosHomeScreenPage
description: Una página que contiene aplicaciones y carpetas en la pantalla de inicio
author: tfitzmac
ms.openlocfilehash: b8aca5c671d0c8521cdf8a870a2f0ad3cd35ba1b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321465"
---
# <a name="ioshomescreenpage-resource-type"></a><span data-ttu-id="4cd3c-103">Tipo de recurso iosHomeScreenPage</span><span class="sxs-lookup"><span data-stu-id="4cd3c-103">iosHomeScreenPage resource type</span></span>

> <span data-ttu-id="4cd3c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4cd3c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4cd3c-105">Una página que contiene aplicaciones y carpetas en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="4cd3c-105">A page containing apps and folders on the Home Screen</span></span>
## <a name="properties"></a><span data-ttu-id="4cd3c-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4cd3c-106">Properties</span></span>
|<span data-ttu-id="4cd3c-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4cd3c-107">Property</span></span>|<span data-ttu-id="4cd3c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4cd3c-108">Type</span></span>|<span data-ttu-id="4cd3c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cd3c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4cd3c-110">displayName</span><span class="sxs-lookup"><span data-stu-id="4cd3c-110">displayName</span></span>|<span data-ttu-id="4cd3c-111">cadena</span><span class="sxs-lookup"><span data-stu-id="4cd3c-111">String</span></span>|<span data-ttu-id="4cd3c-112">Nombre de la página</span><span class="sxs-lookup"><span data-stu-id="4cd3c-112">Name of the page</span></span>|
|<span data-ttu-id="4cd3c-113">iconos</span><span class="sxs-lookup"><span data-stu-id="4cd3c-113">icons</span></span>|<span data-ttu-id="4cd3c-114">Colección [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="4cd3c-114">[iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md) collection</span></span>|<span data-ttu-id="4cd3c-115">Una lista de aplicaciones y carpetas que aparecen en una página.</span><span class="sxs-lookup"><span data-stu-id="4cd3c-115">A list of apps and folders to appear on a page.</span></span> <span data-ttu-id="4cd3c-116">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="4cd3c-116">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4cd3c-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4cd3c-117">Relationships</span></span>
<span data-ttu-id="4cd3c-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4cd3c-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4cd3c-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4cd3c-119">JSON Representation</span></span>
<span data-ttu-id="4cd3c-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4cd3c-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosHomeScreenPage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenPage",
  "displayName": "String",
  "icons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenItem",
      "displayName": "String",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "String",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "String",
              "bundleID": "String"
            }
          ]
        }
      ]
    }
  ]
}
```



