---
title: Create MailFolder
description: Usa esta API para crear una carpeta de correo en la carpeta raíz del buzón del usuario.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: b4a339338063c4aa511a41eac4342b376d8bc1e2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974066"
---
# <a name="create-mailfolder"></a><span data-ttu-id="c378a-103">Create MailFolder</span><span class="sxs-lookup"><span data-stu-id="c378a-103">Create MailFolder</span></span>

> <span data-ttu-id="c378a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c378a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c378a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c378a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c378a-106">Usa esta API para crear una carpeta de correo en la carpeta raíz del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="c378a-106">Use this API to create a new mail folder in the root folder of the user's mailbox.</span></span>
## <a name="permissions"></a><span data-ttu-id="c378a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c378a-107">Permissions</span></span>
<span data-ttu-id="c378a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c378a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c378a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c378a-110">Permission type</span></span>      | <span data-ttu-id="c378a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c378a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c378a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c378a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c378a-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c378a-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c378a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c378a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c378a-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c378a-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c378a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c378a-116">Application</span></span> | <span data-ttu-id="c378a-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c378a-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c378a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c378a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/mailFolders
```
## <a name="request-headers"></a><span data-ttu-id="c378a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c378a-119">Request headers</span></span>
| <span data-ttu-id="c378a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c378a-120">Header</span></span>       | <span data-ttu-id="c378a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c378a-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c378a-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c378a-122">Authorization</span></span>  | <span data-ttu-id="c378a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c378a-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c378a-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c378a-125">Content-Type</span></span>  | <span data-ttu-id="c378a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c378a-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c378a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c378a-127">Request body</span></span>
<span data-ttu-id="c378a-p104">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros. **displayName** es la única propiedad que se puede escribir de un objeto [MailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="c378a-p104">In the request body, provide a JSON object with the following parameters. **displayName** is the only writable property for a [MailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="c378a-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c378a-130">Parameter</span></span>    | <span data-ttu-id="c378a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c378a-131">Type</span></span>   |<span data-ttu-id="c378a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c378a-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c378a-133">displayName</span><span class="sxs-lookup"><span data-stu-id="c378a-133">displayName</span></span>|<span data-ttu-id="c378a-134">String</span><span class="sxs-lookup"><span data-stu-id="c378a-134">String</span></span>|<span data-ttu-id="c378a-135">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="c378a-135">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="c378a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c378a-136">Response</span></span>

<span data-ttu-id="c378a-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y un objeto [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c378a-137">If successful, this method returns `201 Created` response code and a [MailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c378a-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c378a-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c378a-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c378a-139">Request</span></span>
<span data-ttu-id="c378a-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c378a-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_user"
}-->
```http
POST https://graph.microsoft.com/beta/me/mailFolders
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value"
}
```

##### <a name="response"></a><span data-ttu-id="c378a-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c378a-141">Response</span></span>
<span data-ttu-id="c378a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c378a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 179

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create MailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
