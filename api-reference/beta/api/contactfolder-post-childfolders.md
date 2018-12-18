---
title: Create ContactFolder
description: 'Crea una contactFolder como elemento secundario de una carpeta especificada. '
author: angelgolfer-ms
ms.openlocfilehash: a6b638610ed487fe69d80254c36efc3478f476cc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27336487"
---
# <a name="create-contactfolder"></a><span data-ttu-id="52331-103">Create ContactFolder</span><span class="sxs-lookup"><span data-stu-id="52331-103">Create ContactFolder</span></span>

> <span data-ttu-id="52331-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="52331-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="52331-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="52331-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="52331-106">Crea una contactFolder como elemento secundario de una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="52331-106">Create a new contactFolder as a child of a specified folder.</span></span> 

<span data-ttu-id="52331-107">También se puede [crear una contactFolder en la carpeta de contactos predeterminada del usuario](user-post-contactfolders.md).</span><span class="sxs-lookup"><span data-stu-id="52331-107">You can also [create a new contactFolder under the user's default contact folder](user-post-contactfolders.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="52331-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="52331-108">Permissions</span></span>
<span data-ttu-id="52331-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="52331-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="52331-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="52331-111">Permission type</span></span>      | <span data-ttu-id="52331-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="52331-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="52331-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="52331-113">Delegated (work or school account)</span></span> | <span data-ttu-id="52331-114">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="52331-114">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="52331-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="52331-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="52331-116">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="52331-116">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="52331-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="52331-117">Application</span></span> | <span data-ttu-id="52331-118">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="52331-118">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="52331-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52331-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contactFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/contactFolders/{id}/childFolders
```
## <a name="request-headers"></a><span data-ttu-id="52331-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52331-120">Request headers</span></span>
| <span data-ttu-id="52331-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52331-121">Header</span></span>       | <span data-ttu-id="52331-122">Valor</span><span class="sxs-lookup"><span data-stu-id="52331-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="52331-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="52331-123">Authorization</span></span>  | <span data-ttu-id="52331-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="52331-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="52331-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="52331-126">Content-Type</span></span>  | <span data-ttu-id="52331-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="52331-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="52331-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52331-129">Request body</span></span>
<span data-ttu-id="52331-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ContactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="52331-130">In the request body, supply a JSON representation of [ContactFolder](../resources/contactfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="52331-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52331-131">Response</span></span>

<span data-ttu-id="52331-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52331-132">If successful, this method returns `201 Created` response code and [ContactFolder](../resources/contactfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="52331-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52331-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="52331-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52331-134">Request</span></span>
<span data-ttu-id="52331-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52331-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contactfolder_from_contactfolder"
}-->
```http
POST https://graph.microsoft.com/beta/me/contactFolders/{id}/childFolders
Content-type: application/json
Content-length: 84

{
  "displayName": "displayName-value"
}
```
<span data-ttu-id="52331-136">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="52331-136">In the request body, supply a JSON representation of [contactFolder](../resources/contactfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="52331-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52331-137">Response</span></span>
<span data-ttu-id="52331-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="52331-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
