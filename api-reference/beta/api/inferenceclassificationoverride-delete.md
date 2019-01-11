---
title: Delete inferenceClassificationOverride
description: Eliminar un reemplazo dirigidos a Bandeja de entrada especificado por su identificador.
localization_priority: Normal
ms.openlocfilehash: 7db351e11ccfa8e88fe97ff1ee22173a87242d57
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870143"
---
# <a name="delete-inferenceclassificationoverride"></a><span data-ttu-id="d96f8-103">Delete inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="d96f8-103">Delete inferenceClassificationOverride</span></span>

> <span data-ttu-id="d96f8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d96f8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d96f8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d96f8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d96f8-106">Eliminar un reemplazo [Dirigidos a Bandeja de entrada](../resources/manage-focused-inbox.md) especificado por su identificador.</span><span class="sxs-lookup"><span data-stu-id="d96f8-106">Delete a [Focused Inbox](../resources/manage-focused-inbox.md) override specified by its ID.</span></span>
## <a name="permissions"></a><span data-ttu-id="d96f8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d96f8-107">Permissions</span></span>
<span data-ttu-id="d96f8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d96f8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d96f8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d96f8-110">Permission type</span></span>      | <span data-ttu-id="d96f8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d96f8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d96f8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d96f8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d96f8-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d96f8-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="d96f8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d96f8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d96f8-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d96f8-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="d96f8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d96f8-116">Application</span></span> | <span data-ttu-id="d96f8-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d96f8-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d96f8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d96f8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/inferenceClassification/overrides/{id}
DELETE /users/{id}/inferenceClassification/overrides/{id}
```
## <a name="request-headers"></a><span data-ttu-id="d96f8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d96f8-119">Request headers</span></span>
| <span data-ttu-id="d96f8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d96f8-120">Name</span></span>       | <span data-ttu-id="d96f8-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d96f8-121">Type</span></span> | <span data-ttu-id="d96f8-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d96f8-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d96f8-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d96f8-123">Authorization</span></span>  | <span data-ttu-id="d96f8-124">string</span><span class="sxs-lookup"><span data-stu-id="d96f8-124">string</span></span>  | <span data-ttu-id="d96f8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d96f8-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d96f8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d96f8-127">Request body</span></span>
<span data-ttu-id="d96f8-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d96f8-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d96f8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d96f8-129">Response</span></span>

<span data-ttu-id="d96f8-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d96f8-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d96f8-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d96f8-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d96f8-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d96f8-133">Request</span></span>
<span data-ttu-id="d96f8-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d96f8-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_inferenceclassificationoverride"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/inferenceClassification/overrides/98f5bdef-576a-404d-a2ea-07a3cf34af4r
```
##### <a name="response"></a><span data-ttu-id="d96f8-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d96f8-135">Response</span></span>
<span data-ttu-id="d96f8-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d96f8-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete inferenceClassificationOverride",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
