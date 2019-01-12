---
title: Enumerar licenseDetails
description: Recupera una lista de objetos licenseDetails.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 80b2e707ec6106def7d8539dcf5e8e9a20179503
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991898"
---
# <a name="list-licensedetails"></a><span data-ttu-id="4d005-103">Enumerar licenseDetails</span><span class="sxs-lookup"><span data-stu-id="4d005-103">List licenseDetails</span></span>

> <span data-ttu-id="4d005-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4d005-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4d005-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4d005-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4d005-106">Recupera una lista de objetos licenseDetails.</span><span class="sxs-lookup"><span data-stu-id="4d005-106">Retrieve a list of licenseDetails objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="4d005-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4d005-107">Permissions</span></span>
<span data-ttu-id="4d005-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4d005-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4d005-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d005-110">Permission type</span></span>      | <span data-ttu-id="4d005-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d005-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4d005-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d005-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4d005-113">User.Read, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4d005-113">User.Read, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4d005-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d005-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4d005-115">User.Read</span><span class="sxs-lookup"><span data-stu-id="4d005-115">User.Read</span></span>    |
|<span data-ttu-id="4d005-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d005-116">Application</span></span> | <span data-ttu-id="4d005-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4d005-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4d005-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d005-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/licenseDetails
GET /users/{id}/licenseDetails
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4d005-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4d005-119">Optional query parameters</span></span>
<span data-ttu-id="4d005-120">Este método **no** admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters).</span><span class="sxs-lookup"><span data-stu-id="4d005-120">This method does **not** support [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="4d005-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d005-121">Request headers</span></span>
| <span data-ttu-id="4d005-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d005-122">Name</span></span>      |<span data-ttu-id="4d005-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d005-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="4d005-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d005-124">Authorization</span></span>  | <span data-ttu-id="4d005-125">&lt;código&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="4d005-125">Bearer &lt;code&gt;</span></span>|

## <a name="request-body"></a><span data-ttu-id="4d005-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d005-126">Request body</span></span>
<span data-ttu-id="4d005-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4d005-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4d005-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d005-128">Response</span></span>

<span data-ttu-id="4d005-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [licenseDetails](../resources/licensedetails.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d005-129">If successful, this method returns a `200 OK` response code and collection of [licenseDetails](../resources/licensedetails.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4d005-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d005-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4d005-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d005-131">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_licensedetails"
}-->
```http
GET https://graph.microsoft.com/beta/me/licenseDetails
```
##### <a name="response"></a><span data-ttu-id="4d005-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d005-132">Response</span></span>
<span data-ttu-id="4d005-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4d005-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
