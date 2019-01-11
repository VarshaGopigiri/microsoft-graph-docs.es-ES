---
title: Create ContactFolder
description: 'Crea una contactFolder como elemento secundario de una carpeta especificada. '
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 879c0b642a9db22184617544f9cb9be4a7d29cce
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836298"
---
# <a name="create-contactfolder"></a><span data-ttu-id="77be9-103">Create ContactFolder</span><span class="sxs-lookup"><span data-stu-id="77be9-103">Create ContactFolder</span></span>

<span data-ttu-id="77be9-104">Crea una contactFolder como elemento secundario de una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="77be9-104">Create a new contactFolder as a child of a specified folder.</span></span> 

<span data-ttu-id="77be9-105">También se puede [crear una contactFolder en la carpeta de contactos predeterminada del usuario](user-post-contactfolders.md).</span><span class="sxs-lookup"><span data-stu-id="77be9-105">You can also [create a new contactFolder under the user's default contact folder](user-post-contactfolders.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="77be9-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="77be9-106">Permissions</span></span>
<span data-ttu-id="77be9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77be9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="77be9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77be9-109">Permission type</span></span>      | <span data-ttu-id="77be9-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77be9-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="77be9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77be9-111">Delegated (work or school account)</span></span> | <span data-ttu-id="77be9-112">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="77be9-112">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="77be9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77be9-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="77be9-114">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="77be9-114">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="77be9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77be9-115">Application</span></span> | <span data-ttu-id="77be9-116">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="77be9-116">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="77be9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77be9-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contactFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/contactFolders/{id}/childFolders
```
## <a name="request-headers"></a><span data-ttu-id="77be9-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77be9-118">Request headers</span></span>
| <span data-ttu-id="77be9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77be9-119">Header</span></span>       | <span data-ttu-id="77be9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="77be9-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="77be9-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="77be9-121">Authorization</span></span>  | <span data-ttu-id="77be9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="77be9-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="77be9-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="77be9-124">Content-Type</span></span>  | <span data-ttu-id="77be9-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="77be9-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="77be9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77be9-127">Request body</span></span>
<span data-ttu-id="77be9-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ContactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="77be9-128">In the request body, supply a JSON representation of [ContactFolder](../resources/contactfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="77be9-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77be9-129">Response</span></span>

<span data-ttu-id="77be9-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77be9-130">If successful, this method returns `201 Created` response code and [ContactFolder](../resources/contactfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77be9-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77be9-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="77be9-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77be9-132">Request</span></span>
<span data-ttu-id="77be9-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77be9-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contactfolder_from_contactfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contactFolders/{id}/childFolders
Content-type: application/json
Content-length: 84

{
  "displayName": "displayName-value"
}
```
<span data-ttu-id="77be9-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="77be9-134">In the request body, supply a JSON representation of [contactFolder](../resources/contactfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="77be9-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77be9-135">Response</span></span>
<span data-ttu-id="77be9-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77be9-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
