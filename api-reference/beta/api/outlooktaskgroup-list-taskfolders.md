---
title: Lista taskFolders
description: Obtener las carpetas de tareas de Outlook en un outlookTaskGroup específico.
author: angelgolfer-ms
ms.openlocfilehash: b128542ddcfe78cb379da1a7b87f1ee012858cc4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354736"
---
# <a name="list-taskfolders"></a><span data-ttu-id="de8ab-103">Lista taskFolders</span><span class="sxs-lookup"><span data-stu-id="de8ab-103">List taskFolders</span></span>

> <span data-ttu-id="de8ab-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="de8ab-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="de8ab-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="de8ab-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="de8ab-106">Obtener las carpetas de tareas de Outlook en un determinado [outlookTaskGroup](../resources/outlooktaskgroup.md).</span><span class="sxs-lookup"><span data-stu-id="de8ab-106">Get Outlook task folders in a specific [outlookTaskGroup](../resources/outlooktaskgroup.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="de8ab-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="de8ab-107">Permissions</span></span>
<span data-ttu-id="de8ab-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="de8ab-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="de8ab-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="de8ab-110">Permission type</span></span>      | <span data-ttu-id="de8ab-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="de8ab-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="de8ab-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="de8ab-112">Delegated (work or school account)</span></span> | <span data-ttu-id="de8ab-113">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="de8ab-113">Tasks.Read</span></span>    |
|<span data-ttu-id="de8ab-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="de8ab-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="de8ab-115">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="de8ab-115">Tasks.Read</span></span>    |
|<span data-ttu-id="de8ab-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="de8ab-116">Application</span></span> | <span data-ttu-id="de8ab-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de8ab-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="de8ab-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="de8ab-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="de8ab-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="de8ab-119">Optional query parameters</span></span>
<span data-ttu-id="de8ab-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de8ab-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="de8ab-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="de8ab-121">Request headers</span></span>
| <span data-ttu-id="de8ab-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="de8ab-122">Name</span></span>      |<span data-ttu-id="de8ab-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="de8ab-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="de8ab-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="de8ab-124">Authorization</span></span>  | <span data-ttu-id="de8ab-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="de8ab-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="de8ab-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="de8ab-127">Request body</span></span>
<span data-ttu-id="de8ab-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="de8ab-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="de8ab-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de8ab-129">Response</span></span>

<span data-ttu-id="de8ab-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [outlookTaskFolder](../resources/outlooktaskfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de8ab-130">If successful, this method returns a `200 OK` response code and collection of [outlookTaskFolder](../resources/outlooktaskfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="de8ab-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de8ab-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="de8ab-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="de8ab-132">Request</span></span>
<span data-ttu-id="de8ab-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="de8ab-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_taskfolders"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/taskGroups('AAMkADIyAAAhrbe-AAA=')/taskFolders
```
##### <a name="response"></a><span data-ttu-id="de8ab-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de8ab-134">Response</span></span>
<span data-ttu-id="de8ab-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="de8ab-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTaskFolder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 200

{
  "value": [
    {
      "id": "AAMkADIyAAAhrbPXAAA=",
      "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAIbAOlA==",
      "isDefaultFolder": false,
      "name": "Cooking",
      "parentGroupKey": "63d640cf-946f-4734-9c29-60dda7b76acb"
    }

  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List taskFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->