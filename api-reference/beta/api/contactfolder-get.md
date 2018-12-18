---
title: Get contactFolder
description: Obtiene una carpeta de contactos mediante el id. de carpeta de contactos.
author: angelgolfer-ms
ms.openlocfilehash: 7a51194f93bc7daf23fb0a0555e4e69425c7387b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358978"
---
# <a name="get-contactfolder"></a><span data-ttu-id="7c39e-103">Get contactFolder</span><span class="sxs-lookup"><span data-stu-id="7c39e-103">Get contactFolder</span></span>

> <span data-ttu-id="7c39e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c39e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c39e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c39e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7c39e-106">Obtiene una carpeta de contactos mediante el id. de carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="7c39e-106">Get a contact folder by using the contact folder ID.</span></span>

<span data-ttu-id="7c39e-107">Hay dos escenarios donde una aplicación puede obtener la carpeta de contactos de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="7c39e-107">There are two scenarios where an app can get another user's contact folder:</span></span>

* <span data-ttu-id="7c39e-108">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="7c39e-108">If the app has application permissions, or,</span></span>
* <span data-ttu-id="7c39e-109">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de contactos con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="7c39e-109">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a contact folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="7c39e-110">Consulte los [Detalles y un ejemplo](/graph/outlook-get-shared-contacts-folders).</span><span class="sxs-lookup"><span data-stu-id="7c39e-110">See [details and an example](/graph/outlook-get-shared-contacts-folders).</span></span>


## <a name="permissions"></a><span data-ttu-id="7c39e-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="7c39e-111">Permissions</span></span>
<span data-ttu-id="7c39e-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7c39e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7c39e-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7c39e-114">Permission type</span></span>      | <span data-ttu-id="7c39e-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7c39e-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7c39e-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7c39e-116">Delegated (work or school account)</span></span> | <span data-ttu-id="7c39e-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7c39e-117">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="7c39e-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7c39e-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7c39e-119">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7c39e-119">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="7c39e-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7c39e-120">Application</span></span> | <span data-ttu-id="7c39e-121">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7c39e-121">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="7c39e-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7c39e-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactFolders/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7c39e-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7c39e-123">Optional query parameters</span></span>
<span data-ttu-id="7c39e-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c39e-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7c39e-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7c39e-125">Request headers</span></span>
| <span data-ttu-id="7c39e-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="7c39e-126">Name</span></span>       | <span data-ttu-id="7c39e-127">Type</span><span class="sxs-lookup"><span data-stu-id="7c39e-127">Type</span></span> | <span data-ttu-id="7c39e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c39e-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7c39e-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="7c39e-129">Authorization</span></span>  | <span data-ttu-id="7c39e-130">string</span><span class="sxs-lookup"><span data-stu-id="7c39e-130">string</span></span>  | <span data-ttu-id="7c39e-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c39e-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7c39e-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7c39e-133">Request body</span></span>
<span data-ttu-id="7c39e-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7c39e-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7c39e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c39e-135">Response</span></span>

<span data-ttu-id="7c39e-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c39e-136">If successful, this method returns a `200 OK` response code and [contactFolder](../resources/contactfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7c39e-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c39e-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7c39e-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7c39e-138">Request</span></span>
<span data-ttu-id="7c39e-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7c39e-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contactfolder"
}-->
```http
GET https://graph.microsoft.com/beta/me/contactFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="7c39e-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c39e-140">Response</span></span>
<span data-ttu-id="7c39e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7c39e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 104

{
  "displayName": "Finance",
  "id": "AAMkAGI2TKI5AAA=",
  "parentFolderId": "AAMkAGI2AAEOAAA=",
  "wellKnownName": null
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get contactFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
