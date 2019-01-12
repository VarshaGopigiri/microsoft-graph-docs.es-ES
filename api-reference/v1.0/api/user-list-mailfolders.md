---
title: List mailFolders
description: 'Obtiene la colección de carpetas de correo en la carpeta raíz del usuario que inició sesión. '
author: dkershaw10
localization_priority: Priority
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 8515e70ed9502c97706f8eab332c85c748384082
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972764"
---
# <a name="list-mailfolders"></a><span data-ttu-id="fb548-103">List mailFolders</span><span class="sxs-lookup"><span data-stu-id="fb548-103">List mailFolders</span></span>

<span data-ttu-id="fb548-104">Obtiene la colección de carpetas de correo en la carpeta raíz del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="fb548-104">Get the mail folder collection under the root folder of the signed-in user.</span></span> 
## <a name="permissions"></a><span data-ttu-id="fb548-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="fb548-105">Permissions</span></span>
<span data-ttu-id="fb548-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fb548-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fb548-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb548-108">Permission type</span></span>      | <span data-ttu-id="fb548-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb548-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fb548-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb548-110">Delegated (work or school account)</span></span> | <span data-ttu-id="fb548-111">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb548-111">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="fb548-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb548-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fb548-113">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb548-113">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="fb548-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb548-114">Application</span></span> | <span data-ttu-id="fb548-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb548-115">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="fb548-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb548-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/mailFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="fb548-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fb548-117">Optional query parameters</span></span>
<span data-ttu-id="fb548-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb548-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="fb548-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb548-119">Request headers</span></span>
| <span data-ttu-id="fb548-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb548-120">Header</span></span>       | <span data-ttu-id="fb548-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fb548-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="fb548-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="fb548-122">Authorization</span></span>  | <span data-ttu-id="fb548-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fb548-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="fb548-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fb548-125">Content-Type</span></span>   | <span data-ttu-id="fb548-126">application/json</span><span class="sxs-lookup"><span data-stu-id="fb548-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="fb548-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fb548-127">Request body</span></span>
<span data-ttu-id="fb548-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fb548-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fb548-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb548-129">Response</span></span>

<span data-ttu-id="fb548-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb548-130">If successful, this method returns a `200 OK` response code and collection of [MailFolder](../resources/mailfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fb548-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb548-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fb548-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb548-132">Request</span></span>
<span data-ttu-id="fb548-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb548-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailfolders"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders
```
##### <a name="response"></a><span data-ttu-id="fb548-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb548-134">Response</span></span>
<span data-ttu-id="fb548-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fb548-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 232

{
  "value": [
    {
      "displayName": "displayName-value",
      "parentFolderId": "parentFolderId-value",
      "childFolderCount": 99,
      "unreadItemCount": 99,
      "totalItemCount": 99,
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List mailFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
