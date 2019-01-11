---
title: Tipo de recurso iosHomeScreenFolder
description: Una carpeta que contiene páginas de aplicaciones en la pantalla de inicio
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1a4f7f4180bce05d331fcc116826956f4feed70c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844579"
---
# <a name="ioshomescreenfolder-resource-type"></a><span data-ttu-id="afc19-103">Tipo de recurso iosHomeScreenFolder</span><span class="sxs-lookup"><span data-stu-id="afc19-103">iosHomeScreenFolder resource type</span></span>

> <span data-ttu-id="afc19-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="afc19-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="afc19-105">Una carpeta que contiene páginas de aplicaciones en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="afc19-105">A folder containing pages of apps on the Home Screen</span></span>

<span data-ttu-id="afc19-106">Hereda de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="afc19-106">Inherits from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="afc19-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="afc19-107">Properties</span></span>
|<span data-ttu-id="afc19-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="afc19-108">Property</span></span>|<span data-ttu-id="afc19-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="afc19-109">Type</span></span>|<span data-ttu-id="afc19-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="afc19-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="afc19-111">displayName</span><span class="sxs-lookup"><span data-stu-id="afc19-111">displayName</span></span>|<span data-ttu-id="afc19-112">cadena</span><span class="sxs-lookup"><span data-stu-id="afc19-112">String</span></span>|<span data-ttu-id="afc19-113">Nombre de la aplicación heredado de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="afc19-113">Name of the app Inherited from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>|
|<span data-ttu-id="afc19-114">páginas</span><span class="sxs-lookup"><span data-stu-id="afc19-114">pages</span></span>|<span data-ttu-id="afc19-115">Colección [iosHomeScreenFolderPage](../resources/intune-deviceconfig-ioshomescreenfolderpage.md)</span><span class="sxs-lookup"><span data-stu-id="afc19-115">[iosHomeScreenFolderPage](../resources/intune-deviceconfig-ioshomescreenfolderpage.md) collection</span></span>|<span data-ttu-id="afc19-116">Páginas de iconos de diseño de pantalla de inicio que deben ser Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="afc19-116">Pages of Home Screen Layout Icons which must be Application Type.</span></span> <span data-ttu-id="afc19-117">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="afc19-117">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="afc19-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="afc19-118">Relationships</span></span>
<span data-ttu-id="afc19-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="afc19-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="afc19-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="afc19-120">JSON Representation</span></span>
<span data-ttu-id="afc19-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="afc19-121">Here is a JSON representation of the resource.</span></span>
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



