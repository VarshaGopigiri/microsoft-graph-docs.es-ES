---
title: Crear categoría de Outlook
description: Crear un objeto outlookCategory en la lista principal de categorías del usuario.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: e76f6ddc0f733bd2e50b3aac62707acbed370ee3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984706"
---
# <a name="create-outlook-category"></a><span data-ttu-id="54ae5-103">Crear categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="54ae5-103">Create Outlook category</span></span>

> <span data-ttu-id="54ae5-104">**Importante**: las API de la versión de /beta en Microsoft Graph está en vista preliminar y están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="54ae5-104">**Important**: APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="54ae5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="54ae5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="54ae5-106">Crear un objeto [outlookCategory](../resources/outlookcategory.md) en la lista principal de categorías del usuario.</span><span class="sxs-lookup"><span data-stu-id="54ae5-106">Create an [outlookCategory](../resources/outlookcategory.md) object in the user's master list of categories.</span></span>

## <a name="permissions"></a><span data-ttu-id="54ae5-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="54ae5-107">Permissions</span></span>
<span data-ttu-id="54ae5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="54ae5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="54ae5-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54ae5-110">Permission type</span></span>      | <span data-ttu-id="54ae5-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54ae5-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="54ae5-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54ae5-112">Delegated (work or school account)</span></span> | <span data-ttu-id="54ae5-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="54ae5-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="54ae5-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54ae5-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="54ae5-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="54ae5-115">MailboxSettings.ReadWrite</span></span>   |
|<span data-ttu-id="54ae5-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54ae5-116">Application</span></span> | <span data-ttu-id="54ae5-117">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="54ae5-117">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="54ae5-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54ae5-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/outlook/masterCategories
POST /users/{id|userPrincipalName}/outlook/masterCategories
```
## <a name="request-headers"></a><span data-ttu-id="54ae5-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54ae5-119">Request headers</span></span>
| <span data-ttu-id="54ae5-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="54ae5-120">Name</span></span>       | <span data-ttu-id="54ae5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="54ae5-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="54ae5-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="54ae5-122">Authorization</span></span>  | <span data-ttu-id="54ae5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="54ae5-p103">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="54ae5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54ae5-125">Request body</span></span>
<span data-ttu-id="54ae5-126">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [outlookCategory](../resources/outlookcategory.md).</span><span class="sxs-lookup"><span data-stu-id="54ae5-126">In the request body, supply a JSON representation of [outlookCategory](../resources/outlookcategory.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="54ae5-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54ae5-127">Response</span></span>

<span data-ttu-id="54ae5-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [outlookCategory](../resources/outlookcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54ae5-128">If successful, this method returns `201 Created` response code and [outlookCategory](../resources/outlookcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54ae5-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54ae5-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="54ae5-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54ae5-130">Request</span></span>
<span data-ttu-id="54ae5-131">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54ae5-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_outlookcategory_from_outlookuser"
}-->
```http
POST https://graph.microsoft.com/beta/me/outlook/masterCategories
Content-type: application/json
Content-Length: 70

{
      "displayName":"Project expenses",
      "color":"preset9"
}
```
<span data-ttu-id="54ae5-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [outlookCategory](../resources/outlookcategory.md).</span><span class="sxs-lookup"><span data-stu-id="54ae5-132">In the request body, supply a JSON representation of [outlookCategory](../resources/outlookcategory.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="54ae5-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54ae5-133">Response</span></span>
<span data-ttu-id="54ae5-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54ae5-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookCategory"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 250

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories/$entity",
  "id":"bac262b7-485d-4739-b436-e31467d64fac",
  "displayName":"Project expenses",
  "color":"preset9"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create outlookCategory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
