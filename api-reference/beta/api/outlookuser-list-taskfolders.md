---
title: Lista taskFolders
description: Obtenga todas las carpetas de tareas de Outlook en el buzón del usuario.
ms.openlocfilehash: 5c5636af9abe46b67d29fa03ae39d3020173849a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085361"
---
# <a name="list-taskfolders"></a><span data-ttu-id="1935c-103">Lista taskFolders</span><span class="sxs-lookup"><span data-stu-id="1935c-103">List taskFolders</span></span>

> <span data-ttu-id="1935c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1935c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1935c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1935c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1935c-106">Obtenga todas las carpetas de tareas de Outlook en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="1935c-106">Get all the Outlook task folders in the user's mailbox.</span></span>
## <a name="permissions"></a><span data-ttu-id="1935c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1935c-107">Permissions</span></span>
<span data-ttu-id="1935c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1935c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1935c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1935c-110">Permission type</span></span>      | <span data-ttu-id="1935c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1935c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1935c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1935c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1935c-113">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="1935c-113">Tasks.Read</span></span>    |
|<span data-ttu-id="1935c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1935c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1935c-115">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="1935c-115">Tasks.Read</span></span>    |
|<span data-ttu-id="1935c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1935c-116">Application</span></span> | <span data-ttu-id="1935c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1935c-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1935c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1935c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id|userPrincipalName}/outlook/taskFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1935c-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1935c-119">Optional query parameters</span></span>
<span data-ttu-id="1935c-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1935c-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1935c-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1935c-121">Request headers</span></span>
| <span data-ttu-id="1935c-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="1935c-122">Name</span></span>      |<span data-ttu-id="1935c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1935c-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="1935c-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="1935c-124">Authorization</span></span>  | <span data-ttu-id="1935c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1935c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1935c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1935c-127">Request body</span></span>
<span data-ttu-id="1935c-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1935c-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1935c-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1935c-129">Response</span></span>

<span data-ttu-id="1935c-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [outlookTaskFolder](../resources/outlooktaskfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1935c-130">If successful, this method returns a `200 OK` response code and collection of [outlookTaskFolder](../resources/outlooktaskfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1935c-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1935c-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1935c-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1935c-132">Request</span></span>
<span data-ttu-id="1935c-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1935c-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_taskfolders"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/taskFolders
```
##### <a name="response"></a><span data-ttu-id="1935c-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1935c-134">Response</span></span>
<span data-ttu-id="1935c-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1935c-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "id": "AAMkADIyAAAAABrJAAA=",
      "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAAAAeAA==",
      "isDefaultFolder": false,
      "name": "Monthly tasks",
      "parentGroupKey": "0006f0b7-0000-0000-c000-000000000046"
    },
    {
      "id": "AAMkADIyAAAAAAESAAA=",
      "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAAAAAPA==",
      "isDefaultFolder": true,
      "name": "Tasks",
      "parentGroupKey": "0006f0b7-0000-0000-c000-000000000046"
    }

  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List TaskFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->