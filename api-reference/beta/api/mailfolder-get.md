---
title: Get mailFolder
description: Recupere las propiedades y las relaciones de un objeto de carpeta de mensajes.
ms.openlocfilehash: 669ebca608d5df6532ee2f1b10a4217eecfb60d1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085479"
---
# <a name="get-mailfolder"></a><span data-ttu-id="328b4-103">Get mailFolder</span><span class="sxs-lookup"><span data-stu-id="328b4-103">Get mailFolder</span></span>

> <span data-ttu-id="328b4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="328b4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="328b4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="328b4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="328b4-106">Recupere las propiedades y las relaciones de un objeto de carpeta de mensajes.</span><span class="sxs-lookup"><span data-stu-id="328b4-106">Retrieve the properties and relationships of a message folder object.</span></span>

<span data-ttu-id="328b4-107">Hay dos escenarios donde una aplicación puede obtener la carpeta de correo de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="328b4-107">There are two scenarios where an app can get another user's mail folder:</span></span>

* <span data-ttu-id="328b4-108">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="328b4-108">If the app has application permissions, or,</span></span>
* <span data-ttu-id="328b4-109">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de correo con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="328b4-109">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a mail folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="328b4-110">Consulte los [Detalles y un ejemplo](/graph/outlook-share-messages-folders).</span><span class="sxs-lookup"><span data-stu-id="328b4-110">See [details and an example](/graph/outlook-share-messages-folders).</span></span>


## <a name="permissions"></a><span data-ttu-id="328b4-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="328b4-111">Permissions</span></span>
<span data-ttu-id="328b4-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="328b4-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="328b4-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="328b4-114">Permission type</span></span>      | <span data-ttu-id="328b4-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="328b4-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="328b4-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="328b4-116">Delegated (work or school account)</span></span> | <span data-ttu-id="328b4-117">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="328b4-117">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="328b4-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="328b4-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="328b4-119">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="328b4-119">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="328b4-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="328b4-120">Application</span></span> | <span data-ttu-id="328b4-121">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="328b4-121">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="328b4-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="328b4-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="328b4-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="328b4-123">Optional query parameters</span></span>
<span data-ttu-id="328b4-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="328b4-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="328b4-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="328b4-125">Request headers</span></span>
| <span data-ttu-id="328b4-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="328b4-126">Name</span></span>       | <span data-ttu-id="328b4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="328b4-127">Type</span></span> | <span data-ttu-id="328b4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="328b4-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="328b4-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="328b4-129">Authorization</span></span>  | <span data-ttu-id="328b4-130">string</span><span class="sxs-lookup"><span data-stu-id="328b4-130">string</span></span>  | <span data-ttu-id="328b4-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="328b4-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="328b4-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="328b4-133">Request body</span></span>
<span data-ttu-id="328b4-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="328b4-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="328b4-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="328b4-135">Response</span></span>
<span data-ttu-id="328b4-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="328b4-136">If successful, this method returns a `200 OK` response code and [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example-1"></a><span data-ttu-id="328b4-137">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="328b4-137">Example 1</span></span>
#### <a name="request-1"></a><span data-ttu-id="328b4-138">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="328b4-138">Request 1</span></span>
<span data-ttu-id="328b4-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="328b4-139">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailfolder"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailFolders/AAMkAGVmMDEzM
```

#### <a name="response-1"></a><span data-ttu-id="328b4-140">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="328b4-140">Response 1</span></span>
<span data-ttu-id="328b4-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="328b4-141">The following is an example of the response.</span></span>
 ><span data-ttu-id="328b4-142">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="328b4-142">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="328b4-143">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="328b4-143">All the properties will be returned from an actual call.</span></span>
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
    "id": "AAMkAGVmMDEzM",
    "displayName": "Inbox",
    "parentFolderId": "AAMkAGVmMDEzI",
    "childFolderCount": 2,
    "unreadItemCount": 59,
    "totalItemCount": 60,
    "wellKnownName": "inbox"
}
```

## <a name="example-2"></a><span data-ttu-id="328b4-144">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="328b4-144">Example 2</span></span>
#### <a name="request-2"></a><span data-ttu-id="328b4-145">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="328b4-145">Request 2</span></span>
<span data-ttu-id="328b4-146">El siguiente es un ejemplo de la carpeta de búsqueda de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="328b4-146">The following is a search folder example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailSearchfolder"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailFolders/AAMkAGVmMDEzM
```

#### <a name="response-2"></a><span data-ttu-id="328b4-147">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="328b4-147">Response 2</span></span>
<span data-ttu-id="328b4-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="328b4-148">The following is an example of the response.</span></span>
 ><span data-ttu-id="328b4-149">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="328b4-149">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="328b4-150">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="328b4-150">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailSearchFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
    "id": "AAMkAGVmMDEzM",
    "displayName": "Inbox",
    "parentFolderId": "AAMkAGVmMDEzI",
    "childFolderCount": 2,
    "unreadItemCount": 59,
    "totalItemCount": 60,
    "wellKnownName": "inbox"
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
