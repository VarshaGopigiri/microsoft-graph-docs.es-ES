---
title: Directivas de la lista asignadas a la aplicación o entidad de seguridad de servicio
description: Recupere los objetos de directiva asignados a una aplicación o un servicio de entidad de seguridad.
localization_priority: Normal
ms.openlocfilehash: 3c66eece645313f7039f12aec708cba4581fb4bb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875358"
---
# <a name="list-policies-assigned-to-application-or-service-principal"></a><span data-ttu-id="5e513-103">Directivas de la lista asignadas a la aplicación o entidad de seguridad de servicio</span><span class="sxs-lookup"><span data-stu-id="5e513-103">List Policies assigned to Application or Service Principal</span></span>

> <span data-ttu-id="5e513-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5e513-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5e513-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5e513-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5e513-106">Recupere los objetos de [Directiva](../resources/policy.md) asignados a una aplicación o un servicio de entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5e513-106">Retrieve the [policy](../resources/policy.md) objects assigned to an application or service principal.</span></span>

## <a name="permissions"></a><span data-ttu-id="5e513-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5e513-107">Permissions</span></span>
<span data-ttu-id="5e513-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5e513-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5e513-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5e513-110">Permission type</span></span>      | <span data-ttu-id="5e513-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5e513-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5e513-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5e513-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5e513-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="5e513-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="5e513-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5e513-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5e513-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e513-115">Not supported.</span></span>    |
|<span data-ttu-id="5e513-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5e513-116">Application</span></span> | <span data-ttu-id="5e513-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e513-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5e513-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5e513-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /applications/{id}/policies
```

> <span data-ttu-id="5e513-119">Nota: El identificador de"" en la solicitud es la propiedad "id" de la aplicación o el servicio de entidad de seguridad, no la propiedad "appid".</span><span class="sxs-lookup"><span data-stu-id="5e513-119">Note: The "id" in the request is the "id" property of the application or service principal, not the "appid" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5e513-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5e513-120">Request headers</span></span>
| <span data-ttu-id="5e513-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="5e513-121">Name</span></span>       | <span data-ttu-id="5e513-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e513-122">Type</span></span> | <span data-ttu-id="5e513-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e513-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5e513-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="5e513-124">Authorization</span></span>  | <span data-ttu-id="5e513-125">string</span><span class="sxs-lookup"><span data-stu-id="5e513-125">string</span></span>  | <span data-ttu-id="5e513-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e513-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5e513-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5e513-128">Request body</span></span>
<span data-ttu-id="5e513-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5e513-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5e513-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e513-130">Response</span></span>

<span data-ttu-id="5e513-131">Si tiene éxito, este método devuelve `200 OK` objetos de código y la [Directiva](../resources/policy.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e513-131">If successful, this method returns `200 OK` response code and [policy](../resources/policy.md) objects in the response body.</span></span> <span data-ttu-id="5e513-132">Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.</span><span class="sxs-lookup"><span data-stu-id="5e513-132">If unsuccessful, a `4xx` error will be returned with specific details.</span></span>

## <a name="example"></a><span data-ttu-id="5e513-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e513-133">Example</span></span>
<span data-ttu-id="5e513-134">En el ejemplo siguiente se recupera las directivas asignadas a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e513-134">The following example retrieves the policies assigned to an application.</span></span>

##### <a name="request"></a><span data-ttu-id="5e513-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5e513-135">Request</span></span>
<span data-ttu-id="5e513-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e513-136">Here is an example of the request.</span></span>

```http
GET https://graph.microsoft.com/beta/applications/{id}/policies
```

##### <a name="response"></a><span data-ttu-id="5e513-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e513-137">Response</span></span>
<span data-ttu-id="5e513-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5e513-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Cache-Control: private
Content-Type: application/json

{
    "value":[
        {
            "@odata.type":"#microsoft.graph.policy",
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
