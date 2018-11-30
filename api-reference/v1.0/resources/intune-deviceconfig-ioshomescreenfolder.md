---
title: Tipo de recurso iosHomeScreenFolder
description: Una carpeta que contiene páginas de aplicaciones en la pantalla de inicio
ms.openlocfilehash: 1b3d4c75ec177eb4c277c7f5bc7f76ccf550d30b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029084"
---
# <a name="ioshomescreenfolder-resource-type"></a><span data-ttu-id="8d766-103">Tipo de recurso iosHomeScreenFolder</span><span class="sxs-lookup"><span data-stu-id="8d766-103">iosHomeScreenFolder resource type</span></span>

> <span data-ttu-id="8d766-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d766-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d766-105">Una carpeta que contiene páginas de aplicaciones en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="8d766-105">A folder containing pages of apps on the Home Screen</span></span>

<span data-ttu-id="8d766-106">Hereda de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="8d766-106">Inherits from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8d766-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d766-107">Properties</span></span>
|<span data-ttu-id="8d766-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d766-108">Property</span></span>|<span data-ttu-id="8d766-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d766-109">Type</span></span>|<span data-ttu-id="8d766-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d766-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d766-111">displayName</span><span class="sxs-lookup"><span data-stu-id="8d766-111">displayName</span></span>|<span data-ttu-id="8d766-112">cadena</span><span class="sxs-lookup"><span data-stu-id="8d766-112">String</span></span>|<span data-ttu-id="8d766-113">Nombre de la aplicación heredado de [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="8d766-113">Name of the app Inherited from [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span></span>|
|<span data-ttu-id="8d766-114">páginas</span><span class="sxs-lookup"><span data-stu-id="8d766-114">pages</span></span>|<span data-ttu-id="8d766-115">Colección [iosHomeScreenFolderPage](../resources/intune-deviceconfig-ioshomescreenfolderpage.md)</span><span class="sxs-lookup"><span data-stu-id="8d766-115">[iosHomeScreenFolderPage](../resources/intune-deviceconfig-ioshomescreenfolderpage.md) collection</span></span>|<span data-ttu-id="8d766-116">Páginas de iconos de diseño de pantalla de inicio que deben ser Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="8d766-116">Pages of Home Screen Layout Icons which must be Application Type.</span></span> <span data-ttu-id="8d766-117">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8d766-117">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8d766-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8d766-118">Relationships</span></span>
<span data-ttu-id="8d766-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8d766-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8d766-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d766-120">JSON Representation</span></span>
<span data-ttu-id="8d766-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d766-121">Here is a JSON representation of the resource.</span></span>
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



