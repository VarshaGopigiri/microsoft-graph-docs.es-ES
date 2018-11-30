---
title: Create MailFolder
description: Usa esta API para crear una carpeta de correo en la carpeta raíz del buzón del usuario.
ms.openlocfilehash: 5ab8870de334781b59e68cb1d090db5067d53796
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030586"
---
# <a name="create-mailfolder"></a><span data-ttu-id="7ca5f-103">Create MailFolder</span><span class="sxs-lookup"><span data-stu-id="7ca5f-103">Create MailFolder</span></span>

<span data-ttu-id="7ca5f-104">Usa esta API para crear una carpeta de correo en la carpeta raíz del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="7ca5f-104">Use this API to create a new mail folder in the root folder of the user's mailbox.</span></span>
## <a name="permissions"></a><span data-ttu-id="7ca5f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7ca5f-105">Permissions</span></span>
<span data-ttu-id="7ca5f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7ca5f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7ca5f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7ca5f-108">Permission type</span></span>      | <span data-ttu-id="7ca5f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7ca5f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7ca5f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7ca5f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="7ca5f-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7ca5f-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="7ca5f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7ca5f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7ca5f-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7ca5f-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="7ca5f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7ca5f-114">Application</span></span> | <span data-ttu-id="7ca5f-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7ca5f-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="7ca5f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7ca5f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/mailFolders
```
## <a name="request-headers"></a><span data-ttu-id="7ca5f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7ca5f-117">Request headers</span></span>
| <span data-ttu-id="7ca5f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ca5f-118">Header</span></span>       | <span data-ttu-id="7ca5f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7ca5f-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7ca5f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="7ca5f-120">Authorization</span></span>  | <span data-ttu-id="7ca5f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7ca5f-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="7ca5f-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7ca5f-123">Content-Type</span></span>  | <span data-ttu-id="7ca5f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7ca5f-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7ca5f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7ca5f-125">Request body</span></span>
<span data-ttu-id="7ca5f-p103">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros. **displayName** es la única propiedad que se puede escribir de un objeto [MailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="7ca5f-p103">In the request body, provide a JSON object with the following parameters. **displayName** is the only writable property for a [MailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="7ca5f-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7ca5f-128">Parameter</span></span>    | <span data-ttu-id="7ca5f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ca5f-129">Type</span></span>   |<span data-ttu-id="7ca5f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ca5f-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7ca5f-131">displayName</span><span class="sxs-lookup"><span data-stu-id="7ca5f-131">displayName</span></span>|<span data-ttu-id="7ca5f-132">String</span><span class="sxs-lookup"><span data-stu-id="7ca5f-132">String</span></span>|<span data-ttu-id="7ca5f-133">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="7ca5f-133">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="7ca5f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ca5f-134">Response</span></span>

<span data-ttu-id="7ca5f-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y un objeto [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ca5f-135">If successful, this method returns `201 Created` response code and a [MailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7ca5f-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ca5f-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7ca5f-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7ca5f-137">Request</span></span>
<span data-ttu-id="7ca5f-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ca5f-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value"
}
```

##### <a name="response"></a><span data-ttu-id="7ca5f-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ca5f-139">Response</span></span>
<span data-ttu-id="7ca5f-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7ca5f-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
