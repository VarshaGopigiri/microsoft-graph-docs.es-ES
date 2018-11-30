---
title: Crear outlookTaskFolder
description: Cree una carpeta de tarea en el grupo de tarea predeterminado (`My Tasks`) del buzón de usuario.
ms.openlocfilehash: 688f3dfb603bec1bc5acb05344e1dc9e8465ae47
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087360"
---
# <a name="create-outlooktaskfolder"></a><span data-ttu-id="e8bf6-103">Crear outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="e8bf6-103">Create outlookTaskFolder</span></span>

> <span data-ttu-id="e8bf6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e8bf6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e8bf6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e8bf6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e8bf6-106">Cree una carpeta de tarea en el grupo de tarea predeterminado (`My Tasks`) del buzón de usuario.</span><span class="sxs-lookup"><span data-stu-id="e8bf6-106">Create a task folder in the default task group (`My Tasks`) of the user's mailbox.</span></span>

## <a name="permissions"></a><span data-ttu-id="e8bf6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e8bf6-107">Permissions</span></span>
<span data-ttu-id="e8bf6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e8bf6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e8bf6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e8bf6-110">Permission type</span></span>      | <span data-ttu-id="e8bf6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e8bf6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e8bf6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e8bf6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e8bf6-113">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8bf6-113">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="e8bf6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e8bf6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e8bf6-115">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8bf6-115">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="e8bf6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e8bf6-116">Application</span></span> | <span data-ttu-id="e8bf6-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8bf6-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e8bf6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e8bf6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id|userPrincipalName}/outlook/taskFolders

```
## <a name="request-headers"></a><span data-ttu-id="e8bf6-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e8bf6-119">Request headers</span></span>
| <span data-ttu-id="e8bf6-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e8bf6-120">Name</span></span>       | <span data-ttu-id="e8bf6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8bf6-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e8bf6-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e8bf6-122">Authorization</span></span>  | <span data-ttu-id="e8bf6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e8bf6-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e8bf6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e8bf6-125">Request body</span></span>
<span data-ttu-id="e8bf6-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTaskFolder](../resources/outlooktaskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="e8bf6-126">In the request body, supply a JSON representation of [outlookTaskFolder](../resources/outlooktaskfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="e8bf6-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8bf6-127">Response</span></span>

<span data-ttu-id="e8bf6-128">Si tiene éxito, este método devuelve `201 Created` objeto de código y [outlookTaskFolder](../resources/outlooktaskfolder.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8bf6-128">If successful, this method returns `201 Created` response code and [outlookTaskFolder](../resources/outlooktaskfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e8bf6-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8bf6-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e8bf6-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e8bf6-130">Request</span></span>
<span data-ttu-id="e8bf6-131">En el ejemplo siguiente se crea una carpeta de tarea denominada voluntario en el grupo de tarea predeterminado (`My Tasks`) del buzón de usuario.</span><span class="sxs-lookup"><span data-stu-id="e8bf6-131">The following example creates a task folder called Volunteer in the default task group (`My Tasks`) of the user's mailbox.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_outlooktaskfolder_from_outlookuser"
}-->
```http
POST https://graph.microsoft.com/beta/me/outlook/taskfolders 
Content-type: application/json
Content-length: 60

{
  "name": "Volunteer"
}
```
<span data-ttu-id="e8bf6-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTaskFolder](../resources/outlooktaskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="e8bf6-132">In the request body, supply a JSON representation of [outlookTaskFolder](../resources/outlooktaskfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="e8bf6-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8bf6-133">Response</span></span>
<span data-ttu-id="e8bf6-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e8bf6-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTaskFolder"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 151

{
  "id": "AAMkADIyAAAhrbPWAAA=",
  "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAIbAGig==",
  "isDefaultFolder": false,
  "name": "Volunteer",
  "parentGroupKey": "0006f0b7-0000-0000-c000-000000000046"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create outlookTaskFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->