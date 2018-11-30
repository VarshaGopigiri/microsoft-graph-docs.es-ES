---
title: Actualizar outlooktaskgroup
description: Actualizar las propiedades modificables de un grupo de tareas de Outlook.
ms.openlocfilehash: cbe2ae7248f37d9d243673610550a6a974acffb0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085363"
---
# <a name="update-outlooktaskgroup"></a><span data-ttu-id="30a87-103">Actualizar outlooktaskgroup</span><span class="sxs-lookup"><span data-stu-id="30a87-103">Update outlooktaskgroup</span></span>

> <span data-ttu-id="30a87-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="30a87-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="30a87-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="30a87-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="30a87-106">Actualizar las propiedades modificables de un grupo de tareas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="30a87-106">Update the writable properties of an Outlook task group.</span></span>

<span data-ttu-id="30a87-107">Tenga en cuenta que no se puede modificar el nombre del grupo de tarea predeterminado, "Mis tareas".</span><span class="sxs-lookup"><span data-stu-id="30a87-107">Note that you cannot modify the name of the default task group, "My Tasks".</span></span>
## <a name="permissions"></a><span data-ttu-id="30a87-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="30a87-108">Permissions</span></span>
<span data-ttu-id="30a87-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="30a87-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="30a87-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30a87-111">Permission type</span></span>      | <span data-ttu-id="30a87-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30a87-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="30a87-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30a87-113">Delegated (work or school account)</span></span> | <span data-ttu-id="30a87-114">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="30a87-114">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="30a87-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30a87-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="30a87-116">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="30a87-116">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="30a87-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30a87-117">Application</span></span> | <span data-ttu-id="30a87-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30a87-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="30a87-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30a87-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id|userPrincipalName}/outlook/taskGroups/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="30a87-120">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="30a87-120">Optional request headers</span></span>
| <span data-ttu-id="30a87-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="30a87-121">Name</span></span>       | <span data-ttu-id="30a87-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="30a87-122">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="30a87-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="30a87-123">Authorization</span></span>  | <span data-ttu-id="30a87-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="30a87-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="30a87-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30a87-126">Request body</span></span>
<span data-ttu-id="30a87-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="30a87-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="30a87-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="30a87-130">Property</span></span>     | <span data-ttu-id="30a87-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="30a87-131">Type</span></span>   |<span data-ttu-id="30a87-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="30a87-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="30a87-133">name</span><span class="sxs-lookup"><span data-stu-id="30a87-133">name</span></span>|<span data-ttu-id="30a87-134">String</span><span class="sxs-lookup"><span data-stu-id="30a87-134">String</span></span>|<span data-ttu-id="30a87-135">El nombre del grupo de tareas.</span><span class="sxs-lookup"><span data-stu-id="30a87-135">The name of the task group.</span></span>|

## <a name="response"></a><span data-ttu-id="30a87-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30a87-136">Response</span></span>

<span data-ttu-id="30a87-137">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [outlookTaskGroup](../resources/outlooktaskgroup.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30a87-137">If successful, this method returns a `200 OK` response code and updated [outlookTaskGroup](../resources/outlooktaskgroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="30a87-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30a87-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="30a87-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30a87-139">Request</span></span>
<span data-ttu-id="30a87-140">En el ejemplo siguiente se cambia el nombre de un grupo de tareas por "Personal Tasks".</span><span class="sxs-lookup"><span data-stu-id="30a87-140">The following example changes the name of a task group to "Personal Tasks".</span></span> 
<!-- {
  "blockType": "request",
  "name": "update_outlooktaskgroup"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/outlook/taskgroups('AAMkADIyAAAhrbe-AAA=')

Content-type: application/json
Content-length: 28

{
  "name": "Personal Tasks",
}
```
##### <a name="response"></a><span data-ttu-id="30a87-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30a87-141">Response</span></span>
<span data-ttu-id="30a87-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30a87-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTaskGroup"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 138

{
  "id": "AAMkADIyAAAhrbe-AAA=",
  "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAIbAGjw==",
  "isDefaultGroup": false,
  "name": "Personal Tasks",
  "groupKey": "63d640cf-946f-4734-9c29-60dda7b76acb"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update outlooktaskgroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->