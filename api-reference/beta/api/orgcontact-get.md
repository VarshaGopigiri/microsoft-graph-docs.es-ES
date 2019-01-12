---
title: Obtener orgContact
description: Recuperar las propiedades y relaciones del objeto orgcontact.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 28d00c81a24eca077fcdecbbdbb233ba75eadc29
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928216"
---
# <a name="get-orgcontact"></a><span data-ttu-id="25c75-103">Obtener orgContact</span><span class="sxs-lookup"><span data-stu-id="25c75-103">Get orgContact</span></span>

> <span data-ttu-id="25c75-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="25c75-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="25c75-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="25c75-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="25c75-106">Recuperar las propiedades y relaciones del objeto orgcontact.</span><span class="sxs-lookup"><span data-stu-id="25c75-106">Retrieve the properties and relationships of orgcontact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="25c75-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="25c75-107">Permissions</span></span>
<span data-ttu-id="25c75-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="25c75-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="25c75-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="25c75-110">Permission type</span></span>      | <span data-ttu-id="25c75-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="25c75-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="25c75-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="25c75-112">Delegated (work or school account)</span></span> | <span data-ttu-id="25c75-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="25c75-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="25c75-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="25c75-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="25c75-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25c75-115">Not supported.</span></span>    |
|<span data-ttu-id="25c75-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="25c75-116">Application</span></span> | <span data-ttu-id="25c75-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="25c75-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="25c75-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="25c75-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /contacts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="25c75-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="25c75-119">Optional query parameters</span></span>
<span data-ttu-id="25c75-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25c75-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="25c75-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="25c75-121">Request headers</span></span>
| <span data-ttu-id="25c75-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="25c75-122">Name</span></span>       | <span data-ttu-id="25c75-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="25c75-123">Type</span></span> | <span data-ttu-id="25c75-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="25c75-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="25c75-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="25c75-125">Authorization</span></span>  | <span data-ttu-id="25c75-126">string</span><span class="sxs-lookup"><span data-stu-id="25c75-126">string</span></span>  | <span data-ttu-id="25c75-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="25c75-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="25c75-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="25c75-129">Request body</span></span>
<span data-ttu-id="25c75-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="25c75-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="25c75-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25c75-131">Response</span></span>

<span data-ttu-id="25c75-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [orgContact](../resources/orgcontact.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25c75-132">If successful, this method returns a `200 OK` response code and [orgContact](../resources/orgcontact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="25c75-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25c75-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="25c75-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="25c75-134">Request</span></span>
<span data-ttu-id="25c75-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25c75-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_orgcontact"
}-->
```http
GET https://graph.microsoft.com/beta/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="25c75-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25c75-136">Response</span></span>
<span data-ttu-id="25c75-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="25c75-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.orgcontact"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 222

{
  "addresses":[
      {
        "city": "string",
        "countryOrRegion": "string",
        "officeLocation": "string",
        "postalCode": "string",
        "state": "string",
        "street": "string"
      }
  ],
  "companyName": "companyName-value",
  "department": "department-value",
  "displayName": "displayName-value",
  "phones":[
      {
        "type": "string",
        "number": "string"
      }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get orgContact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
