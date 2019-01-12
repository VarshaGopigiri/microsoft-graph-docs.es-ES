---
title: Lista orgContacts
description: Recuperar la lista de contactos organizativas para esta organización.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 53cfa75edeb1994cabc1f363dab79455b90ce921
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915077"
---
# <a name="list-orgcontacts"></a><span data-ttu-id="ad16d-103">Lista orgContacts</span><span class="sxs-lookup"><span data-stu-id="ad16d-103">List orgContacts</span></span>

> <span data-ttu-id="ad16d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ad16d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ad16d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ad16d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ad16d-106">Recuperar la lista de contactos organizativas para esta organización.</span><span class="sxs-lookup"><span data-stu-id="ad16d-106">Retrieve the list of organizational contacts for this organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="ad16d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ad16d-107">Permissions</span></span>
<span data-ttu-id="ad16d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ad16d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ad16d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad16d-110">Permission type</span></span>      | <span data-ttu-id="ad16d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad16d-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ad16d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad16d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ad16d-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ad16d-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ad16d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad16d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ad16d-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad16d-115">Not supported.</span></span>    |
|<span data-ttu-id="ad16d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad16d-116">Application</span></span> | <span data-ttu-id="ad16d-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ad16d-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ad16d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad16d-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ad16d-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ad16d-119">Optional query parameters</span></span>
<span data-ttu-id="ad16d-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad16d-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ad16d-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad16d-121">Request headers</span></span>
| <span data-ttu-id="ad16d-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="ad16d-122">Name</span></span>       | <span data-ttu-id="ad16d-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad16d-123">Type</span></span> | <span data-ttu-id="ad16d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad16d-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ad16d-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="ad16d-125">Authorization</span></span>  | <span data-ttu-id="ad16d-126">string</span><span class="sxs-lookup"><span data-stu-id="ad16d-126">string</span></span>  | <span data-ttu-id="ad16d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ad16d-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ad16d-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad16d-129">Request body</span></span>
<span data-ttu-id="ad16d-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ad16d-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ad16d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad16d-131">Response</span></span>

<span data-ttu-id="ad16d-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [orgContact](../resources/orgcontact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad16d-132">If successful, this method returns a `200 OK` response code and a collection of [orgContact](../resources/orgcontact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ad16d-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad16d-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ad16d-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad16d-134">Request</span></span>
<span data-ttu-id="ad16d-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad16d-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "list_orgcontact"
}-->
```http
GET https://graph.microsoft.com/beta/contacts
```
##### <a name="response"></a><span data-ttu-id="ad16d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad16d-136">Response</span></span>
<span data-ttu-id="ad16d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ad16d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.orgcontact",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 222

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List orgContact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
