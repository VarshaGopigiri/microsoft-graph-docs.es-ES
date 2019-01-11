---
title: tipo de recurso mobileContainedApp
description: Una clase abstracta que representa una aplicación de contenidos en una mobileApp que actúa como un paquete.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b81ee4ca194d1d01e3d834b3287f6b400e712a27
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826288"
---
# <a name="mobilecontainedapp-resource-type"></a><span data-ttu-id="52b17-103">tipo de recurso mobileContainedApp</span><span class="sxs-lookup"><span data-stu-id="52b17-103">mobileContainedApp resource type</span></span>

> <span data-ttu-id="52b17-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="52b17-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="52b17-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="52b17-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="52b17-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="52b17-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="52b17-107">Una clase abstracta que representa una aplicación de contenidos en una mobileApp que actúa como un paquete.</span><span class="sxs-lookup"><span data-stu-id="52b17-107">An abstract class that represents a contained app in a mobileApp acting as a package.</span></span>
## <a name="methods"></a><span data-ttu-id="52b17-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="52b17-108">Methods</span></span>
|<span data-ttu-id="52b17-109">Método</span><span class="sxs-lookup"><span data-stu-id="52b17-109">Method</span></span>|<span data-ttu-id="52b17-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52b17-110">Return Type</span></span>|<span data-ttu-id="52b17-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="52b17-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="52b17-112">Lista mobileContainedApps</span><span class="sxs-lookup"><span data-stu-id="52b17-112">List mobileContainedApps</span></span>](../api/intune-apps-mobilecontainedapp-list.md)|<span data-ttu-id="52b17-113">colección de [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)</span><span class="sxs-lookup"><span data-stu-id="52b17-113">[mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md) collection</span></span>|<span data-ttu-id="52b17-114">Propiedades de la lista y relaciones de los objetos [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md) .</span><span class="sxs-lookup"><span data-stu-id="52b17-114">List properties and relationships of the [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md) objects.</span></span>|
|[<span data-ttu-id="52b17-115">Obtener mobileContainedApp</span><span class="sxs-lookup"><span data-stu-id="52b17-115">Get mobileContainedApp</span></span>](../api/intune-apps-mobilecontainedapp-get.md)|[<span data-ttu-id="52b17-116">mobileContainedApp</span><span class="sxs-lookup"><span data-stu-id="52b17-116">mobileContainedApp</span></span>](../resources/intune-apps-mobilecontainedapp.md)|<span data-ttu-id="52b17-117">Leer las propiedades y las relaciones del objeto [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md) .</span><span class="sxs-lookup"><span data-stu-id="52b17-117">Read properties and relationships of the [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="52b17-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="52b17-118">Properties</span></span>
|<span data-ttu-id="52b17-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="52b17-119">Property</span></span>|<span data-ttu-id="52b17-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="52b17-120">Type</span></span>|<span data-ttu-id="52b17-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="52b17-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="52b17-122">id</span><span class="sxs-lookup"><span data-stu-id="52b17-122">id</span></span>|<span data-ttu-id="52b17-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="52b17-123">String</span></span>|<span data-ttu-id="52b17-124">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="52b17-124">Key of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="52b17-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="52b17-125">Relationships</span></span>
<span data-ttu-id="52b17-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="52b17-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="52b17-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="52b17-127">JSON Representation</span></span>
<span data-ttu-id="52b17-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="52b17-128">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileContainedApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileContainedApp",
  "id": "String (identifier)"
}
```





