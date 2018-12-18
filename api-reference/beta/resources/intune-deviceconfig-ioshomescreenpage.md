---
title: Tipo de recurso iosHomeScreenPage
description: Una página que contiene aplicaciones y carpetas en la pantalla de inicio
author: tfitzmac
ms.openlocfilehash: cd7a2ee863c02aa6484889aa20003a94e525514d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27325561"
---
# <a name="ioshomescreenpage-resource-type"></a><span data-ttu-id="6b637-103">Tipo de recurso iosHomeScreenPage</span><span class="sxs-lookup"><span data-stu-id="6b637-103">iosHomeScreenPage resource type</span></span>

> <span data-ttu-id="6b637-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6b637-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6b637-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6b637-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6b637-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6b637-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6b637-107">Una página que contiene aplicaciones y carpetas en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="6b637-107">A page containing apps and folders on the Home Screen</span></span>
## <a name="properties"></a><span data-ttu-id="6b637-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b637-108">Properties</span></span>
|<span data-ttu-id="6b637-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6b637-109">Property</span></span>|<span data-ttu-id="6b637-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="6b637-110">Type</span></span>|<span data-ttu-id="6b637-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b637-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6b637-112">displayName</span><span class="sxs-lookup"><span data-stu-id="6b637-112">displayName</span></span>|<span data-ttu-id="6b637-113">cadena</span><span class="sxs-lookup"><span data-stu-id="6b637-113">String</span></span>|<span data-ttu-id="6b637-114">Nombre de la página</span><span class="sxs-lookup"><span data-stu-id="6b637-114">Name of the page</span></span>|
|<span data-ttu-id="6b637-115">iconos</span><span class="sxs-lookup"><span data-stu-id="6b637-115">icons</span></span>|<span data-ttu-id="6b637-116">Colección [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="6b637-116">[iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md) collection</span></span>|<span data-ttu-id="6b637-117">Una lista de aplicaciones y carpetas que aparecen en una página.</span><span class="sxs-lookup"><span data-stu-id="6b637-117">A list of apps and folders to appear on a page.</span></span> <span data-ttu-id="6b637-118">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="6b637-118">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6b637-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6b637-119">Relationships</span></span>
<span data-ttu-id="6b637-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6b637-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6b637-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6b637-121">JSON Representation</span></span>
<span data-ttu-id="6b637-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6b637-122">Here is a JSON representation of the resource.</span></span>
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
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
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





