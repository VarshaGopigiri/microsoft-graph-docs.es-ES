---
title: List contactFolders
description: Obtiene la colección de la carpeta de contactos predeterminada del usuario que inició sesión.
ms.openlocfilehash: fa19a848fe206a73503aa27adb258a49cc53baf0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028827"
---
# <a name="list-contactfolders"></a><span data-ttu-id="37f7b-103">List contactFolders</span><span class="sxs-lookup"><span data-stu-id="37f7b-103">List contactFolders</span></span>

<span data-ttu-id="37f7b-104">Obtiene la colección de la carpeta de contactos predeterminada del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="37f7b-104">Get the contact folder collection in the default Contacts folder of the signed-in user.</span></span>
## <a name="permissions"></a><span data-ttu-id="37f7b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="37f7b-105">Permissions</span></span>
<span data-ttu-id="37f7b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="37f7b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="37f7b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="37f7b-108">Permission type</span></span>      | <span data-ttu-id="37f7b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="37f7b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="37f7b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="37f7b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="37f7b-111">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="37f7b-111">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="37f7b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="37f7b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="37f7b-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="37f7b-113">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="37f7b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="37f7b-114">Application</span></span> | <span data-ttu-id="37f7b-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="37f7b-115">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="37f7b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37f7b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/contactFolders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="37f7b-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="37f7b-117">Optional query parameters</span></span>
<span data-ttu-id="37f7b-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37f7b-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="37f7b-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37f7b-119">Request headers</span></span>
| <span data-ttu-id="37f7b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37f7b-120">Header</span></span>       | <span data-ttu-id="37f7b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="37f7b-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="37f7b-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="37f7b-122">Authorization</span></span>  | <span data-ttu-id="37f7b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="37f7b-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="37f7b-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="37f7b-125">Content-Type</span></span>   | <span data-ttu-id="37f7b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="37f7b-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="37f7b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37f7b-127">Request body</span></span>
<span data-ttu-id="37f7b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="37f7b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="37f7b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37f7b-129">Response</span></span>

<span data-ttu-id="37f7b-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37f7b-130">If successful, this method returns a `200 OK` response code and collection of [ContactFolder](../resources/contactfolder.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="37f7b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37f7b-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="37f7b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37f7b-132">Request</span></span>
<span data-ttu-id="37f7b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37f7b-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contactfolders"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders
```
##### <a name="response"></a><span data-ttu-id="37f7b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37f7b-134">Response</span></span>
<span data-ttu-id="37f7b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="37f7b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 145

{
  "value": [
    {
      "parentFolderId": "parentFolderId-value",
      "displayName": "displayName-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List contactFolders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
