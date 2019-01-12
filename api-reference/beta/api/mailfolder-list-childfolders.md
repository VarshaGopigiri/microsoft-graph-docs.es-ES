---
title: List childFolders
description: 'Obtener la colección de la carpeta en la carpeta especificada. Puede usar el `.../me/MailFolders` acceso directo para obtener el nivel superior '
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: a6a3e5c4228371e91fcbe4dc4c1511b805b26388
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27942790"
---
# <a name="list-childfolders"></a><span data-ttu-id="2a999-104">List childFolders</span><span class="sxs-lookup"><span data-stu-id="2a999-104">List childFolders</span></span>

> <span data-ttu-id="2a999-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2a999-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2a999-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2a999-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2a999-p103">Obtiene la colección de carpetas en la carpeta especificada. Puede usar el acceso directo de `.../me/MailFolders` para obtener la colección de carpetas de nivel superior y navegar a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="2a999-p103">Get the folder collection under the specified folder. You can use the `.../me/MailFolders` shortcut to get the top-level folder collection and navigate to another folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="2a999-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="2a999-109">Permissions</span></span>
<span data-ttu-id="2a999-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2a999-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2a999-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2a999-112">Permission type</span></span>      | <span data-ttu-id="2a999-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2a999-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2a999-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2a999-114">Delegated (work or school account)</span></span> | <span data-ttu-id="2a999-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2a999-115">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="2a999-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2a999-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2a999-117">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2a999-117">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="2a999-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2a999-118">Application</span></span> | <span data-ttu-id="2a999-119">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2a999-119">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="2a999-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2a999-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/childFolders
GET /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

## <a name="optional-query-parameters"></a><span data-ttu-id="2a999-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2a999-121">Optional query parameters</span></span>
<span data-ttu-id="2a999-122">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a999-122">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2a999-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2a999-123">Request headers</span></span>
| <span data-ttu-id="2a999-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="2a999-124">Name</span></span>       | <span data-ttu-id="2a999-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a999-125">Type</span></span> | <span data-ttu-id="2a999-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a999-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2a999-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="2a999-127">Authorization</span></span>  | <span data-ttu-id="2a999-128">string</span><span class="sxs-lookup"><span data-stu-id="2a999-128">string</span></span>  | <span data-ttu-id="2a999-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a999-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2a999-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2a999-131">Request body</span></span>
<span data-ttu-id="2a999-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2a999-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2a999-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a999-133">Response</span></span>
<span data-ttu-id="2a999-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a999-134">If successful, this method returns a `200 OK` response code and collection of [MailFolder](../resources/mailfolder.md) objects in the response body.</span></span>

## <a name="example-1"></a><span data-ttu-id="2a999-135">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a999-135">Example 1</span></span>
#### <a name="request-1"></a><span data-ttu-id="2a999-136">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="2a999-136">Request 1</span></span>
<span data-ttu-id="2a999-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a999-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_childfolders"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailFolders/AAMkAGVmMDEzM/childFolders
```

#### <a name="response-1"></a><span data-ttu-id="2a999-138">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="2a999-138">Response 1</span></span>
<span data-ttu-id="2a999-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a999-139">The following is an example of the response.</span></span>
><span data-ttu-id="2a999-140">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2a999-140">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="2a999-141">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2a999-141">All the properties will be returned from an actual call.</span></span>

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
        "id": "AAMkAGVmMDEzA",
        "displayName": "Internal Screens",
        "parentFolderId": "AAMkAGVmMDEzM",
        "childFolderCount": 0,
        "unreadItemCount": 2,
        "totalItemCount": 2,
        "wellKnownName": null
    },
    {
        "id": "AAMkAGVmMDEzB",
        "displayName": "Project Falcon",
        "parentFolderId": "AAMkAGVmMDEzM",
        "childFolderCount": 0,
        "unreadItemCount": 5,
        "totalItemCount": 5,
        "wellKnownName": null
    },
    {
        "id": "AAMkAGVmMDEzMA",
        "displayName": "Finder",
        "parentFolderId": "AAMkAGVmMDEzM",
        "childFolderCount": 4,
        "unreadItemCount": 0,
        "totalItemCount": 0,
        "wellKnownName": "searchfolders"
    }
  ]
}
```

## <a name="example-2"></a><span data-ttu-id="2a999-142">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="2a999-142">Example 2</span></span>
#### <a name="request-2"></a><span data-ttu-id="2a999-143">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="2a999-143">Request 2</span></span>
<span data-ttu-id="2a999-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a999-144">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_childfolders_of_searchfolders"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailFolders/searchfolders/childFolders
```

#### <a name="response-2"></a><span data-ttu-id="2a999-145">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="2a999-145">Response 2</span></span>
<span data-ttu-id="2a999-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a999-146">The following is an example of the response.</span></span>
><span data-ttu-id="2a999-147">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2a999-147">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="2a999-148">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2a999-148">All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailSearchFolder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 232

{
  "value": [
    {
        "id": "AAMkAGVmMDEzA",
        "displayName": "Internal Screens",
        "parentFolderId": "AAMkAGVmMDEzM",
        "childFolderCount": 0,
        "unreadItemCount": 2,
        "totalItemCount": 2,
        "wellKnownName": null
    },
    {
        "id": "AAMkAGVmMDEzB",
        "displayName": "Project Falcon",
        "parentFolderId": "AAMkAGVmMDEzM",
        "childFolderCount": 0,
        "unreadItemCount": 5,
        "totalItemCount": 5,
        "wellKnownName": null
    },
    {
        "id": "AAMkAGVmMDEzMA",
        "displayName": "Finder",
        "parentFolderId": "AAMkAGVmMDEzM",
        "childFolderCount": 4,
        "unreadItemCount": 0,
        "totalItemCount": 0,
        "wellKnownName": "searchfolders"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List childFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
