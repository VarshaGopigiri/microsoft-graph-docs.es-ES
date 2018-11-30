---
title: Lista agreementAcceptances
description: Recuperar una lista de objetos de agreementAcceptance de un usuario.
ms.openlocfilehash: 77e10ff9e35db37247f91f4c473c1775c295033a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090287"
---
# <a name="list-agreementacceptances"></a><span data-ttu-id="46133-103">Lista agreementAcceptances</span><span class="sxs-lookup"><span data-stu-id="46133-103">List agreementAcceptances</span></span>

> <span data-ttu-id="46133-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46133-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46133-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46133-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="46133-106">Recuperar una lista de objetos de [agreementAcceptance](../resources/agreementacceptance.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="46133-106">Retrieve a list of a user's [agreementAcceptance](../resources/agreementacceptance.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="46133-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="46133-107">Permissions</span></span>
<span data-ttu-id="46133-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="46133-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="46133-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="46133-110">Permission type</span></span>                        | <span data-ttu-id="46133-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="46133-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="46133-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="46133-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="46133-113">AgreementAcceptance.Read</span><span class="sxs-lookup"><span data-stu-id="46133-113">AgreementAcceptance.Read</span></span> |
|<span data-ttu-id="46133-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="46133-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="46133-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46133-115">Not supported.</span></span> |
|<span data-ttu-id="46133-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="46133-116">Application</span></span>                            | <span data-ttu-id="46133-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46133-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="46133-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="46133-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/agreementAcceptances
```
<!--
## Optional query parameters
This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.
-->

## <a name="request-headers"></a><span data-ttu-id="46133-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="46133-119">Request headers</span></span>
| <span data-ttu-id="46133-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="46133-120">Name</span></span>      |<span data-ttu-id="46133-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="46133-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="46133-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="46133-122">Authorization</span></span> | <span data-ttu-id="46133-123">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="46133-123">Bearer {token}</span></span> |

## <a name="request-body"></a><span data-ttu-id="46133-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="46133-124">Request body</span></span>
<span data-ttu-id="46133-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="46133-125">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="46133-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46133-126">Response</span></span>
<span data-ttu-id="46133-127">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [agreementAcceptance](../resources/agreementacceptance.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46133-127">If successful, this method returns a `200 OK` response code and a collection of [agreementAcceptance](../resources/agreementacceptance.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="46133-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46133-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="46133-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="46133-129">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_agreementacceptances"
}-->
```http
GET https://graph.microsoft.com/beta/me/agreementAcceptances
```
##### <a name="response"></a><span data-ttu-id="46133-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46133-130">Response</span></span>
><span data-ttu-id="46133-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="46133-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.agreementAcceptance",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 303

{
  "value": [
    {
      "agreementId": "agreementId-value",
      "userId": "userId-value",
      "agreementFileId": "agreementFileId-value",
      "recordedDateTime": "datetime-value",
      "userDisplayName": "userDisplayName-value",
      "userPrincipalName": "userPrincipalName-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List agreementAcceptances",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->