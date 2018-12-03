---
title: Get mailFolder
description: Recupere las propiedades y las relaciones de un objeto de carpeta de mensajes.
ms.openlocfilehash: 394fe948b67dbfded176eff27aaa6222856e69ee
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032079"
---
# <a name="get-mailfolder"></a><span data-ttu-id="79ae2-103">Get mailFolder</span><span class="sxs-lookup"><span data-stu-id="79ae2-103">Get mailFolder</span></span>

<span data-ttu-id="79ae2-104">Recupere las propiedades y las relaciones de un objeto de carpeta de mensajes.</span><span class="sxs-lookup"><span data-stu-id="79ae2-104">Retrieve the properties and relationships of a message folder object.</span></span>

<span data-ttu-id="79ae2-105">Hay dos escenarios donde una aplicación puede obtener la carpeta de correo de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="79ae2-105">There are two scenarios where an app can get another user's mail folder:</span></span>

* <span data-ttu-id="79ae2-106">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="79ae2-106">If the app has application permissions, or,</span></span>
* <span data-ttu-id="79ae2-107">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de correo con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="79ae2-107">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a mail folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="79ae2-108">Consulte los [Detalles y un ejemplo](/graph/outlook-share-messages-folders).</span><span class="sxs-lookup"><span data-stu-id="79ae2-108">See [details and an example](/graph/outlook-share-messages-folders).</span></span>


## <a name="permissions"></a><span data-ttu-id="79ae2-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="79ae2-109">Permissions</span></span>
<span data-ttu-id="79ae2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="79ae2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="79ae2-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79ae2-112">Permission type</span></span>      | <span data-ttu-id="79ae2-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79ae2-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="79ae2-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79ae2-114">Delegated (work or school account)</span></span> | <span data-ttu-id="79ae2-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="79ae2-115">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="79ae2-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79ae2-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="79ae2-117">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="79ae2-117">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="79ae2-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79ae2-118">Application</span></span> | <span data-ttu-id="79ae2-119">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="79ae2-119">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="79ae2-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79ae2-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="79ae2-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="79ae2-121">Optional query parameters</span></span>
<span data-ttu-id="79ae2-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79ae2-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="79ae2-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79ae2-123">Request headers</span></span>
| <span data-ttu-id="79ae2-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="79ae2-124">Name</span></span>       | <span data-ttu-id="79ae2-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="79ae2-125">Type</span></span> | <span data-ttu-id="79ae2-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="79ae2-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="79ae2-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="79ae2-127">Authorization</span></span>  | <span data-ttu-id="79ae2-128">string</span><span class="sxs-lookup"><span data-stu-id="79ae2-128">string</span></span>  | <span data-ttu-id="79ae2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79ae2-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="79ae2-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79ae2-131">Request body</span></span>
<span data-ttu-id="79ae2-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="79ae2-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="79ae2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79ae2-133">Response</span></span>

<span data-ttu-id="79ae2-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79ae2-134">If successful, this method returns a `200 OK` response code and [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="79ae2-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79ae2-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="79ae2-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79ae2-136">Request</span></span>
<span data-ttu-id="79ae2-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79ae2-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailfolder"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="79ae2-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79ae2-138">Response</span></span>
<span data-ttu-id="79ae2-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="79ae2-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get mailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->