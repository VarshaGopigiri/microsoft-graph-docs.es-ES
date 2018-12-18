---
title: Tipo de recurso managedAppOperation
description: Representa una operación que se aplica a un registro de la aplicación.
author: tfitzmac
ms.openlocfilehash: ab12d7e8d7014b1f7c1ea4d6e6dc8e8a81d804d2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356913"
---
# <a name="managedappoperation-resource-type"></a><span data-ttu-id="610dd-103">Tipo de recurso managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="610dd-103">managedAppOperation resource type</span></span>

> <span data-ttu-id="610dd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="610dd-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="610dd-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="610dd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="610dd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="610dd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="610dd-107">Representa una operación que se aplica a un registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="610dd-107">Represents an operation applied against an app registration.</span></span>
## <a name="methods"></a><span data-ttu-id="610dd-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="610dd-108">Methods</span></span>
|<span data-ttu-id="610dd-109">Método</span><span class="sxs-lookup"><span data-stu-id="610dd-109">Method</span></span>|<span data-ttu-id="610dd-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="610dd-110">Return Type</span></span>|<span data-ttu-id="610dd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="610dd-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="610dd-112">Enumerar managedAppOperations</span><span class="sxs-lookup"><span data-stu-id="610dd-112">List managedAppOperations</span></span>](../api/intune-mam-managedappoperation-list.md)|<span data-ttu-id="610dd-113">Colección [managedAppOperation](../resources/intune-mam-managedappoperation.md)</span><span class="sxs-lookup"><span data-stu-id="610dd-113">[managedAppOperation](../resources/intune-mam-managedappoperation.md) collection</span></span>|<span data-ttu-id="610dd-114">Enumere las propiedades y las relaciones de los objetos [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="610dd-114">List properties and relationships of the [managedAppOperation](../resources/intune-mam-managedappoperation.md) objects.</span></span>|
|[<span data-ttu-id="610dd-115">Obtener managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="610dd-115">Get managedAppOperation</span></span>](../api/intune-mam-managedappoperation-get.md)|[<span data-ttu-id="610dd-116">managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="610dd-116">managedAppOperation</span></span>](../resources/intune-mam-managedappoperation.md)|<span data-ttu-id="610dd-117">Lea las propiedades y las relaciones del objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="610dd-117">Read properties and relationships of the [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>|
|[<span data-ttu-id="610dd-118">Crear managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="610dd-118">Create managedAppOperation</span></span>](../api/intune-mam-managedappoperation-create.md)|[<span data-ttu-id="610dd-119">managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="610dd-119">managedAppOperation</span></span>](../resources/intune-mam-managedappoperation.md)|<span data-ttu-id="610dd-120">Cree un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="610dd-120">Create a new [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>|
|[<span data-ttu-id="610dd-121">Eliminar managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="610dd-121">Delete managedAppOperation</span></span>](../api/intune-mam-managedappoperation-delete.md)|<span data-ttu-id="610dd-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="610dd-122">None</span></span>|<span data-ttu-id="610dd-123">Elimina un [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="610dd-123">Deletes a [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span></span>|
|[<span data-ttu-id="610dd-124">Actualizar managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="610dd-124">Update managedAppOperation</span></span>](../api/intune-mam-managedappoperation-update.md)|[<span data-ttu-id="610dd-125">managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="610dd-125">managedAppOperation</span></span>](../resources/intune-mam-managedappoperation.md)|<span data-ttu-id="610dd-126">Actualice las propiedades de un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="610dd-126">Update the properties of a [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="610dd-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="610dd-127">Properties</span></span>
|<span data-ttu-id="610dd-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="610dd-128">Property</span></span>|<span data-ttu-id="610dd-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="610dd-129">Type</span></span>|<span data-ttu-id="610dd-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="610dd-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="610dd-131">displayName</span><span class="sxs-lookup"><span data-stu-id="610dd-131">displayName</span></span>|<span data-ttu-id="610dd-132">String</span><span class="sxs-lookup"><span data-stu-id="610dd-132">String</span></span>|<span data-ttu-id="610dd-133">El nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="610dd-133">The operation name.</span></span>|
|<span data-ttu-id="610dd-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="610dd-134">lastModifiedDateTime</span></span>|<span data-ttu-id="610dd-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="610dd-135">DateTimeOffset</span></span>|<span data-ttu-id="610dd-136">La última vez que se modificó el funcionamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="610dd-136">The last time the app operation was modified.</span></span>|
|<span data-ttu-id="610dd-137">state</span><span class="sxs-lookup"><span data-stu-id="610dd-137">state</span></span>|<span data-ttu-id="610dd-138">String</span><span class="sxs-lookup"><span data-stu-id="610dd-138">String</span></span>|<span data-ttu-id="610dd-139">El estado actual de la operación</span><span class="sxs-lookup"><span data-stu-id="610dd-139">The current state of the operation</span></span>|
|<span data-ttu-id="610dd-140">id</span><span class="sxs-lookup"><span data-stu-id="610dd-140">id</span></span>|<span data-ttu-id="610dd-141">String</span><span class="sxs-lookup"><span data-stu-id="610dd-141">String</span></span>|<span data-ttu-id="610dd-142">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="610dd-142">Key of the entity.</span></span>|
|<span data-ttu-id="610dd-143">version</span><span class="sxs-lookup"><span data-stu-id="610dd-143">version</span></span>|<span data-ttu-id="610dd-144">String</span><span class="sxs-lookup"><span data-stu-id="610dd-144">String</span></span>|<span data-ttu-id="610dd-145">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="610dd-145">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="610dd-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="610dd-146">Relationships</span></span>
<span data-ttu-id="610dd-147">Ninguna</span><span class="sxs-lookup"><span data-stu-id="610dd-147">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="610dd-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="610dd-148">JSON Representation</span></span>
<span data-ttu-id="610dd-149">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="610dd-149">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppOperation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "state": "String",
  "id": "String (identifier)",
  "version": "String"
}
```





