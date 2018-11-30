---
title: Actualizar outlooktaskfolder
description: Actualizar las propiedades modificables de una carpeta de tarea de Outlook.
ms.openlocfilehash: 8b02f3b8eea104ba0a0cfaa3fddaf286fa41f389
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090026"
---
# <a name="update-outlooktaskfolder"></a><span data-ttu-id="dc863-103">Actualizar outlooktaskfolder</span><span class="sxs-lookup"><span data-stu-id="dc863-103">Update outlooktaskfolder</span></span>

> <span data-ttu-id="dc863-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dc863-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dc863-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dc863-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dc863-106">Actualizar las propiedades modificables de una carpeta de tarea de Outlook.</span><span class="sxs-lookup"><span data-stu-id="dc863-106">Update the writable properties of an Outlook task folder.</span></span>

<span data-ttu-id="dc863-107">No se puede cambiar el valor de la propiedad **nombre** de la carpeta tareas predeterminada, "Tareas".</span><span class="sxs-lookup"><span data-stu-id="dc863-107">You cannot change the **name** property value of the default task folder, "Tasks".</span></span>
## <a name="permissions"></a><span data-ttu-id="dc863-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="dc863-108">Permissions</span></span>
<span data-ttu-id="dc863-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc863-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dc863-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dc863-111">Permission type</span></span>      | <span data-ttu-id="dc863-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dc863-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dc863-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dc863-113">Delegated (work or school account)</span></span> | <span data-ttu-id="dc863-114">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dc863-114">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="dc863-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dc863-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dc863-116">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dc863-116">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="dc863-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dc863-117">Application</span></span> | <span data-ttu-id="dc863-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc863-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dc863-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dc863-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id|userPrincipalName}/outlook/taskFolders/{id}
PATCH /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="dc863-120">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="dc863-120">Optional request headers</span></span>
| <span data-ttu-id="dc863-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="dc863-121">Name</span></span>       | <span data-ttu-id="dc863-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc863-122">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="dc863-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="dc863-123">Authorization</span></span>  | <span data-ttu-id="dc863-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dc863-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dc863-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dc863-126">Request body</span></span>
<span data-ttu-id="dc863-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="dc863-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="dc863-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc863-130">Property</span></span>     | <span data-ttu-id="dc863-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc863-131">Type</span></span>   |<span data-ttu-id="dc863-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc863-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dc863-133">name</span><span class="sxs-lookup"><span data-stu-id="dc863-133">name</span></span>|<span data-ttu-id="dc863-134">String</span><span class="sxs-lookup"><span data-stu-id="dc863-134">String</span></span>|<span data-ttu-id="dc863-135">El nombre de la carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="dc863-135">The name of the task folder.</span></span>|

## <a name="response"></a><span data-ttu-id="dc863-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc863-136">Response</span></span>

<span data-ttu-id="dc863-137">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [outlookTaskFolder](../resources/outlooktaskfolder.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc863-137">If successful, this method returns a `200 OK` response code and updated [outlookTaskFolder](../resources/outlooktaskfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="dc863-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc863-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dc863-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dc863-139">Request</span></span>
<span data-ttu-id="dc863-140">En el ejemplo siguiente se cambia el nombre de la carpeta de la tarea especificada a `Charity work`.</span><span class="sxs-lookup"><span data-stu-id="dc863-140">The following example changes the name of the specified task folder to `Charity work`.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_outlooktaskfolder"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/outlook/taskFolders('AAMkADIyAAAhrbPWAAA=')
Content-type: application/json
Content-length: 31

{
  "name": "Charity work"
}
```
##### <a name="response"></a><span data-ttu-id="dc863-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc863-141">Response</span></span>
<span data-ttu-id="dc863-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dc863-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTaskFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 151

{
  "id": "AAMkADIyAAAhrbPWAAA=",
  "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAIbAKfQ==",
  "isDefaultFolder": false,
  "name": "Charity work",
  "parentGroupKey": "0006f0b7-0000-0000-c000-000000000046"

}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update outlooktaskfolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->