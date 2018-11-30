---
title: Enumerar las aplicaciones y entidades de seguridad de servicio con específico directiva asignada
description: Recuperar la aplicación y objetos del servicio de entidad de seguridad con la directiva especificada asignada.
ms.openlocfilehash: 3f281d7c60a506676a78637ad71f1ce26de35e34
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089581"
---
# <a name="list-applications-and-service-principals-with-specific-policy-assigned"></a><span data-ttu-id="5f1c2-103">Enumerar las aplicaciones y entidades de seguridad de servicio con específico directiva asignada</span><span class="sxs-lookup"><span data-stu-id="5f1c2-103">List Applications and Service Principals with specific Policy assigned</span></span>

> <span data-ttu-id="5f1c2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5f1c2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5f1c2-106">Recupere los objetos de [aplicación](../resources/application.md) y [servicio de entidad de seguridad](../resources/serviceprincipal.md) con la directiva especificada asignada.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-106">Retrieve the [application](../resources/application.md) and [service principal](../resources/serviceprincipal.md) objects with the specified policy assigned.</span></span>

## <a name="permissions"></a><span data-ttu-id="5f1c2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5f1c2-107">Permissions</span></span>
<span data-ttu-id="5f1c2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5f1c2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5f1c2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5f1c2-110">Permission type</span></span>      | <span data-ttu-id="5f1c2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5f1c2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5f1c2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5f1c2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5f1c2-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="5f1c2-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="5f1c2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5f1c2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5f1c2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-115">Not supported.</span></span>    |
|<span data-ttu-id="5f1c2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f1c2-116">Application</span></span> | <span data-ttu-id="5f1c2-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5f1c2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f1c2-118">HTTP request</span></span>
```http
GET /policies/{id}/appliesTo
```

## <a name="request-headers"></a><span data-ttu-id="5f1c2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f1c2-119">Request headers</span></span>
| <span data-ttu-id="5f1c2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f1c2-120">Name</span></span>       | <span data-ttu-id="5f1c2-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f1c2-121">Type</span></span> | <span data-ttu-id="5f1c2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f1c2-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5f1c2-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f1c2-123">Authorization</span></span>  | <span data-ttu-id="5f1c2-124">string</span><span class="sxs-lookup"><span data-stu-id="5f1c2-124">string</span></span>  | <span data-ttu-id="5f1c2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5f1c2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5f1c2-127">Request body</span></span>
<span data-ttu-id="5f1c2-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5f1c2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f1c2-129">Response</span></span>

<span data-ttu-id="5f1c2-130">Si tiene éxito, este método devuelve `200 OK` objetos de código y la [aplicación](../resources/application.md) y la [entidad de seguridad del servicio](../resources/serviceprincipal.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-130">If successful, this method returns `200 OK` response code and [application](../resources/application.md) and [service principal](../resources/serviceprincipal.md) objects in the response body.</span></span> <span data-ttu-id="5f1c2-131">Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-131">If unsuccessful, a `4xx` error will be returned with specific details.</span></span>

## <a name="example"></a><span data-ttu-id="5f1c2-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f1c2-132">Example</span></span>
<span data-ttu-id="5f1c2-133">En el ejemplo siguiente se recupera las aplicaciones y entidades de seguridad de servicio con asignada una directiva específica.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-133">The following example retrieves the applications and service principals with a specific policy assigned.</span></span>

##### <a name="request"></a><span data-ttu-id="5f1c2-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f1c2-134">Request</span></span>
<span data-ttu-id="5f1c2-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-135">Here is an example of the request.</span></span>

```http
GET https://graph.microsoft.com/beta/policies/{id}/appliesTo
```

##### <a name="response"></a><span data-ttu-id="5f1c2-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f1c2-136">Response</span></span>
<span data-ttu-id="5f1c2-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5f1c2-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "value":[
        {
            "@odata.type"="#microsoft.graph.application",
            "appId":"appId-value",
            "displayName":"displayName-value",
            "errorUrl":"errorUrl-value",
            "groupMembershipClaims":"groupMembershipClaims-value",
            "homepage":"homepage-value",
            "id":"id-value",
            "keyCredentials":[key-credentials],
            "logoutUrl":"logoutUrl-value",
            "replyUrls":["replyUrls-value"]
        }
    ]
}
```
