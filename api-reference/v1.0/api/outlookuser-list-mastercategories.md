---
title: Enumerar categorías de Outlook
description: Obtener todas las categorías que han sido definidas por el usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 4fd401d2556d805afc35fd906d74b9ddc71423c6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911948"
---
# <a name="list-outlook-categories"></a><span data-ttu-id="63083-103">Enumerar categorías de Outlook</span><span class="sxs-lookup"><span data-stu-id="63083-103">List Outlook categories</span></span>


<span data-ttu-id="63083-104">Obtener todas las categorías que han sido definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="63083-104">Get all the categories that have been defined for the user.</span></span>

## <a name="permissions"></a><span data-ttu-id="63083-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="63083-105">Permissions</span></span>
<span data-ttu-id="63083-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63083-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63083-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63083-108">Permission type</span></span>      | <span data-ttu-id="63083-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63083-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="63083-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63083-110">Delegated (work or school account)</span></span> | <span data-ttu-id="63083-111">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="63083-111">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="63083-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63083-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="63083-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="63083-113">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="63083-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63083-114">Application</span></span> | <span data-ttu-id="63083-115">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="63083-115">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="63083-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63083-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/masterCategories
GET /users/{id|userPrincipalName}/outlook/masterCategories
```
## <a name="optional-query-parameters"></a><span data-ttu-id="63083-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="63083-117">Optional query parameters</span></span>
<span data-ttu-id="63083-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63083-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="63083-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63083-119">Request headers</span></span>
| <span data-ttu-id="63083-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="63083-120">Name</span></span>      |<span data-ttu-id="63083-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="63083-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="63083-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="63083-122">Authorization</span></span>  | <span data-ttu-id="63083-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="63083-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="63083-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63083-125">Request body</span></span>
<span data-ttu-id="63083-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="63083-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="63083-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63083-127">Response</span></span>

<span data-ttu-id="63083-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [outlookCategory](../resources/outlookcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63083-128">If successful, this method returns a `200 OK` response code and collection of [outlookCategory](../resources/outlookcategory.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="63083-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63083-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="63083-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63083-130">Request</span></span>
<span data-ttu-id="63083-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63083-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mastercategories"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/outlook/masterCategories
```
##### <a name="response"></a><span data-ttu-id="63083-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63083-132">Response</span></span>
<span data-ttu-id="63083-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63083-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookCategory",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 727

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories",
  "value":[
    {
      "id":"5a9a6aa8-b65f-4357-b1f9-60c6bf6330d8",
      "displayName":"Red category",
      "color":"preset0"
    },
    {
      "id":"4b1c2495-54c9-4a5e-90a2-0ab0b31987d8",
      "displayName":"Orange category",
      "color":"preset1"
    },
    {
      "id":"de912e4d-c790-4da9-949c-ccd933aaa0f7",
      "displayName":"Yellow category",
      "color":"preset3"
    },
    {
      "id":"79c8d8f8-9db1-49ec-99ce-ae25793e7232",
      "displayName":"Green category",
      "color":"preset4"
    },
    {
      "id":"626e696c-6a10-48b8-89b9-12de3160cfb9",
      "displayName":"Blue category",
      "color":"preset7"
    },
    {
      "id":"453d06d0-447d-41f7-91cd-aa0f6b190b5b",
      "displayName":"Purple category",
      "color":"preset8"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List categories",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
