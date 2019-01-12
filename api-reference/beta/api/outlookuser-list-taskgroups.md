---
title: Lista taskGroups
description: Obtener todos los grupos de tareas de Outlook en el buzón del usuario.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 3e0146a40698f8f150f39064b38aa562756b64ae
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27913712"
---
# <a name="list-taskgroups"></a><span data-ttu-id="36382-103">Lista taskGroups</span><span class="sxs-lookup"><span data-stu-id="36382-103">List taskGroups</span></span>

> <span data-ttu-id="36382-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="36382-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="36382-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="36382-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="36382-106">Obtener todos los grupos de tareas de Outlook en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="36382-106">Get all the Outlook task groups in the user's mailbox.</span></span>

<span data-ttu-id="36382-107">La respuesta incluye siempre el grupo de tareas predeterminada `My Tasks`y otros grupos de tareas que se han creado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="36382-107">The response always includes the default task group `My Tasks`, and any other task groups that have been created in the mailbox.</span></span>
## <a name="permissions"></a><span data-ttu-id="36382-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="36382-108">Permissions</span></span>
<span data-ttu-id="36382-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="36382-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="36382-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="36382-111">Permission type</span></span>      | <span data-ttu-id="36382-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="36382-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="36382-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="36382-113">Delegated (work or school account)</span></span> | <span data-ttu-id="36382-114">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="36382-114">Tasks.Read</span></span>    |
|<span data-ttu-id="36382-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="36382-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="36382-116">Tasks.Read</span><span class="sxs-lookup"><span data-stu-id="36382-116">Tasks.Read</span></span>    |
|<span data-ttu-id="36382-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="36382-117">Application</span></span> | <span data-ttu-id="36382-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36382-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="36382-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="36382-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id|userPrincipalName}/outlook/taskGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="36382-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="36382-120">Optional query parameters</span></span>
<span data-ttu-id="36382-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="36382-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="36382-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="36382-122">Request headers</span></span>
| <span data-ttu-id="36382-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="36382-123">Name</span></span>      |<span data-ttu-id="36382-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="36382-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="36382-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="36382-125">Authorization</span></span>  | <span data-ttu-id="36382-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="36382-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="36382-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="36382-128">Request body</span></span>
<span data-ttu-id="36382-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="36382-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="36382-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36382-130">Response</span></span>

<span data-ttu-id="36382-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [outlookTaskGroup](../resources/outlooktaskgroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="36382-131">If successful, this method returns a `200 OK` response code and collection of [outlookTaskGroup](../resources/outlooktaskgroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="36382-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="36382-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="36382-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="36382-133">Request</span></span>
<span data-ttu-id="36382-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="36382-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_taskgroups"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/taskGroups
```
##### <a name="response"></a><span data-ttu-id="36382-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36382-135">Response</span></span>
<span data-ttu-id="36382-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="36382-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTaskGroup",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 187

{
  "value": [
    {
      "id": "AAMkADIyAAADJ5pYAAA=",
      "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAInHxLA==",
      "isDefaultGroup": true,
      "name": "My Tasks",
      "groupKey": "0006f0b7-0000-0000-c000-000000000046"
    },
    {
      "id": "AAMkADIyAAAhrbe-AAA=",
      "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAInHxKw==",
      "isDefaultGroup": false,
      "name": "Leisure Tasks",
      "groupKey": "63d640cf-946f-4734-9c29-60dda7b76acb"
    }

  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List TaskGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
