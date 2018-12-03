---
title: tipo de recurso directoryAudit
description: Este recurso representa los elementos de auditoría de Active directory y su colección
ms.openlocfilehash: 8656bd910cd5b84d7760f973b160d91efe08abe1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082932"
---
# <a name="directoryaudit-resource-type"></a><span data-ttu-id="7275c-103">tipo de recurso directoryAudit</span><span class="sxs-lookup"><span data-stu-id="7275c-103">directoryAudit resource type</span></span>
<span data-ttu-id="7275c-104">Este recurso representa los elementos de auditoría de Active directory y su colección</span><span class="sxs-lookup"><span data-stu-id="7275c-104">This resource represents the directory Audit items and its collection</span></span>


## <a name="methods"></a><span data-ttu-id="7275c-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="7275c-105">Methods</span></span>

| <span data-ttu-id="7275c-106">Método</span><span class="sxs-lookup"><span data-stu-id="7275c-106">Method</span></span>           | <span data-ttu-id="7275c-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7275c-107">Return Type</span></span>    |<span data-ttu-id="7275c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7275c-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="7275c-109">Lista directoryAudits</span><span class="sxs-lookup"><span data-stu-id="7275c-109">List directoryAudits</span></span>](../api/directoryaudit-list.md) | [<span data-ttu-id="7275c-110">directoryAudit</span><span class="sxs-lookup"><span data-stu-id="7275c-110">directoryAudit</span></span>](directoryaudit.md) |<span data-ttu-id="7275c-111">Lista de los elementos de auditoría de Active directory en la colección y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="7275c-111">List the directory audit items in the collection and their properties.</span></span>|
|[<span data-ttu-id="7275c-112">Obtener directoryAudit</span><span class="sxs-lookup"><span data-stu-id="7275c-112">Get directoryAudit</span></span>](../api/directoryaudit-get.md) | [<span data-ttu-id="7275c-113">directoryAudit</span><span class="sxs-lookup"><span data-stu-id="7275c-113">directoryAudit</span></span>](directoryaudit.md) |<span data-ttu-id="7275c-114">Obtener un elemento de auditoría de directorio específica y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="7275c-114">Get a specific directory audit item and its properties.</span></span>|


## <a name="properties"></a><span data-ttu-id="7275c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7275c-115">Properties</span></span>
| <span data-ttu-id="7275c-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7275c-116">Property</span></span>     | <span data-ttu-id="7275c-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="7275c-117">Type</span></span>   |<span data-ttu-id="7275c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="7275c-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7275c-119">activityDateTime</span><span class="sxs-lookup"><span data-stu-id="7275c-119">activityDateTime</span></span>|<span data-ttu-id="7275c-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7275c-120">DateTimeOffset</span></span>|<span data-ttu-id="7275c-121">Indica la fecha y hora que se llevó a cabo la actividad.</span><span class="sxs-lookup"><span data-stu-id="7275c-121">Indicates the date and time the activity was performed.</span></span> <span data-ttu-id="7275c-122">El tipo de marca de tiempo es siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="7275c-122">The Timestamp type is always in UTC time.</span></span> <span data-ttu-id="7275c-123">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="7275c-123">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="7275c-124">activityDisplayName</span><span class="sxs-lookup"><span data-stu-id="7275c-124">activityDisplayName</span></span>|<span data-ttu-id="7275c-125">String</span><span class="sxs-lookup"><span data-stu-id="7275c-125">String</span></span>|<span data-ttu-id="7275c-126">Indica el nombre de la actividad o el nombre de la operación (por ejemplo</span><span class="sxs-lookup"><span data-stu-id="7275c-126">Indicates the activity name or the operation name (E.g.</span></span> <span data-ttu-id="7275c-127">"Crear usuario", "Agregar miembros al grupo").</span><span class="sxs-lookup"><span data-stu-id="7275c-127">"Create User", "Add member to group").</span></span> <span data-ttu-id="7275c-128">Para obtener una lista de actividades que se registran, hacer referencia a la [lista de actividades de Azure Ad](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-audit-logs#azure-ad-audit-activity-list).</span><span class="sxs-lookup"><span data-stu-id="7275c-128">For a list of activities logged,refer to [Azure Ad activity list](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-activity-audit-logs#azure-ad-audit-activity-list).</span></span>|
|<span data-ttu-id="7275c-129">additionalDetails</span><span class="sxs-lookup"><span data-stu-id="7275c-129">additionalDetails</span></span>|<span data-ttu-id="7275c-130">colección [keyValue](keyvalue.md)</span><span class="sxs-lookup"><span data-stu-id="7275c-130">[keyValue](keyvalue.md) collection</span></span>|<span data-ttu-id="7275c-131">Indica información adicional sobre la actividad.</span><span class="sxs-lookup"><span data-stu-id="7275c-131">Indicates additional details on the activity.</span></span>|
|<span data-ttu-id="7275c-132">.</span><span class="sxs-lookup"><span data-stu-id="7275c-132">category</span></span>|<span data-ttu-id="7275c-133">String</span><span class="sxs-lookup"><span data-stu-id="7275c-133">String</span></span>|<span data-ttu-id="7275c-134">Indica qué categoría de recurso que está dirigido por la actividad.</span><span class="sxs-lookup"><span data-stu-id="7275c-134">Indicates which resource category that's targeted by the activity.</span></span> <span data-ttu-id="7275c-135">(Por ejemplo: administración de usuario, grupo de administración etcetera..)</span><span class="sxs-lookup"><span data-stu-id="7275c-135">(For example: User Management, Group Management etc..)</span></span>|
|<span data-ttu-id="7275c-136">correlationId</span><span class="sxs-lookup"><span data-stu-id="7275c-136">correlationId</span></span>|<span data-ttu-id="7275c-137">GUID</span><span class="sxs-lookup"><span data-stu-id="7275c-137">GUID</span></span>|<span data-ttu-id="7275c-138">Indica un identificador único que ayuda a relacionar actividades que abarcan varios servicios.</span><span class="sxs-lookup"><span data-stu-id="7275c-138">Indicates a unique ID that helps correlate activities that span across various services.</span></span> <span data-ttu-id="7275c-139">Se puede usar para los registros de seguimiento a través de servicios.</span><span class="sxs-lookup"><span data-stu-id="7275c-139">Can be used to trace logs across services.</span></span>|
|<span data-ttu-id="7275c-140">id</span><span class="sxs-lookup"><span data-stu-id="7275c-140">id</span></span>|<span data-ttu-id="7275c-141">String</span><span class="sxs-lookup"><span data-stu-id="7275c-141">String</span></span>| <span data-ttu-id="7275c-142">Indica el identificador único para la actividad.</span><span class="sxs-lookup"><span data-stu-id="7275c-142">Indicates the unique ID for the activity.</span></span> <span data-ttu-id="7275c-143">Esto es un GUID.</span><span class="sxs-lookup"><span data-stu-id="7275c-143">This is a GUID.</span></span>|
|<span data-ttu-id="7275c-144">initiatedBy</span><span class="sxs-lookup"><span data-stu-id="7275c-144">initiatedBy</span></span>|[<span data-ttu-id="7275c-145">auditActivityInitiator</span><span class="sxs-lookup"><span data-stu-id="7275c-145">auditActivityInitiator</span></span>](auditactivityinitiator.md)|<span data-ttu-id="7275c-146">Indica información sobre el usuario o aplicación iniciadas por la actividad.</span><span class="sxs-lookup"><span data-stu-id="7275c-146">Indicates information about the user or app initiated the activity.</span></span>|
|<span data-ttu-id="7275c-147">loggedByService</span><span class="sxs-lookup"><span data-stu-id="7275c-147">loggedByService</span></span>|<span data-ttu-id="7275c-148">String</span><span class="sxs-lookup"><span data-stu-id="7275c-148">String</span></span>|<span data-ttu-id="7275c-149">Indica información en el que la actividad iniciadas por el servicio (por ejemplo: administración de contraseñas sin intervención del administrador, directorios principales, B2C, los usuarios invitados, Microsoft Identity Manager, con privilegios de administración de identidades.</span><span class="sxs-lookup"><span data-stu-id="7275c-149">Indicates information on which service initiated the activity (For example: Self-service Password Management, Core Directory, B2C, Invited Users, Microsoft Identity Manager, Privileged Identity Management.</span></span>|
|<span data-ttu-id="7275c-150">result</span><span class="sxs-lookup"><span data-stu-id="7275c-150">result</span></span>|<span data-ttu-id="7275c-151">string</span><span class="sxs-lookup"><span data-stu-id="7275c-151">string</span></span>| <span data-ttu-id="7275c-152">Indica el resultado de la actividad. Los valores posibles son: `success`, `failure`, `timeout`, `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="7275c-152">Indicates the result of the activity.Possible values are: `success`, `failure`, `timeout`, `unknownFutureValue`.</span></span>||
|<span data-ttu-id="7275c-153">resultReason</span><span class="sxs-lookup"><span data-stu-id="7275c-153">resultReason</span></span>|<span data-ttu-id="7275c-154">String</span><span class="sxs-lookup"><span data-stu-id="7275c-154">String</span></span>|<span data-ttu-id="7275c-155">Indica el motivo del error si el resultado es "Error" o "tiempo de espera".</span><span class="sxs-lookup"><span data-stu-id="7275c-155">Indicates the reason for failure if the result is "Failure" or "timeout".</span></span>|
|<span data-ttu-id="7275c-156">targetResources</span><span class="sxs-lookup"><span data-stu-id="7275c-156">targetResources</span></span>|<span data-ttu-id="7275c-157">colección de [targetResource](targetresource.md)</span><span class="sxs-lookup"><span data-stu-id="7275c-157">[targetResource](targetresource.md) collection</span></span>|<span data-ttu-id="7275c-158">Indica información en la que el recurso se cambió debido a la actividad.</span><span class="sxs-lookup"><span data-stu-id="7275c-158">Indicates information on which resource was changed due to the activity.</span></span> <span data-ttu-id="7275c-159">Tipo de recurso de destino puede ser usuario, dispositivo, Active Directory, aplicación, rol, grupo, directiva u otra.</span><span class="sxs-lookup"><span data-stu-id="7275c-159">Target Resource Type can be User, Device, Directory, App, Role, Group, Policy or Other.</span></span>

## <a name="relationships"></a><span data-ttu-id="7275c-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7275c-160">Relationships</span></span>
<span data-ttu-id="7275c-161">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7275c-161">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="7275c-162">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7275c-162">JSON representation</span></span>

<span data-ttu-id="7275c-163">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7275c-163">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directoryAudit"
}-->

```json
{
  "activityDateTime": "String (timestamp)",
  "activityDisplayName": "String",
  "additionalDetails": [{"@odata.type": "microsoft.graph.keyValue"}],
  "category": "String",
  "correlationId": "Guid",
  "id": "String (identifier)",
  "initiatedBy": {"@odata.type": "microsoft.graph.auditActivityInitiator"},
  "loggedByService": "String",
  "result": "string",
  "resultReason": "String",
  "targetResources": [{"@odata.type": "microsoft.graph.targetResource"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryAudit resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->