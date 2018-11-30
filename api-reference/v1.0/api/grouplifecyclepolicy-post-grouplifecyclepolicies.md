---
title: Crear groupLifecyclePolicy
description: Crea un nuevo objeto groupLifecyclePolicy.
ms.openlocfilehash: d588ca925be011561c14fdbc06bd0a5294faf450
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030499"
---
# <a name="create-grouplifecyclepolicy"></a><span data-ttu-id="d344d-103">Crear groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="d344d-103">Create groupLifecyclePolicy</span></span>

<span data-ttu-id="d344d-104">Crea un nuevo objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d344d-104">Creates a new [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="d344d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d344d-105">Permissions</span></span>

<span data-ttu-id="d344d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d344d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d344d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d344d-108">Permission type</span></span>      | <span data-ttu-id="d344d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d344d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d344d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d344d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d344d-111">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d344d-111">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="d344d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d344d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d344d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d344d-113">Not supported.</span></span>    |
|<span data-ttu-id="d344d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d344d-114">Application</span></span> | <span data-ttu-id="d344d-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d344d-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d344d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d344d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies

```

## <a name="request-headers"></a><span data-ttu-id="d344d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d344d-117">Request headers</span></span>

| <span data-ttu-id="d344d-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="d344d-118">Name</span></span> | <span data-ttu-id="d344d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d344d-119">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="d344d-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="d344d-120">Authorization</span></span> | <span data-ttu-id="d344d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d344d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d344d-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d344d-123">Content-Type</span></span>  | <span data-ttu-id="d344d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d344d-124">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="d344d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d344d-125">Request body</span></span>
<span data-ttu-id="d344d-126">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d344d-126">In the request body, supply a JSON representation of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="d344d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d344d-127">Response</span></span>

<span data-ttu-id="d344d-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d344d-128">If successful, this method returns `201 Created` response code and [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d344d-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d344d-129">Example</span></span>

##### <a name="request"></a><span data-ttu-id="d344d-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d344d-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_grouplifecyclepolicy_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groupLifecyclePolicies
Content-type: application/json
Content-length: 125

{
  "groupLifetimeInDays": 100,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```
<span data-ttu-id="d344d-131">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d344d-131">In the request body, supply a JSON representation of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="d344d-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d344d-132">Response</span></span>

<span data-ttu-id="d344d-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d344d-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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