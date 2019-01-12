---
title: Obtener outlookTaskFolder
description: Obtener las propiedades y relaciones de la carpeta de tareas de Outlook especificada.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 7e8f8e9c1fa16b5e0a00b0f779d652d2c6e1aa93
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929224"
---
# <a name="get-outlooktaskfolder"></a><span data-ttu-id="809f1-103">Obtener outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="809f1-103">Get outlookTaskFolder</span></span>

> <span data-ttu-id="809f1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="809f1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="809f1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="809f1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="809f1-106">Obtener las propiedades y relaciones de la carpeta de tareas de Outlook especificada.</span><span class="sxs-lookup"><span data-stu-id="809f1-106">Get the properties and relationships of the specified Outlook task folder.</span></span>
## <a name="permissions"></a><span data-ttu-id="809f1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="809f1-107">Permissions</span></span>
<span data-ttu-id="809f1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="809f1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="809f1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="809f1-110">Permission type</span></span>      | <span data-ttu-id="809f1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="809f1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="809f1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="809f1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="809f1-113">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="809f1-113">Tasks.Read</span></span>    |
|<span data-ttu-id="809f1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="809f1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="809f1-115">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="809f1-115">Tasks.Read</span></span>    |
|<span data-ttu-id="809f1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="809f1-116">Application</span></span> | <span data-ttu-id="809f1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="809f1-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="809f1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="809f1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id|userPrincipalName}/outlook/taskFolders/{id}
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="809f1-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="809f1-119">Optional query parameters</span></span>
<span data-ttu-id="809f1-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="809f1-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="809f1-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="809f1-121">Request headers</span></span>
| <span data-ttu-id="809f1-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="809f1-122">Name</span></span>      |<span data-ttu-id="809f1-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="809f1-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="809f1-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="809f1-124">Authorization</span></span>  | <span data-ttu-id="809f1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="809f1-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="809f1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="809f1-127">Request body</span></span>
<span data-ttu-id="809f1-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="809f1-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="809f1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="809f1-129">Response</span></span>

<span data-ttu-id="809f1-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [outlookTaskFolder](../resources/outlooktaskfolder.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="809f1-130">If successful, this method returns a `200 OK` response code and [outlookTaskFolder](../resources/outlooktaskfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="809f1-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="809f1-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="809f1-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="809f1-132">Request</span></span>
<span data-ttu-id="809f1-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="809f1-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_outlooktaskfolder"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/taskFolders('AAMkADIyAAAAABrJAAA=')
```
##### <a name="response"></a><span data-ttu-id="809f1-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="809f1-134">Response</span></span>
<span data-ttu-id="809f1-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="809f1-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "id": "AAMkADIyAAAAABrJAAA=",
  "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAAAAeAA==",
  "isDefaultFolder": false,
  "name": "Monthly tasks",
  "parentGroupKey": "0006f0b7-0000-0000-c000-000000000046"

}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get outlookTaskFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
