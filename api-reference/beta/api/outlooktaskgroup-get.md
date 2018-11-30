---
title: Obtener outlookTaskGroup
description: Obtener las propiedades y relaciones del grupo de tareas de Outlook especificado.
ms.openlocfilehash: ca1ceaf41c7664d83cfd042a61cf98c105bfdd73
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090840"
---
# <a name="get-outlooktaskgroup"></a><span data-ttu-id="89d0f-103">Obtener outlookTaskGroup</span><span class="sxs-lookup"><span data-stu-id="89d0f-103">Get outlookTaskGroup</span></span>

> <span data-ttu-id="89d0f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="89d0f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="89d0f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="89d0f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="89d0f-106">Obtener las propiedades y relaciones del grupo de tareas de Outlook especificado.</span><span class="sxs-lookup"><span data-stu-id="89d0f-106">Get the properties and relationships of the specified Outlook task group.</span></span>
## <a name="permissions"></a><span data-ttu-id="89d0f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="89d0f-107">Permissions</span></span>
<span data-ttu-id="89d0f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="89d0f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="89d0f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="89d0f-110">Permission type</span></span>      | <span data-ttu-id="89d0f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="89d0f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="89d0f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="89d0f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="89d0f-113">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="89d0f-113">Tasks.Read</span></span>    |
|<span data-ttu-id="89d0f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89d0f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="89d0f-115">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="89d0f-115">Tasks.Read</span></span>    |
|<span data-ttu-id="89d0f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="89d0f-116">Application</span></span> | <span data-ttu-id="89d0f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89d0f-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="89d0f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="89d0f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="89d0f-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="89d0f-119">Optional query parameters</span></span>
<span data-ttu-id="89d0f-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89d0f-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="89d0f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="89d0f-121">Request headers</span></span>
| <span data-ttu-id="89d0f-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="89d0f-122">Name</span></span>      |<span data-ttu-id="89d0f-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="89d0f-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="89d0f-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="89d0f-124">Authorization</span></span>  | <span data-ttu-id="89d0f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="89d0f-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="89d0f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="89d0f-127">Request body</span></span>
<span data-ttu-id="89d0f-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="89d0f-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="89d0f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89d0f-129">Response</span></span>

<span data-ttu-id="89d0f-130">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [outlookTaskGroup](../resources/outlooktaskgroup.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89d0f-130">If successful, this method returns a `200 OK` response code and [outlookTaskGroup](../resources/outlooktaskgroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="89d0f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89d0f-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="89d0f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="89d0f-132">Request</span></span>
<span data-ttu-id="89d0f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="89d0f-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_outlooktaskgroup"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/taskGroups('AAMkADIyAAAhrbe-AAA=')
```
##### <a name="response"></a><span data-ttu-id="89d0f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89d0f-134">Response</span></span>
<span data-ttu-id="89d0f-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="89d0f-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAInHxKw==",
    "isDefaultGroup": false,
    "name": "Leisure Tasks",
    "groupKey": "63d640cf-946f-4734-9c29-60dda7b76acb"

}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get outlookTaskGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->