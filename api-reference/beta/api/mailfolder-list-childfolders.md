---
title: List childFolders
description: 'Obtener la colección de la carpeta en la carpeta especificada. Puede usar el `.../me/MailFolders` acceso directo para obtener el nivel superior '
ms.openlocfilehash: 826ce59f0f808ee94107a41e76207e83632361ff
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087885"
---
# <a name="list-childfolders"></a><span data-ttu-id="ea6d7-104">List childFolders</span><span class="sxs-lookup"><span data-stu-id="ea6d7-104">List childFolders</span></span>

> <span data-ttu-id="ea6d7-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ea6d7-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ea6d7-p103">Obtiene la colección de carpetas en la carpeta especificada. Puede usar el acceso directo de `.../me/MailFolders` para obtener la colección de carpetas de nivel superior y navegar a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-p103">Get the folder collection under the specified folder. You can use the `.../me/MailFolders` shortcut to get the top-level folder collection and navigate to another folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="ea6d7-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="ea6d7-109">Permissions</span></span>
<span data-ttu-id="ea6d7-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea6d7-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ea6d7-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea6d7-112">Permission type</span></span>      | <span data-ttu-id="ea6d7-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea6d7-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ea6d7-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea6d7-114">Delegated (work or school account)</span></span> | <span data-ttu-id="ea6d7-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea6d7-115">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ea6d7-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea6d7-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ea6d7-117">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea6d7-117">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ea6d7-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea6d7-118">Application</span></span> | <span data-ttu-id="ea6d7-119">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea6d7-119">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ea6d7-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea6d7-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/childFolders
GET /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ea6d7-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ea6d7-121">Optional query parameters</span></span>
<span data-ttu-id="ea6d7-122">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-122">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ea6d7-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea6d7-123">Request headers</span></span>
| <span data-ttu-id="ea6d7-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="ea6d7-124">Name</span></span>       | <span data-ttu-id="ea6d7-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea6d7-125">Type</span></span> | <span data-ttu-id="ea6d7-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea6d7-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ea6d7-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea6d7-127">Authorization</span></span>  | <span data-ttu-id="ea6d7-128">string</span><span class="sxs-lookup"><span data-stu-id="ea6d7-128">string</span></span>  | <span data-ttu-id="ea6d7-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ea6d7-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea6d7-131">Request body</span></span>
<span data-ttu-id="ea6d7-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ea6d7-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea6d7-133">Response</span></span>
<span data-ttu-id="ea6d7-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-134">If successful, this method returns a `200 OK` response code and collection of [MailFolder](../resources/mailfolder.md) objects in the response body.</span></span>

## <a name="example-1"></a><span data-ttu-id="ea6d7-135">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea6d7-135">Example 1</span></span>
#### <a name="request-1"></a><span data-ttu-id="ea6d7-136">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="ea6d7-136">Request 1</span></span>
<span data-ttu-id="ea6d7-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_childfolders"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailFolders/AAMkAGVmMDEzM/childFolders
```

#### <a name="response-1"></a><span data-ttu-id="ea6d7-138">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="ea6d7-138">Response 1</span></span>
<span data-ttu-id="ea6d7-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-139">The following is an example of the response.</span></span>
><span data-ttu-id="ea6d7-140">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-140">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="ea6d7-141">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-141">All the properties will be returned from an actual call.</span></span>

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

## <a name="example-2"></a><span data-ttu-id="ea6d7-142">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea6d7-142">Example 2</span></span>
#### <a name="request-2"></a><span data-ttu-id="ea6d7-143">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="ea6d7-143">Request 2</span></span>
<span data-ttu-id="ea6d7-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-144">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_childfolders_of_searchfolders"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailFolders/searchfolders/childFolders
```

#### <a name="response-2"></a><span data-ttu-id="ea6d7-145">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="ea6d7-145">Response 2</span></span>
<span data-ttu-id="ea6d7-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-146">The following is an example of the response.</span></span>
><span data-ttu-id="ea6d7-147">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-147">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="ea6d7-148">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-148">All the properties will be returned from an actual call.</span></span>

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
