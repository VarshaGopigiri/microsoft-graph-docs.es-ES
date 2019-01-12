---
title: List mailFolders
description: Obtenga todas las carpetas de correo en el buzón del usuario que ha iniciado sesión.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: cb2d9e50776d88676cd6c2fdde39d9de89a635c0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990302"
---
# <a name="list-mailfolders"></a><span data-ttu-id="6d365-103">List mailFolders</span><span class="sxs-lookup"><span data-stu-id="6d365-103">List mailFolders</span></span>

> <span data-ttu-id="6d365-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6d365-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6d365-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6d365-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6d365-106">Obtenga todas las carpetas de correo en el buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="6d365-106">Get all the mail folders in the signed-in user's mailbox.</span></span>

## <a name="permissions"></a><span data-ttu-id="6d365-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6d365-107">Permissions</span></span>
<span data-ttu-id="6d365-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6d365-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6d365-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d365-110">Permission type</span></span>      | <span data-ttu-id="6d365-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d365-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6d365-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d365-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6d365-113">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6d365-113">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6d365-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d365-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6d365-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6d365-115">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6d365-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d365-116">Application</span></span> | <span data-ttu-id="6d365-117">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6d365-117">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="6d365-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d365-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/mailFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6d365-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6d365-119">Optional query parameters</span></span>
<span data-ttu-id="6d365-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d365-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="6d365-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d365-121">Request headers</span></span>
| <span data-ttu-id="6d365-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d365-122">Header</span></span>       | <span data-ttu-id="6d365-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6d365-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6d365-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="6d365-124">Authorization</span></span>  | <span data-ttu-id="6d365-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d365-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="6d365-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6d365-127">Content-Type</span></span>   | <span data-ttu-id="6d365-128">application/json</span><span class="sxs-lookup"><span data-stu-id="6d365-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6d365-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d365-129">Request body</span></span>
<span data-ttu-id="6d365-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6d365-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6d365-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d365-131">Response</span></span>

<span data-ttu-id="6d365-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d365-132">If successful, this method returns a `200 OK` response code and collection of [MailFolder](../resources/mailfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6d365-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d365-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6d365-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d365-134">Request</span></span>
<span data-ttu-id="6d365-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d365-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailfolders"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailFolders
```
##### <a name="response"></a><span data-ttu-id="6d365-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d365-136">Response</span></span>
<span data-ttu-id="6d365-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6d365-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
