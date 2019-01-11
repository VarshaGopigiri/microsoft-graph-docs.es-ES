---
title: Directivas de lista
description: Recuperar todos los objetos de directiva en el directorio.
localization_priority: Normal
ms.openlocfilehash: ea97146b646068515ab6fdc7fab4b3cefb16031e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836060"
---
# <a name="list-policies"></a><span data-ttu-id="88bba-103">Directivas de lista</span><span class="sxs-lookup"><span data-stu-id="88bba-103">List Policies</span></span>

> <span data-ttu-id="88bba-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="88bba-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="88bba-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="88bba-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="88bba-106">Recuperar todos los objetos de [Directiva](../resources/policy.md) en el directorio.</span><span class="sxs-lookup"><span data-stu-id="88bba-106">Retrieve all [policy](../resources/policy.md) objects in the directory.</span></span>

## <a name="permissions"></a><span data-ttu-id="88bba-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="88bba-107">Permissions</span></span>
<span data-ttu-id="88bba-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88bba-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="88bba-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88bba-110">Permission type</span></span>      | <span data-ttu-id="88bba-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88bba-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="88bba-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88bba-112">Delegated (work or school account)</span></span> | <span data-ttu-id="88bba-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="88bba-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="88bba-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88bba-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88bba-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88bba-115">Not supported.</span></span>    |
|<span data-ttu-id="88bba-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88bba-116">Application</span></span> | <span data-ttu-id="88bba-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88bba-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="88bba-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88bba-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /policies
```
## <a name="request-headers"></a><span data-ttu-id="88bba-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88bba-119">Request headers</span></span>
| <span data-ttu-id="88bba-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="88bba-120">Name</span></span>       | <span data-ttu-id="88bba-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="88bba-121">Type</span></span> | <span data-ttu-id="88bba-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="88bba-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="88bba-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="88bba-123">Authorization</span></span>  | <span data-ttu-id="88bba-124">string</span><span class="sxs-lookup"><span data-stu-id="88bba-124">string</span></span>  | <span data-ttu-id="88bba-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88bba-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="88bba-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88bba-127">Request body</span></span>
<span data-ttu-id="88bba-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="88bba-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="88bba-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88bba-129">Response</span></span>

<span data-ttu-id="88bba-130">Si tiene éxito, este método devuelve `200 OK` objetos de código y la [Directiva](../resources/policy.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88bba-130">If successful, this method returns `200 OK` response code and [policy](../resources/policy.md) objects in the response body.</span></span> <span data-ttu-id="88bba-131">Si no lo consigue...</span><span class="sxs-lookup"><span data-stu-id="88bba-131">If unsuccessful...</span></span>

## <a name="example"></a><span data-ttu-id="88bba-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88bba-132">Example</span></span>
<span data-ttu-id="88bba-133">En el ejemplo siguiente se recupera todas las directivas.</span><span class="sxs-lookup"><span data-stu-id="88bba-133">The following example retrieves all policies.</span></span>

##### <a name="request"></a><span data-ttu-id="88bba-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88bba-134">Request</span></span>
<span data-ttu-id="88bba-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88bba-135">Here is an example of the request.</span></span>

```http
GET https://graph.microsoft.com/beta/policies
```

##### <a name="response"></a><span data-ttu-id="88bba-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88bba-136">Response</span></span>
<span data-ttu-id="88bba-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88bba-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
