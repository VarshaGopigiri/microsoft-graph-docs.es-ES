---
title: Tipo de recurso managedAppOperation
description: Representa una operación que se aplica a un registro de la aplicación.
ms.openlocfilehash: 267adafc5a74ad447dfb3468cf9238e1c4642e5f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083217"
---
# <a name="managedappoperation-resource-type"></a><span data-ttu-id="86a07-103">Tipo de recurso managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="86a07-103">managedAppOperation resource type</span></span>

> <span data-ttu-id="86a07-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="86a07-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="86a07-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="86a07-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="86a07-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="86a07-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="86a07-107">Representa una operación que se aplica a un registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="86a07-107">Represents an operation applied against an app registration.</span></span>
## <a name="methods"></a><span data-ttu-id="86a07-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="86a07-108">Methods</span></span>
|<span data-ttu-id="86a07-109">Método</span><span class="sxs-lookup"><span data-stu-id="86a07-109">Method</span></span>|<span data-ttu-id="86a07-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86a07-110">Return Type</span></span>|<span data-ttu-id="86a07-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="86a07-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="86a07-112">Enumerar managedAppOperations</span><span class="sxs-lookup"><span data-stu-id="86a07-112">List managedAppOperations</span></span>](../api/intune-mam-managedappoperation-list.md)|<span data-ttu-id="86a07-113">Colección [managedAppOperation](../resources/intune-mam-managedappoperation.md)</span><span class="sxs-lookup"><span data-stu-id="86a07-113">[managedAppOperation](../resources/intune-mam-managedappoperation.md) collection</span></span>|<span data-ttu-id="86a07-114">Enumere las propiedades y las relaciones de los objetos [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="86a07-114">List properties and relationships of the [managedAppOperation](../resources/intune-mam-managedappoperation.md) objects.</span></span>|
|[<span data-ttu-id="86a07-115">Obtener managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="86a07-115">Get managedAppOperation</span></span>](../api/intune-mam-managedappoperation-get.md)|[<span data-ttu-id="86a07-116">managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="86a07-116">managedAppOperation</span></span>](../resources/intune-mam-managedappoperation.md)|<span data-ttu-id="86a07-117">Lea las propiedades y las relaciones del objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="86a07-117">Read properties and relationships of the [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>|
|[<span data-ttu-id="86a07-118">Crear managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="86a07-118">Create managedAppOperation</span></span>](../api/intune-mam-managedappoperation-create.md)|[<span data-ttu-id="86a07-119">managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="86a07-119">managedAppOperation</span></span>](../resources/intune-mam-managedappoperation.md)|<span data-ttu-id="86a07-120">Cree un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="86a07-120">Create a new [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>|
|[<span data-ttu-id="86a07-121">Eliminar managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="86a07-121">Delete managedAppOperation</span></span>](../api/intune-mam-managedappoperation-delete.md)|<span data-ttu-id="86a07-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="86a07-122">None</span></span>|<span data-ttu-id="86a07-123">Elimina un [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="86a07-123">Deletes a [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span></span>|
|[<span data-ttu-id="86a07-124">Actualizar managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="86a07-124">Update managedAppOperation</span></span>](../api/intune-mam-managedappoperation-update.md)|[<span data-ttu-id="86a07-125">managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="86a07-125">managedAppOperation</span></span>](../resources/intune-mam-managedappoperation.md)|<span data-ttu-id="86a07-126">Actualice las propiedades de un objeto [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="86a07-126">Update the properties of a [managedAppOperation](../resources/intune-mam-managedappoperation.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="86a07-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="86a07-127">Properties</span></span>
|<span data-ttu-id="86a07-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="86a07-128">Property</span></span>|<span data-ttu-id="86a07-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="86a07-129">Type</span></span>|<span data-ttu-id="86a07-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="86a07-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="86a07-131">displayName</span><span class="sxs-lookup"><span data-stu-id="86a07-131">displayName</span></span>|<span data-ttu-id="86a07-132">String</span><span class="sxs-lookup"><span data-stu-id="86a07-132">String</span></span>|<span data-ttu-id="86a07-133">El nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="86a07-133">The operation name.</span></span>|
|<span data-ttu-id="86a07-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="86a07-134">lastModifiedDateTime</span></span>|<span data-ttu-id="86a07-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="86a07-135">DateTimeOffset</span></span>|<span data-ttu-id="86a07-136">La última vez que se modificó el funcionamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="86a07-136">The last time the app operation was modified.</span></span>|
|<span data-ttu-id="86a07-137">estado</span><span class="sxs-lookup"><span data-stu-id="86a07-137">state</span></span>|<span data-ttu-id="86a07-138">String</span><span class="sxs-lookup"><span data-stu-id="86a07-138">String</span></span>|<span data-ttu-id="86a07-139">El estado actual de la operación</span><span class="sxs-lookup"><span data-stu-id="86a07-139">The current state of the operation</span></span>|
|<span data-ttu-id="86a07-140">id</span><span class="sxs-lookup"><span data-stu-id="86a07-140">id</span></span>|<span data-ttu-id="86a07-141">String</span><span class="sxs-lookup"><span data-stu-id="86a07-141">String</span></span>|<span data-ttu-id="86a07-142">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="86a07-142">Key of the entity.</span></span>|
|<span data-ttu-id="86a07-143">version</span><span class="sxs-lookup"><span data-stu-id="86a07-143">version</span></span>|<span data-ttu-id="86a07-144">String</span><span class="sxs-lookup"><span data-stu-id="86a07-144">String</span></span>|<span data-ttu-id="86a07-145">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="86a07-145">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="86a07-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="86a07-146">Relationships</span></span>
<span data-ttu-id="86a07-147">Ninguna</span><span class="sxs-lookup"><span data-stu-id="86a07-147">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="86a07-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="86a07-148">JSON Representation</span></span>
<span data-ttu-id="86a07-149">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="86a07-149">Here is a JSON representation of the resource.</span></span>
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





