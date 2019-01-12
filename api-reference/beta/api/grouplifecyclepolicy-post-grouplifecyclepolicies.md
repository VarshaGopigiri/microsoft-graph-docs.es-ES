---
title: Crear groupLifecyclePolicy
description: Crea un nuevo objeto groupLifecyclePolicy.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: b4fe572e67d0b55ea4ee7adb431f5c0705c9b6db
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959457"
---
# <a name="create-grouplifecyclepolicy"></a><span data-ttu-id="558e1-103">Crear groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="558e1-103">Create groupLifecyclePolicy</span></span>

> <span data-ttu-id="558e1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="558e1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="558e1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="558e1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="558e1-106">Crea un nuevo objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="558e1-106">Creates a new [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="558e1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="558e1-107">Permissions</span></span>

<span data-ttu-id="558e1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="558e1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="558e1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="558e1-110">Permission type</span></span>      | <span data-ttu-id="558e1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="558e1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="558e1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="558e1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="558e1-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="558e1-113">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="558e1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="558e1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="558e1-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="558e1-115">Not supported</span></span> |
|<span data-ttu-id="558e1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="558e1-116">Application</span></span> |  <span data-ttu-id="558e1-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="558e1-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="558e1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="558e1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies

```

## <a name="request-headers"></a><span data-ttu-id="558e1-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="558e1-119">Request headers</span></span>

| <span data-ttu-id="558e1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="558e1-120">Name</span></span> | <span data-ttu-id="558e1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="558e1-121">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="558e1-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="558e1-122">Authorization</span></span> | <span data-ttu-id="558e1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="558e1-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="558e1-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="558e1-125">Content-Type</span></span>  | <span data-ttu-id="558e1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="558e1-126">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="558e1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="558e1-127">Request body</span></span>
<span data-ttu-id="558e1-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="558e1-128">In the request body, supply a JSON representation of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="558e1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="558e1-129">Response</span></span>

<span data-ttu-id="558e1-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="558e1-130">If successful, this method returns `201 Created` response code and [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="558e1-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="558e1-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="558e1-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="558e1-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_grouplifecyclepolicy_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/groupLifecyclePolicies
Content-type: application/json
Content-length: 125

{
  "groupLifetimeInDays": 100,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```
<span data-ttu-id="558e1-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="558e1-133">In the request body, supply a JSON representation of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="558e1-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="558e1-134">Response</span></span>

<span data-ttu-id="558e1-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="558e1-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 174

{
  "id": "ffffffff-ffff-ffff-ffff-ffffffffffff",
  "groupLifetimeInDays": 100,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create groupLifecyclePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
