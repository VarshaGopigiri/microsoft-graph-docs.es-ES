---
title: Enumerar miembros
description: Recupera una lista de los usuarios que están asignados al rol de directorio.  Solo los usuarios se pueden asignar a un rol de directorio.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: ad27b5d4a56bee9e149b9f6de87271a86e9945e4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970811"
---
# <a name="list-members"></a><span data-ttu-id="4bd11-104">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="4bd11-104">List members</span></span>

> <span data-ttu-id="4bd11-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4bd11-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4bd11-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4bd11-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4bd11-p103">Recupera una lista de los usuarios que están asignados al rol de directorio.  Solo los usuarios se pueden asignar a un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="4bd11-p103">Retrieve a list of the users that are assigned to the directory role.  Only users can be assigned to a directory role.</span></span>
## <a name="permissions"></a><span data-ttu-id="4bd11-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="4bd11-109">Permissions</span></span>
<span data-ttu-id="4bd11-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4bd11-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="4bd11-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4bd11-112">Permission type</span></span>      | <span data-ttu-id="4bd11-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4bd11-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4bd11-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4bd11-114">Delegated (work or school account)</span></span> | <span data-ttu-id="4bd11-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4bd11-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4bd11-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4bd11-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4bd11-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4bd11-117">Not supported.</span></span>    |
|<span data-ttu-id="4bd11-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4bd11-118">Application</span></span> | <span data-ttu-id="4bd11-119">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4bd11-119">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4bd11-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4bd11-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/{id}/members
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4bd11-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4bd11-121">Optional query parameters</span></span>
<span data-ttu-id="4bd11-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4bd11-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="4bd11-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4bd11-123">Request headers</span></span>
| <span data-ttu-id="4bd11-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="4bd11-124">Name</span></span>       | <span data-ttu-id="4bd11-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="4bd11-125">Type</span></span> | <span data-ttu-id="4bd11-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bd11-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="4bd11-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="4bd11-127">Authorization</span></span>  | <span data-ttu-id="4bd11-128">string</span><span class="sxs-lookup"><span data-stu-id="4bd11-128">string</span></span>  | <span data-ttu-id="4bd11-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4bd11-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4bd11-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4bd11-131">Request body</span></span>
<span data-ttu-id="4bd11-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4bd11-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4bd11-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4bd11-133">Response</span></span>

<span data-ttu-id="4bd11-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4bd11-134">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4bd11-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4bd11-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4bd11-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4bd11-136">Request</span></span>
<span data-ttu-id="4bd11-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4bd11-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/beta/directoryRoles/{id}/members
```
##### <a name="response"></a><span data-ttu-id="4bd11-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4bd11-138">Response</span></span>
<span data-ttu-id="4bd11-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4bd11-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List members",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
