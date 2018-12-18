---
title: List attachments
description: Obtener una lista de objetos de datos adjuntos asociados a una tarea de Outlook.
author: angelgolfer-ms
ms.openlocfilehash: db27cfa94e90607e64bed0bf71f55dfbea14b7e5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309936"
---
# <a name="list-attachments"></a><span data-ttu-id="937bc-103">List attachments</span><span class="sxs-lookup"><span data-stu-id="937bc-103">List attachments</span></span>

> <span data-ttu-id="937bc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="937bc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="937bc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="937bc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="937bc-106">Obtener una lista de objetos de [datos adjuntos](../resources/attachment.md) asociados a una tarea de Outlook.</span><span class="sxs-lookup"><span data-stu-id="937bc-106">Get a list of [attachment](../resources/attachment.md) objects attached to an Outlook task.</span></span>
## <a name="permissions"></a><span data-ttu-id="937bc-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="937bc-107">Permissions</span></span>
<span data-ttu-id="937bc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="937bc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="937bc-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="937bc-110">Permission type</span></span>      | <span data-ttu-id="937bc-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="937bc-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="937bc-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="937bc-112">Delegated (work or school account)</span></span> | <span data-ttu-id="937bc-113">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="937bc-113">Tasks.Read</span></span>    |
|<span data-ttu-id="937bc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="937bc-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="937bc-115">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="937bc-115">Tasks.Read</span></span>    |
|<span data-ttu-id="937bc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="937bc-116">Application</span></span> | <span data-ttu-id="937bc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="937bc-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="937bc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="937bc-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id|userPrincipalName}/outlook/tasks/{id}/attachments
GET /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks/{id}/attachments
GET /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="937bc-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="937bc-119">Optional query parameters</span></span>
<span data-ttu-id="937bc-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="937bc-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="937bc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="937bc-121">Request headers</span></span>
| <span data-ttu-id="937bc-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="937bc-122">Name</span></span>      |<span data-ttu-id="937bc-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="937bc-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="937bc-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="937bc-124">Authorization</span></span>  | <span data-ttu-id="937bc-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="937bc-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="937bc-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="937bc-127">Request body</span></span>
<span data-ttu-id="937bc-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="937bc-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="937bc-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="937bc-129">Response</span></span>

<span data-ttu-id="937bc-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [datos adjuntos](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="937bc-130">If successful, this method returns a `200 OK` response code and collection of [attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="937bc-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="937bc-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="937bc-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="937bc-132">Request</span></span>
<span data-ttu-id="937bc-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="937bc-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/beta/users/{id}/outlook/tasks/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="937bc-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="937bc-134">Response</span></span>
<span data-ttu-id="937bc-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="937bc-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "value": [
    {
      "lastModifiedDateTime": "datetime-value",
      "name": "name-value",
      "contentType": "contentType-value",
      "size": 99,
      "isInline": true,
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List attachments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->