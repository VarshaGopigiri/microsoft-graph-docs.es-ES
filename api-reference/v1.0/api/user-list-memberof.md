---
title: List memberOf
description: 'Obtiene todos los grupos y roles de directorio de los que el usuario sea miembro directo. '
author: dkershaw10
localization_priority: Priority
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 389cbe5a62b75e9396077d9710c0b92a497e8bd0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962530"
---
# <a name="list-memberof"></a><span data-ttu-id="2984b-103">Enumerar memberOf</span><span class="sxs-lookup"><span data-stu-id="2984b-103">List memberOf</span></span>

<span data-ttu-id="2984b-104">Obtiene todos los [grupos](../resources/group.md) y [roles de directorio](../resources/directoryrole.md) de los que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="2984b-104">Get [groups](../resources/group.md) and [directory roles](../resources/directoryrole.md) that the user is a direct member of.</span></span> 

## <a name="permissions"></a><span data-ttu-id="2984b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2984b-105">Permissions</span></span>
<span data-ttu-id="2984b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2984b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2984b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2984b-108">Permission type</span></span>      | <span data-ttu-id="2984b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2984b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2984b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2984b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2984b-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2984b-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="2984b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2984b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2984b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2984b-113">Not supported.</span></span>    |
|<span data-ttu-id="2984b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2984b-114">Application</span></span> | <span data-ttu-id="2984b-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2984b-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2984b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2984b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/memberOf
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2984b-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2984b-117">Optional query parameters</span></span>
<span data-ttu-id="2984b-p102">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta. No se admite $filter.</span><span class="sxs-lookup"><span data-stu-id="2984b-p102">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response. $filter is not supported.</span></span> 

## <a name="request-headers"></a><span data-ttu-id="2984b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2984b-120">Request headers</span></span>
| <span data-ttu-id="2984b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2984b-121">Header</span></span>       | <span data-ttu-id="2984b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2984b-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2984b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="2984b-123">Authorization</span></span>  | <span data-ttu-id="2984b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2984b-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="2984b-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2984b-126">Accept</span></span>  | <span data-ttu-id="2984b-127">application/json</span><span class="sxs-lookup"><span data-stu-id="2984b-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2984b-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2984b-128">Request body</span></span>
<span data-ttu-id="2984b-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2984b-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2984b-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2984b-130">Response</span></span>

<span data-ttu-id="2984b-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2984b-131">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2984b-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2984b-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2984b-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2984b-133">Request</span></span>
<span data-ttu-id="2984b-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2984b-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_memberof"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/memberOf
```
##### <a name="response"></a><span data-ttu-id="2984b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2984b-135">Response</span></span>
<span data-ttu-id="2984b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2984b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "id-value",
      "createdDateTime": null,
      "description": "All users at the company",
      "displayName": "All Users",
      "groupTypes": [],
      "mailEnabled": false,
      "securityEnabled": true,
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
