---
title: Create MailFolder
description: Usa esta API para crear una carpeta de correo en la carpeta raíz del buzón del usuario.
ms.openlocfilehash: 6e6b42197dcb5b968a59303d2e9c8c8b1ddf6feb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089592"
---
# <a name="create-mailfolder"></a><span data-ttu-id="9e240-103">Create MailFolder</span><span class="sxs-lookup"><span data-stu-id="9e240-103">Create MailFolder</span></span>

> <span data-ttu-id="9e240-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9e240-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9e240-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9e240-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9e240-106">Usa esta API para crear una carpeta de correo en la carpeta raíz del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="9e240-106">Use this API to create a new mail folder in the root folder of the user's mailbox.</span></span>
## <a name="permissions"></a><span data-ttu-id="9e240-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9e240-107">Permissions</span></span>
<span data-ttu-id="9e240-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9e240-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9e240-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9e240-110">Permission type</span></span>      | <span data-ttu-id="9e240-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9e240-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9e240-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9e240-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9e240-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9e240-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="9e240-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9e240-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9e240-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9e240-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="9e240-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9e240-116">Application</span></span> | <span data-ttu-id="9e240-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9e240-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="9e240-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9e240-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/mailFolders
```
## <a name="request-headers"></a><span data-ttu-id="9e240-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9e240-119">Request headers</span></span>
| <span data-ttu-id="9e240-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e240-120">Header</span></span>       | <span data-ttu-id="9e240-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9e240-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9e240-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="9e240-122">Authorization</span></span>  | <span data-ttu-id="9e240-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9e240-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="9e240-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9e240-125">Content-Type</span></span>  | <span data-ttu-id="9e240-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9e240-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9e240-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9e240-127">Request body</span></span>
<span data-ttu-id="9e240-p104">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros. **displayName** es la única propiedad que se puede escribir de un objeto [MailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="9e240-p104">In the request body, provide a JSON object with the following parameters. **displayName** is the only writable property for a [MailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="9e240-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9e240-130">Parameter</span></span>    | <span data-ttu-id="9e240-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e240-131">Type</span></span>   |<span data-ttu-id="9e240-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e240-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9e240-133">displayName</span><span class="sxs-lookup"><span data-stu-id="9e240-133">displayName</span></span>|<span data-ttu-id="9e240-134">String</span><span class="sxs-lookup"><span data-stu-id="9e240-134">String</span></span>|<span data-ttu-id="9e240-135">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="9e240-135">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="9e240-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e240-136">Response</span></span>

<span data-ttu-id="9e240-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y un objeto [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e240-137">If successful, this method returns `201 Created` response code and a [MailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9e240-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9e240-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9e240-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9e240-139">Request</span></span>
<span data-ttu-id="9e240-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9e240-140">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="9e240-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9e240-141">Response</span></span>
<span data-ttu-id="9e240-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9e240-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
