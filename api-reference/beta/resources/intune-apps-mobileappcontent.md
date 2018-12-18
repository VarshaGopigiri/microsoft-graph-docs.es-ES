---
title: Tipo de recurso mobileAppContent
description: Contiene las propiedades del contenido de una versión de aplicación específica. Cada mobileAppContent puede tener varios mobileAppContentFile.
author: tfitzmac
ms.openlocfilehash: 8cc5bd6e3c7aa5f08236d2662821a9a5d03707d0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360350"
---
# <a name="mobileappcontent-resource-type"></a><span data-ttu-id="26906-104">Tipo de recurso mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="26906-104">mobileAppContent resource type</span></span>

> <span data-ttu-id="26906-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="26906-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="26906-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="26906-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="26906-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="26906-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="26906-108">Contiene las propiedades del contenido de una versión de aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="26906-108">Contains content properties for a specific app version.</span></span> <span data-ttu-id="26906-109">Cada mobileAppContent puede tener varios mobileAppContentFile.</span><span class="sxs-lookup"><span data-stu-id="26906-109">Each mobileAppContent can have multiple mobileAppContentFile.</span></span>
## <a name="methods"></a><span data-ttu-id="26906-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="26906-110">Methods</span></span>
|<span data-ttu-id="26906-111">Método</span><span class="sxs-lookup"><span data-stu-id="26906-111">Method</span></span>|<span data-ttu-id="26906-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26906-112">Return Type</span></span>|<span data-ttu-id="26906-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="26906-113">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="26906-114">Enumerar mobileAppContents</span><span class="sxs-lookup"><span data-stu-id="26906-114">List mobileAppContents</span></span>](../api/intune-apps-mobileappcontent-list.md)|<span data-ttu-id="26906-115">Colección [mobileAppContent](../resources/intune-apps-mobileappcontent.md)</span><span class="sxs-lookup"><span data-stu-id="26906-115">[mobileAppContent](../resources/intune-apps-mobileappcontent.md) collection</span></span>|<span data-ttu-id="26906-116">Enumere las propiedades y las relaciones de los objetos [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="26906-116">List properties and relationships of the [mobileAppContent](../resources/intune-apps-mobileappcontent.md) objects.</span></span>|
|[<span data-ttu-id="26906-117">Obtener mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="26906-117">Get mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-get.md)|[<span data-ttu-id="26906-118">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="26906-118">mobileAppContent</span></span>](../resources/intune-apps-mobileappcontent.md)|<span data-ttu-id="26906-119">Lea las propiedades y las relaciones del objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="26906-119">Read properties and relationships of the [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>|
|[<span data-ttu-id="26906-120">Crear mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="26906-120">Create mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-create.md)|[<span data-ttu-id="26906-121">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="26906-121">mobileAppContent</span></span>](../resources/intune-apps-mobileappcontent.md)|<span data-ttu-id="26906-122">Cree un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="26906-122">Create a new [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>|
|[<span data-ttu-id="26906-123">Eliminar mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="26906-123">Delete mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-delete.md)|<span data-ttu-id="26906-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="26906-124">None</span></span>|<span data-ttu-id="26906-125">Elimina un [mobileAppContent](../resources/intune-apps-mobileappcontent.md)</span><span class="sxs-lookup"><span data-stu-id="26906-125">Deletes a [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span></span>|
|[<span data-ttu-id="26906-126">Actualizar mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="26906-126">Update mobileAppContent</span></span>](../api/intune-apps-mobileappcontent-update.md)|[<span data-ttu-id="26906-127">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="26906-127">mobileAppContent</span></span>](../resources/intune-apps-mobileappcontent.md)|<span data-ttu-id="26906-128">Actualice las propiedades de un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="26906-128">Update the properties of a [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="26906-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26906-129">Properties</span></span>
|<span data-ttu-id="26906-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26906-130">Property</span></span>|<span data-ttu-id="26906-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="26906-131">Type</span></span>|<span data-ttu-id="26906-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="26906-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="26906-133">id</span><span class="sxs-lookup"><span data-stu-id="26906-133">id</span></span>|<span data-ttu-id="26906-134">String</span><span class="sxs-lookup"><span data-stu-id="26906-134">String</span></span>|<span data-ttu-id="26906-135">La versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="26906-135">The app content version.</span></span>|

## <a name="relationships"></a><span data-ttu-id="26906-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="26906-136">Relationships</span></span>
|<span data-ttu-id="26906-137">Relación</span><span class="sxs-lookup"><span data-stu-id="26906-137">Relationship</span></span>|<span data-ttu-id="26906-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="26906-138">Type</span></span>|<span data-ttu-id="26906-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="26906-139">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="26906-140">archivos</span><span class="sxs-lookup"><span data-stu-id="26906-140">files</span></span>|<span data-ttu-id="26906-141">Colección [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md)</span><span class="sxs-lookup"><span data-stu-id="26906-141">[mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) collection</span></span>|<span data-ttu-id="26906-142">La lista de archivos de esta versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="26906-142">The list of files for this app content version.</span></span>|
|<span data-ttu-id="26906-143">containedApps</span><span class="sxs-lookup"><span data-stu-id="26906-143">containedApps</span></span>|<span data-ttu-id="26906-144">colección de [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)</span><span class="sxs-lookup"><span data-stu-id="26906-144">[mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md) collection</span></span>|<span data-ttu-id="26906-145">La colección de aplicaciones de contenido en una MobileLobApp que actúa como un paquete.</span><span class="sxs-lookup"><span data-stu-id="26906-145">The collection of contained apps in a MobileLobApp acting as a package.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="26906-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="26906-146">JSON Representation</span></span>
<span data-ttu-id="26906-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="26906-147">Here is a JSON representation of the resource.</span></span>
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





