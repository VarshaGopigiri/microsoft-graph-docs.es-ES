---
title: Obtener orgContact
description: Recuperar las propiedades y relaciones del objeto orgcontact.
localization_priority: Normal
ms.openlocfilehash: 4a806c48ef7fc9adc4a8eb94bc7c28e3add78d14
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842934"
---
# <a name="get-orgcontact"></a><span data-ttu-id="aaf8f-103">Obtener orgContact</span><span class="sxs-lookup"><span data-stu-id="aaf8f-103">Get orgContact</span></span>

> <span data-ttu-id="aaf8f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="aaf8f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="aaf8f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="aaf8f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="aaf8f-106">Recuperar las propiedades y relaciones del objeto orgcontact.</span><span class="sxs-lookup"><span data-stu-id="aaf8f-106">Retrieve the properties and relationships of orgcontact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="aaf8f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="aaf8f-107">Permissions</span></span>
<span data-ttu-id="aaf8f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aaf8f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aaf8f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aaf8f-110">Permission type</span></span>      | <span data-ttu-id="aaf8f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aaf8f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="aaf8f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aaf8f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="aaf8f-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="aaf8f-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="aaf8f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aaf8f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="aaf8f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aaf8f-115">Not supported.</span></span>    |
|<span data-ttu-id="aaf8f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aaf8f-116">Application</span></span> | <span data-ttu-id="aaf8f-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aaf8f-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="aaf8f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aaf8f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /contacts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="aaf8f-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="aaf8f-119">Optional query parameters</span></span>
<span data-ttu-id="aaf8f-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aaf8f-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="aaf8f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aaf8f-121">Request headers</span></span>
| <span data-ttu-id="aaf8f-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="aaf8f-122">Name</span></span>       | <span data-ttu-id="aaf8f-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="aaf8f-123">Type</span></span> | <span data-ttu-id="aaf8f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="aaf8f-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="aaf8f-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="aaf8f-125">Authorization</span></span>  | <span data-ttu-id="aaf8f-126">string</span><span class="sxs-lookup"><span data-stu-id="aaf8f-126">string</span></span>  | <span data-ttu-id="aaf8f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aaf8f-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="aaf8f-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aaf8f-129">Request body</span></span>
<span data-ttu-id="aaf8f-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="aaf8f-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="aaf8f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aaf8f-131">Response</span></span>

<span data-ttu-id="aaf8f-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [orgContact](../resources/orgcontact.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aaf8f-132">If successful, this method returns a `200 OK` response code and [orgContact](../resources/orgcontact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="aaf8f-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aaf8f-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="aaf8f-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aaf8f-134">Request</span></span>
<span data-ttu-id="aaf8f-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aaf8f-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_orgcontact"
}-->
```http
GET https://graph.microsoft.com/beta/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="aaf8f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aaf8f-136">Response</span></span>
<span data-ttu-id="aaf8f-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aaf8f-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
