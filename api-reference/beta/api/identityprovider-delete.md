---
title: Eliminar identityProvider
description: Eliminar un identityProvider existente.
localization_priority: Normal
ms.openlocfilehash: 35689037d4f6a564ee3e1e40d18401ef793ef474
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808298"
---
# <a name="delete-identityprovider"></a><span data-ttu-id="a5d72-103">Eliminar identityProvider</span><span class="sxs-lookup"><span data-stu-id="a5d72-103">Delete identityProvider</span></span>

> <span data-ttu-id="a5d72-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a5d72-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a5d72-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a5d72-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a5d72-106">Eliminar una existente [identityProvider](../resources/identityprovider.md).</span><span class="sxs-lookup"><span data-stu-id="a5d72-106">Delete an existing [identityProvider](../resources/identityprovider.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="a5d72-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a5d72-107">Permissions</span></span>

<span data-ttu-id="a5d72-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5d72-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5d72-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5d72-110">Permission type</span></span>      | <span data-ttu-id="a5d72-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5d72-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a5d72-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5d72-112">Delegated (work or school account)</span></span>|<span data-ttu-id="a5d72-113">IdentityProvider.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a5d72-113">IdentityProvider.ReadWrite.All</span></span>|
|<span data-ttu-id="a5d72-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5d72-114">Delegated (personal Microsoft account)</span></span>| <span data-ttu-id="a5d72-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5d72-115">Not supported.</span></span>|
|<span data-ttu-id="a5d72-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5d72-116">Application</span></span>|<span data-ttu-id="a5d72-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5d72-117">Not supported.</span></span>|

<span data-ttu-id="a5d72-118">La cuenta de trabajo o escuela debe ser un administrador global del inquilino.</span><span class="sxs-lookup"><span data-stu-id="a5d72-118">The work or school account must be a global administrator of the tenant.</span></span>

## <a name="http-request"></a><span data-ttu-id="a5d72-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5d72-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
DELETE /identityProviders/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a5d72-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5d72-120">Request headers</span></span>

|<span data-ttu-id="a5d72-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a5d72-121">Name</span></span>|<span data-ttu-id="a5d72-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5d72-122">Description</span></span>|
|:---------------|:----------|
|<span data-ttu-id="a5d72-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5d72-123">Authorization</span></span>|<span data-ttu-id="a5d72-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5d72-p103">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a5d72-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5d72-126">Request body</span></span>

<span data-ttu-id="a5d72-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a5d72-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a5d72-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5d72-128">Response</span></span>

<span data-ttu-id="a5d72-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="a5d72-129">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="a5d72-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5d72-130">Example</span></span>

<span data-ttu-id="a5d72-131">En el ejemplo siguiente se elimina un **identityProvider**.</span><span class="sxs-lookup"><span data-stu-id="a5d72-131">The following example deletes an **identityProvider**.</span></span>

##### <a name="request"></a><span data-ttu-id="a5d72-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5d72-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_identityprovider"
}-->
```http
DELETE https://graph.microsoft.com/beta/identityProviders/Amazon-OAuth
```

##### <a name="response"></a><span data-ttu-id="a5d72-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5d72-133">Response</span></span>

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
  "description": "Delete identityProvider",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
