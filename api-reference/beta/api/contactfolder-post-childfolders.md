---
title: Create ContactFolder
description: 'Crea una contactFolder como elemento secundario de una carpeta especificada. '
ms.openlocfilehash: 5e73a80556a9b896afa166c4207efffb831c9a3c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085550"
---
# <a name="create-contactfolder"></a><span data-ttu-id="8f3d1-103">Create ContactFolder</span><span class="sxs-lookup"><span data-stu-id="8f3d1-103">Create ContactFolder</span></span>

> <span data-ttu-id="8f3d1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8f3d1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8f3d1-106">Crea una contactFolder como elemento secundario de una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-106">Create a new contactFolder as a child of a specified folder.</span></span> 

<span data-ttu-id="8f3d1-107">También se puede [crear una contactFolder en la carpeta de contactos predeterminada del usuario](user-post-contactfolders.md).</span><span class="sxs-lookup"><span data-stu-id="8f3d1-107">You can also [create a new contactFolder under the user's default contact folder](user-post-contactfolders.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="8f3d1-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="8f3d1-108">Permissions</span></span>
<span data-ttu-id="8f3d1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8f3d1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8f3d1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f3d1-111">Permission type</span></span>      | <span data-ttu-id="8f3d1-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f3d1-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8f3d1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f3d1-113">Delegated (work or school account)</span></span> | <span data-ttu-id="8f3d1-114">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f3d1-114">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="8f3d1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f3d1-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8f3d1-116">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f3d1-116">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="8f3d1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f3d1-117">Application</span></span> | <span data-ttu-id="8f3d1-118">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f3d1-118">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="8f3d1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f3d1-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contactFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/contactFolders/{id}/childFolders
```
## <a name="request-headers"></a><span data-ttu-id="8f3d1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f3d1-120">Request headers</span></span>
| <span data-ttu-id="8f3d1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f3d1-121">Header</span></span>       | <span data-ttu-id="8f3d1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8f3d1-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8f3d1-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8f3d1-123">Authorization</span></span>  | <span data-ttu-id="8f3d1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="8f3d1-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8f3d1-126">Content-Type</span></span>  | <span data-ttu-id="8f3d1-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8f3d1-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f3d1-129">Request body</span></span>
<span data-ttu-id="8f3d1-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ContactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="8f3d1-130">In the request body, supply a JSON representation of [ContactFolder](../resources/contactfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="8f3d1-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f3d1-131">Response</span></span>

<span data-ttu-id="8f3d1-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-132">If successful, this method returns `201 Created` response code and [ContactFolder](../resources/contactfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f3d1-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f3d1-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8f3d1-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f3d1-134">Request</span></span>
<span data-ttu-id="8f3d1-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-135">Here is an example of the request.</span></span>
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
<span data-ttu-id="8f3d1-136">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="8f3d1-136">In the request body, supply a JSON representation of [contactFolder](../resources/contactfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="8f3d1-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f3d1-137">Response</span></span>
<span data-ttu-id="8f3d1-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
