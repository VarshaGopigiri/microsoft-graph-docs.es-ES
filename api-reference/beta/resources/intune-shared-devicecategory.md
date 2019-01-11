---
title: Tipo de recurso deviceCategory
description: A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos. Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b61927b5d4c6e8c85ba454d241a0d61a20185579
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888826"
---
# <a name="devicecategory-resource-type"></a><span data-ttu-id="f88b0-104">Tipo de recurso deviceCategory</span><span class="sxs-lookup"><span data-stu-id="f88b0-104">deviceCategory resource type</span></span>

> <span data-ttu-id="f88b0-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f88b0-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f88b0-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f88b0-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f88b0-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f88b0-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f88b0-108">Categorías de dispositivos proporcionan una forma de organizar los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f88b0-108">Device categories provide a way to organize your devices.</span></span> <span data-ttu-id="f88b0-109">Uso de categorías de dispositivos, administradores de la compañía pueden definir categorías exclusivas que tiene sentido para su empresa.</span><span class="sxs-lookup"><span data-stu-id="f88b0-109">Using device categories, company administrators can define unique categories that make sense to their company.</span></span><span data-ttu-id="f88b0-110">A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f88b0-110"> These categories can then be applied to a device in the Intune Azure console or selected by a user during device enrollment.</span></span> <span data-ttu-id="f88b0-111">Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f88b0-111">You can filter reports and create dynamic Azure Active Directory device groups based on device categories.</span></span>

## <a name="methods"></a><span data-ttu-id="f88b0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f88b0-112">Methods</span></span>
|<span data-ttu-id="f88b0-113">Método</span><span class="sxs-lookup"><span data-stu-id="f88b0-113">Method</span></span>|<span data-ttu-id="f88b0-114">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f88b0-114">Return Type</span></span>|<span data-ttu-id="f88b0-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f88b0-115">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="f88b0-116">Enumerar deviceCategories</span><span class="sxs-lookup"><span data-stu-id="f88b0-116">List deviceCategories</span></span>](../api/intune-shared-devicecategory-list.md)|<span data-ttu-id="f88b0-117">Colección [deviceCategory](../resources/intune-shared-devicecategory.md)</span><span class="sxs-lookup"><span data-stu-id="f88b0-117">[deviceCategory](../resources/intune-shared-devicecategory.md) collection</span></span>|<span data-ttu-id="f88b0-118">Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="f88b0-118">List properties and relationships of the [deviceCategory](../resources/intune-shared-devicecategory.md) objects.</span></span>|
|[<span data-ttu-id="f88b0-119">Obtener deviceCategory</span><span class="sxs-lookup"><span data-stu-id="f88b0-119">Get deviceCategory</span></span>](../api/intune-shared-devicecategory-get.md)|[<span data-ttu-id="f88b0-120">deviceCategory</span><span class="sxs-lookup"><span data-stu-id="f88b0-120">deviceCategory</span></span>](../resources/intune-shared-devicecategory.md)|<span data-ttu-id="f88b0-121">Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="f88b0-121">Read properties and relationships of the [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>|
|[<span data-ttu-id="f88b0-122">Crear deviceCategory</span><span class="sxs-lookup"><span data-stu-id="f88b0-122">Create deviceCategory</span></span>](../api/intune-shared-devicecategory-create.md)|[<span data-ttu-id="f88b0-123">deviceCategory</span><span class="sxs-lookup"><span data-stu-id="f88b0-123">deviceCategory</span></span>](../resources/intune-shared-devicecategory.md)|<span data-ttu-id="f88b0-124">Cree un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="f88b0-124">Create a new [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>|
|[<span data-ttu-id="f88b0-125">Eliminar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="f88b0-125">Delete deviceCategory</span></span>](../api/intune-shared-devicecategory-delete.md)|<span data-ttu-id="f88b0-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f88b0-126">None</span></span>|<span data-ttu-id="f88b0-127">Elimina un [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="f88b0-127">Deletes a [deviceCategory](../resources/intune-shared-devicecategory.md).</span></span>|
|[<span data-ttu-id="f88b0-128">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="f88b0-128">Update deviceCategory</span></span>](../api/intune-shared-devicecategory-update.md)|[<span data-ttu-id="f88b0-129">deviceCategory</span><span class="sxs-lookup"><span data-stu-id="f88b0-129">deviceCategory</span></span>](../resources/intune-shared-devicecategory.md)|<span data-ttu-id="f88b0-130">Actualice las propiedades de un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="f88b0-130">Update the properties of a [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="f88b0-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f88b0-131">Properties</span></span>
|<span data-ttu-id="f88b0-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f88b0-132">Property</span></span>|<span data-ttu-id="f88b0-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="f88b0-133">Type</span></span>|<span data-ttu-id="f88b0-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="f88b0-134">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f88b0-135">id</span><span class="sxs-lookup"><span data-stu-id="f88b0-135">id</span></span>|<span data-ttu-id="f88b0-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="f88b0-136">String</span></span>|<span data-ttu-id="f88b0-137">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f88b0-137">Unique identifier for the device category.</span></span> <span data-ttu-id="f88b0-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f88b0-138">Read-only.</span></span>|
|<span data-ttu-id="f88b0-139">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="f88b0-139">**Onboarding**</span></span>|
|<span data-ttu-id="f88b0-140">displayName</span><span class="sxs-lookup"><span data-stu-id="f88b0-140">displayName</span></span>|<span data-ttu-id="f88b0-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="f88b0-141">String</span></span>|<span data-ttu-id="f88b0-142">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f88b0-142">Display name for the device category.</span></span>|
|<span data-ttu-id="f88b0-143">descripción</span><span class="sxs-lookup"><span data-stu-id="f88b0-143">description</span></span>|<span data-ttu-id="f88b0-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="f88b0-144">String</span></span>|<span data-ttu-id="f88b0-145">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f88b0-145">Optional description for the device category.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f88b0-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f88b0-146">Relationships</span></span>
<span data-ttu-id="f88b0-147">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f88b0-147">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="f88b0-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f88b0-148">JSON Representation</span></span>
<span data-ttu-id="f88b0-149">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f88b0-149">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```



