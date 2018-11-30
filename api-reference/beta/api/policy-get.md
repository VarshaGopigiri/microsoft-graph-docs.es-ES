---
title: Obtener la directiva
description: Recuperar las propiedades de una directiva.
ms.openlocfilehash: a6827813193d134f54c3274e2b035e241bb99dc5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084422"
---
# <a name="get-policy"></a><span data-ttu-id="c897e-103">Obtener la directiva</span><span class="sxs-lookup"><span data-stu-id="c897e-103">Get Policy</span></span>

> <span data-ttu-id="c897e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c897e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c897e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c897e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c897e-106">Recuperar las propiedades de una [Directiva](../resources/policy.md).</span><span class="sxs-lookup"><span data-stu-id="c897e-106">Retrieve the properties of a [policy](../resources/policy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="c897e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c897e-107">Permissions</span></span>
<span data-ttu-id="c897e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c897e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c897e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c897e-110">Permission type</span></span>      | <span data-ttu-id="c897e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c897e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c897e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c897e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c897e-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c897e-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c897e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c897e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c897e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c897e-115">Not supported.</span></span>    |
|<span data-ttu-id="c897e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c897e-116">Application</span></span> | <span data-ttu-id="c897e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c897e-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c897e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c897e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /policies/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c897e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c897e-119">Request headers</span></span>
| <span data-ttu-id="c897e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c897e-120">Name</span></span>       | <span data-ttu-id="c897e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="c897e-121">Type</span></span> | <span data-ttu-id="c897e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c897e-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c897e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c897e-123">Authorization</span></span>  | <span data-ttu-id="c897e-124">string</span><span class="sxs-lookup"><span data-stu-id="c897e-124">string</span></span>  | <span data-ttu-id="c897e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c897e-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c897e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c897e-127">Request body</span></span>
<span data-ttu-id="c897e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c897e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c897e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c897e-129">Response</span></span>

<span data-ttu-id="c897e-130">Si tiene éxito, este método devuelve `200 OK` código de respuesta y un objeto de [Directiva](../resources/policy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c897e-130">If successful, this method returns `200 OK` response code and a [policy](../resources/policy.md) object in the response body.</span></span> <span data-ttu-id="c897e-131">Si unsucccessful...</span><span class="sxs-lookup"><span data-stu-id="c897e-131">If unsucccessful...</span></span>

## <a name="example"></a><span data-ttu-id="c897e-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c897e-132">Example</span></span>
<span data-ttu-id="c897e-133">En el ejemplo siguiente se recupera una directiva específica.</span><span class="sxs-lookup"><span data-stu-id="c897e-133">The following example retrieves a specific policy.</span></span>

##### <a name="request"></a><span data-ttu-id="c897e-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c897e-134">Request</span></span>
<span data-ttu-id="c897e-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c897e-135">Here is an example of the request.</span></span>

```http
GET https://graph.microsoft.com/beta/policies/{id}
```

##### <a name="response"></a><span data-ttu-id="c897e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c897e-136">Response</span></span>
<span data-ttu-id="c897e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c897e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#policies/$entity",
    "id":"id-value",
    "alternativeIdentifier":null,
    "definition":["policy-definition"],
    "displayName":"name-value",
    "isOrganizationDefault":boolean-value,
    "keyCredentials":[key-credentials],
    "type":"type-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: createReply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
