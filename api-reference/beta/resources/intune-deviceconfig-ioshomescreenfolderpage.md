---
title: Tipo de recurso iosHomeScreenFolderPage
description: Una carpeta que contiene aplicaciones en la pantalla de inicio
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 38b1d898cb4bc1eacaa427ed412b536ba40cd0f9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941964"
---
# <a name="ioshomescreenfolderpage-resource-type"></a><span data-ttu-id="fa670-103">Tipo de recurso iosHomeScreenFolderPage</span><span class="sxs-lookup"><span data-stu-id="fa670-103">iosHomeScreenFolderPage resource type</span></span>

> <span data-ttu-id="fa670-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fa670-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fa670-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fa670-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fa670-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fa670-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fa670-107">Una carpeta que contiene aplicaciones en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="fa670-107">A folder containing apps on the Home Screen</span></span>
## <a name="properties"></a><span data-ttu-id="fa670-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fa670-108">Properties</span></span>
|<span data-ttu-id="fa670-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa670-109">Property</span></span>|<span data-ttu-id="fa670-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa670-110">Type</span></span>|<span data-ttu-id="fa670-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa670-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fa670-112">displayName</span><span class="sxs-lookup"><span data-stu-id="fa670-112">displayName</span></span>|<span data-ttu-id="fa670-113">cadena</span><span class="sxs-lookup"><span data-stu-id="fa670-113">String</span></span>|<span data-ttu-id="fa670-114">Nombre de la página de la carpeta</span><span class="sxs-lookup"><span data-stu-id="fa670-114">Name of the folder page</span></span>|
|<span data-ttu-id="fa670-115">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fa670-115">apps</span></span>|<span data-ttu-id="fa670-116">Colección [iosHomeScreenApp](../resources/intune-deviceconfig-ioshomescreenapp.md)</span><span class="sxs-lookup"><span data-stu-id="fa670-116">[iosHomeScreenApp](../resources/intune-deviceconfig-ioshomescreenapp.md) collection</span></span>|<span data-ttu-id="fa670-117">Una lista de aplicaciones que aparecen en una página dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="fa670-117">A list of apps to appear on a page within a folder.</span></span> <span data-ttu-id="fa670-118">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="fa670-118">This collection can contain a maximum of 500 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fa670-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fa670-119">Relationships</span></span>
<span data-ttu-id="fa670-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fa670-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fa670-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fa670-121">JSON Representation</span></span>
<span data-ttu-id="fa670-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fa670-122">Here is a JSON representation of the resource.</span></span>
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





