---
title: Directivas de lista
description: Recuperar todos los objetos de directiva en el directorio.
ms.openlocfilehash: 5abff0973a53dc3bddfd256dbc43faad519e20e4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090276"
---
# <a name="list-policies"></a><span data-ttu-id="88206-103">Directivas de lista</span><span class="sxs-lookup"><span data-stu-id="88206-103">List Policies</span></span>

> <span data-ttu-id="88206-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="88206-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="88206-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="88206-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="88206-106">Recuperar todos los objetos de [Directiva](../resources/policy.md) en el directorio.</span><span class="sxs-lookup"><span data-stu-id="88206-106">Retrieve all [policy](../resources/policy.md) objects in the directory.</span></span>

## <a name="permissions"></a><span data-ttu-id="88206-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="88206-107">Permissions</span></span>
<span data-ttu-id="88206-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88206-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="88206-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88206-110">Permission type</span></span>      | <span data-ttu-id="88206-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88206-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="88206-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88206-112">Delegated (work or school account)</span></span> | <span data-ttu-id="88206-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="88206-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="88206-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88206-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88206-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88206-115">Not supported.</span></span>    |
|<span data-ttu-id="88206-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88206-116">Application</span></span> | <span data-ttu-id="88206-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88206-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="88206-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88206-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /policies
```
## <a name="request-headers"></a><span data-ttu-id="88206-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88206-119">Request headers</span></span>
| <span data-ttu-id="88206-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="88206-120">Name</span></span>       | <span data-ttu-id="88206-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="88206-121">Type</span></span> | <span data-ttu-id="88206-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="88206-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="88206-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="88206-123">Authorization</span></span>  | <span data-ttu-id="88206-124">string</span><span class="sxs-lookup"><span data-stu-id="88206-124">string</span></span>  | <span data-ttu-id="88206-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88206-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="88206-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88206-127">Request body</span></span>
<span data-ttu-id="88206-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="88206-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="88206-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88206-129">Response</span></span>

<span data-ttu-id="88206-130">Si tiene éxito, este método devuelve `200 OK` objetos de código y la [Directiva](../resources/policy.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88206-130">If successful, this method returns `200 OK` response code and [policy](../resources/policy.md) objects in the response body.</span></span> <span data-ttu-id="88206-131">Si no lo consigue...</span><span class="sxs-lookup"><span data-stu-id="88206-131">If unsuccessful...</span></span>

## <a name="example"></a><span data-ttu-id="88206-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88206-132">Example</span></span>
<span data-ttu-id="88206-133">En el ejemplo siguiente se recupera todas las directivas.</span><span class="sxs-lookup"><span data-stu-id="88206-133">The following example retrieves all policies.</span></span>

##### <a name="request"></a><span data-ttu-id="88206-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88206-134">Request</span></span>
<span data-ttu-id="88206-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88206-135">Here is an example of the request.</span></span>

```http
GET https://graph.microsoft.com/beta/policies
```

##### <a name="response"></a><span data-ttu-id="88206-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88206-136">Response</span></span>
<span data-ttu-id="88206-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88206-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
{
    "value":[
        {
            "id":"id-value",
            "alternativeIdentifier":null,
            "definition":["policy-definition"],
            "displayName":"name-value",
            "isOrganizationDefault":boolean-value,
            "keyCredentials":[key-credentials],
            "type":"type-value"
        }
    ]
}
```
