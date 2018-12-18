---
title: List directoryRoleTemplates
description: Recupera una lista de objetos directoryRoleTemplate.
author: lleonard-msft
ms.openlocfilehash: 0e43bdb3217827c8369ebe226a9aacea54996be2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301529"
---
# <a name="list-directoryroletemplates"></a><span data-ttu-id="bce6d-103">List directoryRoleTemplates</span><span class="sxs-lookup"><span data-stu-id="bce6d-103">List directoryRoleTemplates</span></span>

<span data-ttu-id="bce6d-104">Recupera una lista de objetos directoryRoleTemplate.</span><span class="sxs-lookup"><span data-stu-id="bce6d-104">Retrieve a list of directoryRoleTemplate objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="bce6d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bce6d-105">Permissions</span></span>
<span data-ttu-id="bce6d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bce6d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="bce6d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bce6d-108">Permission type</span></span>      | <span data-ttu-id="bce6d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bce6d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bce6d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bce6d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bce6d-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="bce6d-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="bce6d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bce6d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bce6d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bce6d-113">Not supported.</span></span>    |
|<span data-ttu-id="bce6d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bce6d-114">Application</span></span> | <span data-ttu-id="bce6d-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bce6d-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bce6d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bce6d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoleTemplates
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bce6d-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bce6d-117">Optional query parameters</span></span>
<span data-ttu-id="bce6d-118">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="bce6d-118">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="bce6d-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bce6d-119">Request headers</span></span>
| <span data-ttu-id="bce6d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="bce6d-120">Name</span></span>       | <span data-ttu-id="bce6d-121">Type</span><span class="sxs-lookup"><span data-stu-id="bce6d-121">Type</span></span> | <span data-ttu-id="bce6d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bce6d-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bce6d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="bce6d-123">Authorization</span></span>  | <span data-ttu-id="bce6d-124">string</span><span class="sxs-lookup"><span data-stu-id="bce6d-124">string</span></span>  | <span data-ttu-id="bce6d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bce6d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bce6d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bce6d-127">Request body</span></span>
<span data-ttu-id="bce6d-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bce6d-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bce6d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bce6d-129">Response</span></span>

<span data-ttu-id="bce6d-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryRoleTemplate](../resources/directoryroletemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bce6d-130">If successful, this method returns a `200 OK` response code and collection of [directoryRoleTemplate](../resources/directoryroletemplate.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bce6d-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bce6d-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bce6d-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bce6d-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directoryroletemplates"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoleTemplates
```
##### <a name="response"></a><span data-ttu-id="bce6d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bce6d-133">Response</span></span>
<span data-ttu-id="bce6d-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bce6d-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRoleTemplate",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "description": "description-value",
      "displayName": "displayName-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directoryRoleTemplates",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
