---
title: List childFolders
description: 'Obtener la colección de la carpeta en la carpeta especificada. Puede usar el `.../me/MailFolders` acceso directo para obtener el nivel superior '
author: angelgolfer-ms
localization_priority: Priority
ms.prod: outlook
ms.openlocfilehash: 3fec593d1d1b29e84f43e46d4bee7ef8f4aa61d7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935405"
---
# <a name="list-childfolders"></a><span data-ttu-id="ea1ed-104">List childFolders</span><span class="sxs-lookup"><span data-stu-id="ea1ed-104">List childFolders</span></span>

<span data-ttu-id="ea1ed-p102">Obtiene la colección de carpetas en la carpeta especificada. Puede usar el acceso directo de `.../me/MailFolders` para obtener la colección de carpetas de nivel superior y navegar a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-p102">Get the folder collection under the specified folder. You can use the `.../me/MailFolders` shortcut to get the top-level folder collection and navigate to another folder.</span></span>
## <a name="permissions"></a><span data-ttu-id="ea1ed-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ea1ed-107">Permissions</span></span>
<span data-ttu-id="ea1ed-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea1ed-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ea1ed-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea1ed-110">Permission type</span></span>      | <span data-ttu-id="ea1ed-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea1ed-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ea1ed-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea1ed-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ea1ed-113">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea1ed-113">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ea1ed-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea1ed-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ea1ed-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea1ed-115">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ea1ed-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea1ed-116">Application</span></span> | <span data-ttu-id="ea1ed-117">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea1ed-117">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ea1ed-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea1ed-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/childFolders
GET /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ea1ed-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ea1ed-119">Optional query parameters</span></span>
<span data-ttu-id="ea1ed-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ea1ed-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea1ed-121">Request headers</span></span>
| <span data-ttu-id="ea1ed-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="ea1ed-122">Name</span></span>       | <span data-ttu-id="ea1ed-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea1ed-123">Type</span></span> | <span data-ttu-id="ea1ed-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea1ed-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ea1ed-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="ea1ed-125">Authorization</span></span>  | <span data-ttu-id="ea1ed-126">string</span><span class="sxs-lookup"><span data-stu-id="ea1ed-126">string</span></span>  | <span data-ttu-id="ea1ed-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ea1ed-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea1ed-129">Request body</span></span>
<span data-ttu-id="ea1ed-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ea1ed-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea1ed-131">Response</span></span>

<span data-ttu-id="ea1ed-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-132">If successful, this method returns a `200 OK` response code and collection of [MailFolder](../resources/mailfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ea1ed-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea1ed-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ea1ed-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea1ed-134">Request</span></span>
<span data-ttu-id="ea1ed-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_childfolders"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/{id}/childFolders
```
##### <a name="response"></a><span data-ttu-id="ea1ed-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea1ed-136">Response</span></span>
<span data-ttu-id="ea1ed-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List childFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
