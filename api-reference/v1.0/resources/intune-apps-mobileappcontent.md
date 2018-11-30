---
title: Tipo de recurso mobileAppContent
description: Contiene las propiedades del contenido de una versión de aplicación específica. Cada mobileAppContent puede tener varios mobileAppContentFile.
ms.openlocfilehash: 75d00e0b59fe3ca0848c5ad1bcdade76a9430ec1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031484"
---
# <a name="mobileappcontent-resource-type"></a><span data-ttu-id="92a74-104">Tipo de recurso mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="92a74-104">mobileAppContent resource type</span></span>

> <span data-ttu-id="92a74-105">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="92a74-105">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="92a74-106">Contiene las propiedades del contenido de una versión de aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="92a74-106">Contains content properties for a specific app version.</span></span> <span data-ttu-id="92a74-107">Cada mobileAppContent puede tener varios mobileAppContentFile.</span><span class="sxs-lookup"><span data-stu-id="92a74-107">Each mobileAppContent can have multiple mobileAppContentFile.</span></span>
## <a name="methods"></a><span data-ttu-id="92a74-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="92a74-108">Methods</span></span>
|<span data-ttu-id="92a74-109">Método</span><span class="sxs-lookup"><span data-stu-id="92a74-109">Method</span></span>|<span data-ttu-id="92a74-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92a74-110">Return Type</span></span>|<span data-ttu-id="92a74-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="92a74-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="92a74-112">Enumerar mobileAppContents</span><span class="sxs-lookup"><span data-stu-id="92a74-112">List mobileAppContents</span></span>](../api/intune-apps-mobileappcontent-list.md)|<span data-ttu-id="92a74-113">Colección [mobileAppContent](../resources/intune-apps-mobileappcontent.md)</span><span class="sxs-lookup"><span data-stu-id="92a74-113">[mobileAppContent](../resources/intune-apps-mobileappcontent.md) collection</span></span>|<span data-ttu-id="92a74-114">Enumere las propiedades y las relaciones de los objetos [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="92a74-114">List properties and relationships of the [mobileAppContent](../resources/intune-apps-mobileappcontent.md) objects.</span></span>|
|[<span data-ttu-id="92a74-115">Obtener mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="92a74-115">Get mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-get.md)|[<span data-ttu-id="92a74-116">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="92a74-116">mobileAppContent</span></span>](../resources/intune-apps-mobileappcontent.md)|<span data-ttu-id="92a74-117">Lea las propiedades y las relaciones del objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="92a74-117">Read properties and relationships of the [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>|
|[<span data-ttu-id="92a74-118">Crear mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="92a74-118">Create mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-create.md)|[<span data-ttu-id="92a74-119">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="92a74-119">mobileAppContent</span></span>](../resources/intune-apps-mobileappcontent.md)|<span data-ttu-id="92a74-120">Cree un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="92a74-120">Create a new [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>|
|[<span data-ttu-id="92a74-121">Eliminar mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="92a74-121">Delete mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-delete.md)|<span data-ttu-id="92a74-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="92a74-122">None</span></span>|<span data-ttu-id="92a74-123">Elimina un [mobileAppContent](../resources/intune-apps-mobileappcontent.md)</span><span class="sxs-lookup"><span data-stu-id="92a74-123">Deletes a [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span></span>|
|[<span data-ttu-id="92a74-124">Actualizar mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="92a74-124">Update mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-update.md)|[<span data-ttu-id="92a74-125">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="92a74-125">mobileAppContent</span></span>](../resources/intune-apps-mobileappcontent.md)|<span data-ttu-id="92a74-126">Actualice las propiedades de un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="92a74-126">Update the properties of a [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="92a74-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92a74-127">Properties</span></span>
|<span data-ttu-id="92a74-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="92a74-128">Property</span></span>|<span data-ttu-id="92a74-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="92a74-129">Type</span></span>|<span data-ttu-id="92a74-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="92a74-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="92a74-131">id</span><span class="sxs-lookup"><span data-stu-id="92a74-131">id</span></span>|<span data-ttu-id="92a74-132">String</span><span class="sxs-lookup"><span data-stu-id="92a74-132">String</span></span>|<span data-ttu-id="92a74-133">La versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="92a74-133">The app content version.</span></span>|

## <a name="relationships"></a><span data-ttu-id="92a74-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="92a74-134">Relationships</span></span>
|<span data-ttu-id="92a74-135">Relación</span><span class="sxs-lookup"><span data-stu-id="92a74-135">Relationship</span></span>|<span data-ttu-id="92a74-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="92a74-136">Type</span></span>|<span data-ttu-id="92a74-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="92a74-137">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="92a74-138">archivos</span><span class="sxs-lookup"><span data-stu-id="92a74-138">files</span></span>|<span data-ttu-id="92a74-139">Colección [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md)</span><span class="sxs-lookup"><span data-stu-id="92a74-139">[mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) collection</span></span>|<span data-ttu-id="92a74-140">La lista de archivos de esta versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="92a74-140">The list of files for this app content version.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="92a74-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="92a74-141">JSON Representation</span></span>
<span data-ttu-id="92a74-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="92a74-142">Here is a JSON representation of the resource.</span></span>
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



