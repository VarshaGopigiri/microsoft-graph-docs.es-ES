---
title: Crear outlookTaskFolder
description: Cree una carpeta de tarea de Outlook en un outlookTaskGroup especificado.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 4d6d6f103c1dd002f4c01e0dbdd71d1ebd7ddd10
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823838"
---
# <a name="create-outlooktaskfolder"></a><span data-ttu-id="50414-103">Crear outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="50414-103">Create outlookTaskFolder</span></span>

> <span data-ttu-id="50414-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="50414-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="50414-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="50414-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="50414-106">Cree una carpeta de tarea de Outlook en un [outlookTaskGroup](../resources/outlooktaskgroup.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="50414-106">Create an Outlook task folder under a specified [outlookTaskGroup](../resources/outlooktaskgroup.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="50414-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="50414-107">Permissions</span></span>
<span data-ttu-id="50414-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="50414-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="50414-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="50414-110">Permission type</span></span>      | <span data-ttu-id="50414-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="50414-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="50414-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="50414-112">Delegated (work or school account)</span></span> | <span data-ttu-id="50414-113">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="50414-113">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="50414-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="50414-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="50414-115">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="50414-115">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="50414-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="50414-116">Application</span></span> | <span data-ttu-id="50414-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50414-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="50414-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="50414-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders

```
## <a name="request-headers"></a><span data-ttu-id="50414-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="50414-119">Request headers</span></span>
| <span data-ttu-id="50414-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="50414-120">Name</span></span>       | <span data-ttu-id="50414-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="50414-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="50414-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="50414-122">Authorization</span></span>  | <span data-ttu-id="50414-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="50414-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="50414-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="50414-125">Request body</span></span>
<span data-ttu-id="50414-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTaskFolder](../resources/outlooktaskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="50414-126">In the request body, supply a JSON representation of [outlookTaskFolder](../resources/outlooktaskfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="50414-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50414-127">Response</span></span>

<span data-ttu-id="50414-128">Si tiene éxito, este método devuelve `201 Created` objeto de código y [outlookTaskFolder](../resources/outlooktaskfolder.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50414-128">If successful, this method returns `201 Created` response code and [outlookTaskFolder](../resources/outlooktaskfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="50414-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50414-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="50414-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="50414-130">Request</span></span>
<span data-ttu-id="50414-131">En el ejemplo siguiente se crea una carpeta de tarea denominada `Cooking` en el grupo de tareas especificado.</span><span class="sxs-lookup"><span data-stu-id="50414-131">The following example creates a task folder called `Cooking` in the specified task group.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_outlooktaskfolder_from_outlooktaskgroup"
}-->
```http
POST https://graph.microsoft.com/beta/me/taskgroups('AAMkADIyAAAhrbe-AAA')/taskfolders 

Content-type: application/json
Content-length: 131

{
  "name": "Cooking"
}
```
<span data-ttu-id="50414-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTaskFolder](../resources/outlooktaskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="50414-132">In the request body, supply a JSON representation of [outlookTaskFolder](../resources/outlooktaskfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="50414-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50414-133">Response</span></span>
<span data-ttu-id="50414-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="50414-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "id": "AAMkADIyAAAhrbPXAAA=",
  "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAIbAOlA==",
  "isDefaultFolder": false,
  "name": "Cooking",
  "parentGroupKey": "63d640cf-946f-4734-9c29-60dda7b76acb"
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
