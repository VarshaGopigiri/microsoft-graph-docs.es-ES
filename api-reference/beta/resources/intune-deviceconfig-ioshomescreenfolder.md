---
title: Tipo de recurso iosHomeScreenFolder
description: Una carpeta que contiene páginas de aplicaciones en la pantalla de inicio
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 97d159b09d8484a88db46ec6d25fa9996127b484
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937953"
---
# <a name="ioshomescreenfolder-resource-type"></a><span data-ttu-id="7bd22-103">Tipo de recurso iosHomeScreenFolder</span><span class="sxs-lookup"><span data-stu-id="7bd22-103">iosHomeScreenFolder resource type</span></span>

> <span data-ttu-id="7bd22-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7bd22-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7bd22-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7bd22-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7bd22-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7bd22-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7bd22-107">Una carpeta que contiene páginas de aplicaciones en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="7bd22-107">A folder containing pages of apps on the Home Screen</span></span>

<span data-ttu-id="7bd22-108">Hereda de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="7bd22-108">Inherits from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="7bd22-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7bd22-109">Properties</span></span>
|<span data-ttu-id="7bd22-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7bd22-110">Property</span></span>|<span data-ttu-id="7bd22-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bd22-111">Type</span></span>|<span data-ttu-id="7bd22-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bd22-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7bd22-113">displayName</span><span class="sxs-lookup"><span data-stu-id="7bd22-113">displayName</span></span>|<span data-ttu-id="7bd22-114">cadena</span><span class="sxs-lookup"><span data-stu-id="7bd22-114">String</span></span>|<span data-ttu-id="7bd22-115">Nombre de la aplicación heredado de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="7bd22-115">Name of the app Inherited from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>|
|<span data-ttu-id="7bd22-116">páginas</span><span class="sxs-lookup"><span data-stu-id="7bd22-116">pages</span></span>|<span data-ttu-id="7bd22-117">Colección [iosHomeScreenFolderPage](../resources/intune-deviceconfig-ioshomescreenfolderpage.md)</span><span class="sxs-lookup"><span data-stu-id="7bd22-117">[iosHomeScreenFolderPage](../resources/intune-deviceconfig-ioshomescreenfolderpage.md) collection</span></span>|<span data-ttu-id="7bd22-118">Páginas de iconos de diseño de pantalla de inicio que deben ser Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="7bd22-118">Pages of Home Screen Layout Icons which must be Application Type.</span></span> <span data-ttu-id="7bd22-119">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="7bd22-119">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7bd22-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7bd22-120">Relationships</span></span>
<span data-ttu-id="7bd22-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7bd22-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7bd22-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7bd22-122">JSON Representation</span></span>
<span data-ttu-id="7bd22-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7bd22-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosHomeScreenFolder"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenFolder",
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
```





