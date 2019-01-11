---
title: Obtener privilegedRoleSettings
description: Recuperar la configuración de las funciones para la función dada. Se devuelve un objeto privilegedRoleSettings.
localization_priority: Normal
ms.openlocfilehash: a80c4027ace009292e7a57b8104e94e114175f1d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879817"
---
# <a name="get-privilegedrolesettings"></a><span data-ttu-id="039b1-104">Obtener privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="039b1-104">Get privilegedRoleSettings</span></span>

> <span data-ttu-id="039b1-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="039b1-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="039b1-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="039b1-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="039b1-107">Recuperar la configuración de las funciones para la función dada.</span><span class="sxs-lookup"><span data-stu-id="039b1-107">Retrieve the role settings for the given role.</span></span> <span data-ttu-id="039b1-108">Se devuelve un objeto [privilegedRoleSettings](../resources/privilegedrolesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="039b1-108">A [privilegedRoleSettings](../resources/privilegedrolesettings.md) object will be returned.</span></span>
## <a name="permissions"></a><span data-ttu-id="039b1-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="039b1-109">Permissions</span></span>

<span data-ttu-id="039b1-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="039b1-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="039b1-112">El solicitante debe tener uno de los siguientes roles: _Administrador de roles con privilegios_, _Administrador Global_, _Administrador de seguridad_o _Lector de seguridad_.</span><span class="sxs-lookup"><span data-stu-id="039b1-112">The requestor needs to have one of the following roles: _Privileged Role Administrator_, _Global Administrator_, _Security Administrator_, or _Security Reader_.</span></span> 

|<span data-ttu-id="039b1-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="039b1-113">Permission type</span></span>      | <span data-ttu-id="039b1-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="039b1-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="039b1-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="039b1-115">Delegated (work or school account)</span></span> | <span data-ttu-id="039b1-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="039b1-116">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="039b1-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="039b1-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="039b1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="039b1-118">Not supported.</span></span>    |
|<span data-ttu-id="039b1-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="039b1-119">Application</span></span> | <span data-ttu-id="039b1-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="039b1-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="039b1-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="039b1-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedRoles/{id}/settings
```
## <a name="optional-query-parameters"></a><span data-ttu-id="039b1-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="039b1-122">Optional query parameters</span></span>
<span data-ttu-id="039b1-123">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="039b1-123">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="039b1-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="039b1-124">Request headers</span></span>
| <span data-ttu-id="039b1-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="039b1-125">Name</span></span>      |<span data-ttu-id="039b1-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="039b1-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="039b1-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="039b1-127">Authorization</span></span>  | <span data-ttu-id="039b1-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="039b1-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="039b1-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="039b1-130">Request body</span></span>
<span data-ttu-id="039b1-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="039b1-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="039b1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="039b1-132">Response</span></span>

<span data-ttu-id="039b1-133">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [privilegedRoleSettings](../resources/privilegedrolesettings.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="039b1-133">If successful, this method returns a `200 OK` response code and [privilegedRoleSettings](../resources/privilegedrolesettings.md) object in the response body.</span></span>

<span data-ttu-id="039b1-134">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="039b1-134">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="039b1-135">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="039b1-135">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="039b1-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="039b1-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="039b1-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="039b1-137">Request</span></span>
<span data-ttu-id="039b1-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="039b1-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedrolesettings"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoles/{id}/settings
```
##### <a name="response"></a><span data-ttu-id="039b1-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="039b1-139">Response</span></span>
<span data-ttu-id="039b1-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="039b1-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleSettings"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 228

{
  "minElevationDuration": "2016-10-19T10:37:00Z",
  "maxElavationDuration": "2016-10-19T10:37:00Z",
  "elevationDuration": "2016-10-19T10:37:00Z",
  "id": "id-value",
  "notificationToUserOnElevation": true,
  "ticketingInfoOnElevation": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get privilegedRoleSettings",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
