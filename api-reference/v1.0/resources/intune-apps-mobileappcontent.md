---
title: Tipo de recurso mobileAppContent
description: Contiene las propiedades del contenido de una versión de aplicación específica. Cada mobileAppContent puede tener varios mobileAppContentFile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 76895e336b633da63d62a467a267f96b3f344132
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918878"
---
# <a name="mobileappcontent-resource-type"></a><span data-ttu-id="7c610-104">Tipo de recurso mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="7c610-104">mobileAppContent resource type</span></span>

> <span data-ttu-id="7c610-105">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7c610-105">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7c610-106">Contiene las propiedades del contenido de una versión de aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="7c610-106">Contains content properties for a specific app version.</span></span> <span data-ttu-id="7c610-107">Cada mobileAppContent puede tener varios mobileAppContentFile.</span><span class="sxs-lookup"><span data-stu-id="7c610-107">Each mobileAppContent can have multiple mobileAppContentFile.</span></span>
## <a name="methods"></a><span data-ttu-id="7c610-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7c610-108">Methods</span></span>
|<span data-ttu-id="7c610-109">Método</span><span class="sxs-lookup"><span data-stu-id="7c610-109">Method</span></span>|<span data-ttu-id="7c610-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c610-110">Return Type</span></span>|<span data-ttu-id="7c610-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c610-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="7c610-112">Enumerar mobileAppContents</span><span class="sxs-lookup"><span data-stu-id="7c610-112">List mobileAppContents</span></span>](../api/intune-apps-mobileappcontent-list.md)|<span data-ttu-id="7c610-113">Colección [mobileAppContent](../resources/intune-apps-mobileappcontent.md)</span><span class="sxs-lookup"><span data-stu-id="7c610-113">[mobileAppContent](../resources/intune-apps-mobileappcontent.md) collection</span></span>|<span data-ttu-id="7c610-114">Enumere las propiedades y las relaciones de los objetos [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="7c610-114">List properties and relationships of the [mobileAppContent](../resources/intune-apps-mobileappcontent.md) objects.</span></span>|
|[<span data-ttu-id="7c610-115">Obtener mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="7c610-115">Get mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-get.md)|[<span data-ttu-id="7c610-116">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="7c610-116">mobileAppContent</span></span>](../resources/intune-apps-mobileappcontent.md)|<span data-ttu-id="7c610-117">Lea las propiedades y las relaciones del objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="7c610-117">Read properties and relationships of the [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>|
|[<span data-ttu-id="7c610-118">Crear mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="7c610-118">Create mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-create.md)|[<span data-ttu-id="7c610-119">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="7c610-119">mobileAppContent</span></span>](../resources/intune-apps-mobileappcontent.md)|<span data-ttu-id="7c610-120">Cree un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="7c610-120">Create a new [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>|
|[<span data-ttu-id="7c610-121">Eliminar mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="7c610-121">Delete mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-delete.md)|<span data-ttu-id="7c610-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7c610-122">None</span></span>|<span data-ttu-id="7c610-123">Elimina un [mobileAppContent](../resources/intune-apps-mobileappcontent.md)</span><span class="sxs-lookup"><span data-stu-id="7c610-123">Deletes a [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span></span>|
|[<span data-ttu-id="7c610-124">Actualizar mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="7c610-124">Update mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-update.md)|[<span data-ttu-id="7c610-125">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="7c610-125">mobileAppContent</span></span>](../resources/intune-apps-mobileappcontent.md)|<span data-ttu-id="7c610-126">Actualice las propiedades de un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="7c610-126">Update the properties of a [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="7c610-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c610-127">Properties</span></span>
|<span data-ttu-id="7c610-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c610-128">Property</span></span>|<span data-ttu-id="7c610-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c610-129">Type</span></span>|<span data-ttu-id="7c610-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c610-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7c610-131">id</span><span class="sxs-lookup"><span data-stu-id="7c610-131">id</span></span>|<span data-ttu-id="7c610-132">String</span><span class="sxs-lookup"><span data-stu-id="7c610-132">String</span></span>|<span data-ttu-id="7c610-133">La versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7c610-133">The app content version.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7c610-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7c610-134">Relationships</span></span>
|<span data-ttu-id="7c610-135">Relación</span><span class="sxs-lookup"><span data-stu-id="7c610-135">Relationship</span></span>|<span data-ttu-id="7c610-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c610-136">Type</span></span>|<span data-ttu-id="7c610-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c610-137">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7c610-138">archivos</span><span class="sxs-lookup"><span data-stu-id="7c610-138">files</span></span>|<span data-ttu-id="7c610-139">Colección [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md)</span><span class="sxs-lookup"><span data-stu-id="7c610-139">[mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) collection</span></span>|<span data-ttu-id="7c610-140">La lista de archivos de esta versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7c610-140">The list of files for this app content version.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7c610-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7c610-141">JSON Representation</span></span>
<span data-ttu-id="7c610-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7c610-142">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppContent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppContent",
  "id": "String (identifier)"
}
```



