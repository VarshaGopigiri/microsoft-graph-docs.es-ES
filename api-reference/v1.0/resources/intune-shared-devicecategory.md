---
title: Tipo de recurso deviceCategory
description: A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos. Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 80f8f1f36198ecfab1021e30cb2f28fa4377852c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810839"
---
# <a name="devicecategory-resource-type"></a><span data-ttu-id="a3e98-104">Tipo de recurso deviceCategory</span><span class="sxs-lookup"><span data-stu-id="a3e98-104">deviceCategory resource type</span></span>

> <span data-ttu-id="a3e98-105">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a3e98-105">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a3e98-106">Las categorías de dispositivo proporcionan una forma de organizar sus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a3e98-106">Device categories provides a way to organize your devices.</span></span> <span data-ttu-id="a3e98-107">Al usar categorías de dispositivos, los administradores de la compañía pueden definir las categorías de forma pertinente para su empresa.</span><span class="sxs-lookup"><span data-stu-id="a3e98-107">Using device categories, company administrators can define their own categories that make sense to their company.</span></span><span data-ttu-id="a3e98-108">A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a3e98-108"> These categories can then be applied to a device in the Intune Azure console or selected by a user during device enrollment.</span></span> <span data-ttu-id="a3e98-109">Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a3e98-109">You can filter reports and create dynamic Azure Active Directory device groups based on device categories.</span></span>

## <a name="methods"></a><span data-ttu-id="a3e98-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a3e98-110">Methods</span></span>
|<span data-ttu-id="a3e98-111">Método</span><span class="sxs-lookup"><span data-stu-id="a3e98-111">Method</span></span>|<span data-ttu-id="a3e98-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3e98-112">Return Type</span></span>|<span data-ttu-id="a3e98-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3e98-113">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a3e98-114">Colección de [lista deviceCategories](../api/intune-shared-devicecategory-list.md)</span><span class="sxs-lookup"><span data-stu-id="a3e98-114">[List deviceCategories](../api/intune-shared-devicecategory-list.md) collection</span></span>|<span data-ttu-id="a3e98-115">Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="a3e98-115">List properties and relationships of the [deviceCategory](../resources/intune-shared-devicecategory.md) objects.</span></span>|
|[<span data-ttu-id="a3e98-116">Obtener deviceCategory</span><span class="sxs-lookup"><span data-stu-id="a3e98-116">Get deviceCategory</span></span>](../api/intune-shared-devicecategory-get.md)|<span data-ttu-id="a3e98-117">Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="a3e98-117">Read properties and relationships of the [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>|
|[<span data-ttu-id="a3e98-118">Crear deviceCategory</span><span class="sxs-lookup"><span data-stu-id="a3e98-118">Create deviceCategory</span></span>](../api/intune-shared-devicecategory-create.md)|<span data-ttu-id="a3e98-119">Cree un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="a3e98-119">Create a new [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>|
|<span data-ttu-id="a3e98-120">[Eliminar deviceCategory](../api/intune-shared-devicecategory-delete.md).</span><span class="sxs-lookup"><span data-stu-id="a3e98-120">[Delete deviceCategory](../api/intune-shared-devicecategory-delete.md).</span></span>|
|[<span data-ttu-id="a3e98-121">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="a3e98-121">Update deviceCategory</span></span>](../api/intune-shared-devicecategory-update.md)|<span data-ttu-id="a3e98-122">Actualice las propiedades de un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="a3e98-122">Update the properties of a [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="a3e98-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3e98-123">Properties</span></span>
|<span data-ttu-id="a3e98-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a3e98-124">Property</span></span>|<span data-ttu-id="a3e98-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3e98-125">Type</span></span>|<span data-ttu-id="a3e98-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3e98-126">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a3e98-127">id</span><span class="sxs-lookup"><span data-stu-id="a3e98-127">id</span></span>|<span data-ttu-id="a3e98-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="a3e98-128">String</span></span>|<span data-ttu-id="a3e98-129">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3e98-129">Unique identifier for the device category.</span></span> <span data-ttu-id="a3e98-130">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a3e98-130">Read-only.</span></span>|
|<span data-ttu-id="a3e98-131">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="a3e98-131">**Onboarding**</span></span>|
|<span data-ttu-id="a3e98-132">displayName</span><span class="sxs-lookup"><span data-stu-id="a3e98-132">displayName</span></span>|<span data-ttu-id="a3e98-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="a3e98-133">String</span></span>|<span data-ttu-id="a3e98-134">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3e98-134">Display name for the device category.</span></span>|
|<span data-ttu-id="a3e98-135">descripción</span><span class="sxs-lookup"><span data-stu-id="a3e98-135">description</span></span>|<span data-ttu-id="a3e98-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="a3e98-136">String</span></span>|<span data-ttu-id="a3e98-137">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3e98-137">Optional description for the device category.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a3e98-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a3e98-138">Relationships</span></span>
<span data-ttu-id="a3e98-139">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a3e98-139">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="a3e98-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a3e98-140">JSON Representation</span></span>
<span data-ttu-id="a3e98-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a3e98-141">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceCategory"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```



