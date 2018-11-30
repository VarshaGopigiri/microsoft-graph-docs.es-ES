---
title: List mailFolders
description: 'Obtiene la colección de carpetas de correo en la carpeta raíz del usuario que inició sesión. '
ms.openlocfilehash: 92143ab874ce724e72de6cae18593d0d652fd8d6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028823"
---
# <a name="list-mailfolders"></a><span data-ttu-id="86e72-103">List mailFolders</span><span class="sxs-lookup"><span data-stu-id="86e72-103">List mailFolders</span></span>

<span data-ttu-id="86e72-104">Obtiene la colección de carpetas de correo en la carpeta raíz del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="86e72-104">Get the mail folder collection under the root folder of the signed-in user.</span></span> 
## <a name="permissions"></a><span data-ttu-id="86e72-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="86e72-105">Permissions</span></span>
<span data-ttu-id="86e72-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="86e72-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="86e72-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="86e72-108">Permission type</span></span>      | <span data-ttu-id="86e72-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="86e72-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="86e72-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="86e72-110">Delegated (work or school account)</span></span> | <span data-ttu-id="86e72-111">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="86e72-111">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="86e72-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="86e72-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="86e72-113">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="86e72-113">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="86e72-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="86e72-114">Application</span></span> | <span data-ttu-id="86e72-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="86e72-115">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="86e72-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86e72-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/mailFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="86e72-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="86e72-117">Optional query parameters</span></span>
<span data-ttu-id="86e72-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86e72-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="86e72-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="86e72-119">Request headers</span></span>
| <span data-ttu-id="86e72-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86e72-120">Header</span></span>       | <span data-ttu-id="86e72-121">Valor</span><span class="sxs-lookup"><span data-stu-id="86e72-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="86e72-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="86e72-122">Authorization</span></span>  | <span data-ttu-id="86e72-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="86e72-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="86e72-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="86e72-125">Content-Type</span></span>   | <span data-ttu-id="86e72-126">application/json</span><span class="sxs-lookup"><span data-stu-id="86e72-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="86e72-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="86e72-127">Request body</span></span>
<span data-ttu-id="86e72-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="86e72-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="86e72-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86e72-129">Response</span></span>

<span data-ttu-id="86e72-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86e72-130">If successful, this method returns a `200 OK` response code and collection of [MailFolder](../resources/mailfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="86e72-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86e72-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="86e72-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="86e72-132">Request</span></span>
<span data-ttu-id="86e72-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="86e72-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailfolders"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders
```
##### <a name="response"></a><span data-ttu-id="86e72-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86e72-134">Response</span></span>
<span data-ttu-id="86e72-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="86e72-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
