---
title: Create ContactFolder
description: Crea una contactFolder en la carpeta predeterminada de contactos del usuario.
ms.openlocfilehash: 0d8e76c62d0e5265656bc953696d613d2c59675a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090289"
---
# <a name="create-contactfolder"></a><span data-ttu-id="58e5e-103">Create ContactFolder</span><span class="sxs-lookup"><span data-stu-id="58e5e-103">Create ContactFolder</span></span>

> <span data-ttu-id="58e5e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="58e5e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="58e5e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="58e5e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="58e5e-106">Crea una contactFolder en la carpeta predeterminada de contactos del usuario.</span><span class="sxs-lookup"><span data-stu-id="58e5e-106">Create a new contactFolder under the user's default contacts folder.</span></span>

<span data-ttu-id="58e5e-107">También se puede [crear una contactfolder como elemento secundario de cualquier carpeta de contacto especificada](contactfolder-post-childfolders.md).</span><span class="sxs-lookup"><span data-stu-id="58e5e-107">You can also [create a new contactfolder as a child of any specified contact folder](contactfolder-post-childfolders.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="58e5e-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="58e5e-108">Permissions</span></span>
<span data-ttu-id="58e5e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="58e5e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="58e5e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="58e5e-111">Permission type</span></span>      | <span data-ttu-id="58e5e-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="58e5e-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="58e5e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="58e5e-113">Delegated (work or school account)</span></span> | <span data-ttu-id="58e5e-114">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="58e5e-114">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="58e5e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="58e5e-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="58e5e-116">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="58e5e-116">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="58e5e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="58e5e-117">Application</span></span> | <span data-ttu-id="58e5e-118">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="58e5e-118">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="58e5e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="58e5e-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/contactFolders
```
## <a name="request-headers"></a><span data-ttu-id="58e5e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="58e5e-120">Request headers</span></span>
| <span data-ttu-id="58e5e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58e5e-121">Header</span></span>       | <span data-ttu-id="58e5e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="58e5e-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="58e5e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="58e5e-123">Authorization</span></span>  | <span data-ttu-id="58e5e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="58e5e-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="58e5e-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="58e5e-126">Content-Type</span></span>  | <span data-ttu-id="58e5e-127">application/json</span><span class="sxs-lookup"><span data-stu-id="58e5e-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="58e5e-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="58e5e-128">Request body</span></span>
<span data-ttu-id="58e5e-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ContactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="58e5e-129">In the request body, supply a JSON representation of [ContactFolder](../resources/contactfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="58e5e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58e5e-130">Response</span></span>

<span data-ttu-id="58e5e-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58e5e-131">If successful, this method returns `201 Created` response code and [ContactFolder](../resources/contactfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="58e5e-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58e5e-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="58e5e-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="58e5e-133">Request</span></span>
<span data-ttu-id="58e5e-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58e5e-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contactfolder_from_user"
}-->
```http
POST https://graph.microsoft.com/beta/me/contactFolders
Content-type: application/json
Content-length: 84

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value"
}
```
<span data-ttu-id="58e5e-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="58e5e-135">In the request body, supply a JSON representation of [contactFolder](../resources/contactfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="58e5e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58e5e-136">Response</span></span>
<span data-ttu-id="58e5e-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="58e5e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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