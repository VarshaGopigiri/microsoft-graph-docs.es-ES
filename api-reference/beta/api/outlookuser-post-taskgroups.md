---
title: Crear outlookTaskGroup
description: Cree un grupo de tareas de Outlook en el buzón del usuario.
ms.openlocfilehash: dc3efc7b663d5eab3d9165b1d72fec5dd187db53
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091070"
---
# <a name="create-outlooktaskgroup"></a><span data-ttu-id="b2f9d-103">Crear outlookTaskGroup</span><span class="sxs-lookup"><span data-stu-id="b2f9d-103">Create outlookTaskGroup</span></span>

> <span data-ttu-id="b2f9d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b2f9d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b2f9d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b2f9d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b2f9d-106">Cree un grupo de tareas de Outlook en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="b2f9d-106">Create an Outlook task group in the user's mailbox.</span></span>
## <a name="permissions"></a><span data-ttu-id="b2f9d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b2f9d-107">Permissions</span></span>
<span data-ttu-id="b2f9d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b2f9d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b2f9d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b2f9d-110">Permission type</span></span>      | <span data-ttu-id="b2f9d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b2f9d-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b2f9d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b2f9d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b2f9d-113">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b2f9d-113">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="b2f9d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b2f9d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b2f9d-115">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b2f9d-115">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="b2f9d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b2f9d-116">Application</span></span> | <span data-ttu-id="b2f9d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2f9d-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b2f9d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b2f9d-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id|userPrincipalName}/outlook/taskGroups

```
## <a name="request-headers"></a><span data-ttu-id="b2f9d-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2f9d-119">Request headers</span></span>
| <span data-ttu-id="b2f9d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b2f9d-120">Name</span></span>       | <span data-ttu-id="b2f9d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2f9d-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b2f9d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b2f9d-122">Authorization</span></span>  | <span data-ttu-id="b2f9d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b2f9d-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b2f9d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b2f9d-125">Request body</span></span>
<span data-ttu-id="b2f9d-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTaskGroup](../resources/outlooktaskgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f9d-126">In the request body, supply a JSON representation of [outlookTaskGroup](../resources/outlooktaskgroup.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="b2f9d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2f9d-127">Response</span></span>

<span data-ttu-id="b2f9d-128">Si tiene éxito, este método devuelve `201 Created` objeto de código y [outlookTaskGroup](../resources/outlooktaskgroup.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2f9d-128">If successful, this method returns `201 Created` response code and [outlookTaskGroup](../resources/outlooktaskgroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b2f9d-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2f9d-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b2f9d-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b2f9d-130">Request</span></span>
<span data-ttu-id="b2f9d-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2f9d-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_outlooktaskgroup_from_outlookuser"
}-->
```http
POST https://graph.microsoft.com/beta/me/outlook/taskGroups
Content-type: application/json
Content-length: 40

{
  "name": "Leisure tasks"
}
```
<span data-ttu-id="b2f9d-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTaskGroup](../resources/outlooktaskgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f9d-132">In the request body, supply a JSON representation of [outlookTaskGroup](../resources/outlooktaskgroup.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="b2f9d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2f9d-133">Response</span></span>
<span data-ttu-id="b2f9d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b2f9d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTaskGroup"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 138

{
  "id": "AAMkADIyAAAhrbe-AAA=",
  "changeKey": "hmM7Eb/jgEec8l3+gkJEawAAIbAGjg==",
  "isDefaultGroup": false,
  "name": "Leisure tasks",
  "groupKey": "63d640cf-946f-4734-9c29-60dda7b76acb"

}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create outlookTaskGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->