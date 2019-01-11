---
title: Actualizar oAuth2PermissionGrant
description: Actualizar las propiedades del objeto oAuth2PermissionGrant.
localization_priority: Normal
ms.openlocfilehash: 3c01d62dfb7c0c6906ff860656ee87b5f6d40aed
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822354"
---
# <a name="update-oauth2permissiongrant"></a><span data-ttu-id="d7517-103">Actualizar oAuth2PermissionGrant</span><span class="sxs-lookup"><span data-stu-id="d7517-103">Update oAuth2PermissionGrant</span></span>

> <span data-ttu-id="d7517-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7517-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7517-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7517-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d7517-106">Actualizar las propiedades del objeto oAuth2PermissionGrant.</span><span class="sxs-lookup"><span data-stu-id="d7517-106">Update the properties of oAuth2PermissionGrant object.</span></span>

## <a name="permissions"></a><span data-ttu-id="d7517-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d7517-107">Permissions</span></span>

<span data-ttu-id="d7517-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d7517-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="d7517-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7517-110">Permission type</span></span>      | <span data-ttu-id="d7517-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d7517-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d7517-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7517-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d7517-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d7517-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d7517-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d7517-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d7517-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7517-115">Not supported.</span></span>    |
|<span data-ttu-id="d7517-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7517-116">Application</span></span> | <span data-ttu-id="d7517-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d7517-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d7517-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7517-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /oAuth2Permissiongrants/{id}
PATCH /users/{id | userPrincipalName}/oAuth2Permissiongrants/{id}
PATCH /drive/root/createdByUser/oAuth2Permissiongrants/{id}
```
## <a name="request-headers"></a><span data-ttu-id="d7517-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d7517-119">Request headers</span></span>
| <span data-ttu-id="d7517-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d7517-120">Name</span></span>       | <span data-ttu-id="d7517-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7517-121">Type</span></span> | <span data-ttu-id="d7517-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7517-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d7517-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d7517-123">Authorization</span></span>  | <span data-ttu-id="d7517-124">string</span><span class="sxs-lookup"><span data-stu-id="d7517-124">string</span></span>  | <span data-ttu-id="d7517-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7517-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d7517-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d7517-127">Request body</span></span>
<span data-ttu-id="d7517-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="d7517-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="d7517-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7517-131">Property</span></span>     | <span data-ttu-id="d7517-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7517-132">Type</span></span>   |<span data-ttu-id="d7517-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7517-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d7517-134">scope</span><span class="sxs-lookup"><span data-stu-id="d7517-134">scope</span></span>|<span data-ttu-id="d7517-135">String</span><span class="sxs-lookup"><span data-stu-id="d7517-135">String</span></span>| <span data-ttu-id="d7517-136">Especifica el valor de la notificación de ámbito que se debe esperar a que la aplicación de recursos en el token de acceso de OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="d7517-136">Specifies the value of the scope claim that the resource application should expect in the OAuth 2.0 access token.</span></span> |

## <a name="response"></a><span data-ttu-id="d7517-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7517-137">Response</span></span>

<span data-ttu-id="d7517-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7517-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d7517-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d7517-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d7517-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d7517-141">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_oAuth2Permissiongrant"
}-->
```http
PATCH https://graph.microsoft.com/beta/oAuth2Permissiongrants/{id}
Content-type: application/json
Content-length: 30

{
  "scope": "scope-value"
}
```
##### <a name="response"></a><span data-ttu-id="d7517-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7517-142">Response</span></span>

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
  "description": "Update oAuth2Permissiongrant",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
