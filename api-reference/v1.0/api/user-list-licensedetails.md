---
title: Enumerar licenseDetails
description: Recupera una lista de objetos licenseDetails.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 0ad9b10a377e89858cad03d3eabe4e62a4f86627
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931828"
---
# <a name="list-licensedetails"></a><span data-ttu-id="e6da3-103">Enumerar licenseDetails</span><span class="sxs-lookup"><span data-stu-id="e6da3-103">List licenseDetails</span></span>

<span data-ttu-id="e6da3-104">Recupera una lista de objetos licenseDetails.</span><span class="sxs-lookup"><span data-stu-id="e6da3-104">Retrieve a list of licenseDetails objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="e6da3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e6da3-105">Permissions</span></span>
<span data-ttu-id="e6da3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6da3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e6da3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6da3-108">Permission type</span></span>      | <span data-ttu-id="e6da3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6da3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e6da3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6da3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e6da3-111">User.Read, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e6da3-111">User.Read, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="e6da3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6da3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e6da3-113">User.Read</span><span class="sxs-lookup"><span data-stu-id="e6da3-113">User.Read</span></span>    |
|<span data-ttu-id="e6da3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6da3-114">Application</span></span> | <span data-ttu-id="e6da3-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6da3-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e6da3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6da3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/licenseDetails
GET /users/{id}/licenseDetails
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e6da3-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e6da3-117">Optional query parameters</span></span>
<span data-ttu-id="e6da3-118">Este método **no** admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters).</span><span class="sxs-lookup"><span data-stu-id="e6da3-118">This method does **not** support [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="e6da3-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6da3-119">Request headers</span></span>
| <span data-ttu-id="e6da3-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e6da3-120">Name</span></span>      |<span data-ttu-id="e6da3-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6da3-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="e6da3-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e6da3-122">Authorization</span></span>  | <span data-ttu-id="e6da3-123">&lt;código&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="e6da3-123">Bearer &lt;code&gt;</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6da3-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6da3-124">Request body</span></span>
<span data-ttu-id="e6da3-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e6da3-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e6da3-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6da3-126">Response</span></span>

<span data-ttu-id="e6da3-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [licenseDetails](../resources/licensedetails.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6da3-127">If successful, this method returns a `200 OK` response code and collection of [licenseDetails](../resources/licensedetails.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e6da3-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6da3-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e6da3-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6da3-129">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_licensedetails"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/licenseDetails
```
##### <a name="response"></a><span data-ttu-id="e6da3-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6da3-130">Response</span></span>
<span data-ttu-id="e6da3-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6da3-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.licenseDetails",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 389

{
  "value": [
    {
      "servicePlans": [
        {
          "servicePlanId": "servicePlanId-value",
          "servicePlanName": "servicePlanName-value",
          "provisioningStatus": "provisioningStatus-value",
          "appliesTo": "appliesTo-value"
        }
      ],
      "skuId": "skuId-value",
      "skuPartNumber": "skuPartNumber-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List licenseDetails",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
