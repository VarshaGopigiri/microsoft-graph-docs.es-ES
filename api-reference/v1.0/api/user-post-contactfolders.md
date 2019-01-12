---
title: Create ContactFolder
description: Crea una contactFolder en la carpeta predeterminada de contactos del usuario.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 2e76da12d152a28f5f8579d41f1cf3e159b0e078
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921678"
---
# <a name="create-contactfolder"></a><span data-ttu-id="3c068-103">Create ContactFolder</span><span class="sxs-lookup"><span data-stu-id="3c068-103">Create ContactFolder</span></span>

<span data-ttu-id="3c068-104">Crea una contactFolder en la carpeta predeterminada de contactos del usuario.</span><span class="sxs-lookup"><span data-stu-id="3c068-104">Create a new contactFolder under the user's default contacts folder.</span></span>

<span data-ttu-id="3c068-105">También se puede [crear una contactfolder como elemento secundario de cualquier carpeta de contacto especificada](contactfolder-post-childfolders.md).</span><span class="sxs-lookup"><span data-stu-id="3c068-105">You can also [create a new contactfolder as a child of any specified contact folder](contactfolder-post-childfolders.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="3c068-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="3c068-106">Permissions</span></span>
<span data-ttu-id="3c068-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3c068-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3c068-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3c068-109">Permission type</span></span>      | <span data-ttu-id="3c068-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3c068-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3c068-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3c068-111">Delegated (work or school account)</span></span> | <span data-ttu-id="3c068-112">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3c068-112">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="3c068-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3c068-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3c068-114">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3c068-114">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="3c068-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3c068-115">Application</span></span> | <span data-ttu-id="3c068-116">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3c068-116">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="3c068-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3c068-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/contactFolders
```
## <a name="request-headers"></a><span data-ttu-id="3c068-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3c068-118">Request headers</span></span>
| <span data-ttu-id="3c068-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c068-119">Header</span></span>       | <span data-ttu-id="3c068-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3c068-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3c068-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="3c068-121">Authorization</span></span>  | <span data-ttu-id="3c068-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3c068-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="3c068-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3c068-124">Content-Type</span></span>  | <span data-ttu-id="3c068-125">application/json</span><span class="sxs-lookup"><span data-stu-id="3c068-125">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3c068-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3c068-126">Request body</span></span>
<span data-ttu-id="3c068-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ContactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="3c068-127">In the request body, supply a JSON representation of [ContactFolder](../resources/contactfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="3c068-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c068-128">Response</span></span>

<span data-ttu-id="3c068-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c068-129">If successful, this method returns `201 Created` response code and [ContactFolder](../resources/contactfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3c068-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3c068-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3c068-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3c068-131">Request</span></span>
<span data-ttu-id="3c068-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3c068-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contactfolder_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contactFolders
Content-type: application/json
Content-length: 84

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value"
}
```
<span data-ttu-id="3c068-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="3c068-133">In the request body, supply a JSON representation of [contactFolder](../resources/contactfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="3c068-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c068-134">Response</span></span>
<span data-ttu-id="3c068-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3c068-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 104

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create ContactFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
