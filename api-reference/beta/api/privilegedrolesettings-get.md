---
title: Obtener privilegedRoleSettings
description: Recuperar la configuración de las funciones para la función dada. Se devuelve un objeto privilegedRoleSettings.
ms.openlocfilehash: c064e2eb11a4e91247894338c43c7c6dd9f9dcc3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084431"
---
# <a name="get-privilegedrolesettings"></a><span data-ttu-id="8089e-104">Obtener privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="8089e-104">Get privilegedRoleSettings</span></span>

> <span data-ttu-id="8089e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8089e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8089e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8089e-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8089e-107">Recuperar la configuración de las funciones para la función dada.</span><span class="sxs-lookup"><span data-stu-id="8089e-107">Retrieve the role settings for the given role.</span></span> <span data-ttu-id="8089e-108">Se devuelve un objeto [privilegedRoleSettings](../resources/privilegedrolesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="8089e-108">A [privilegedRoleSettings](../resources/privilegedrolesettings.md) object will be returned.</span></span>
## <a name="permissions"></a><span data-ttu-id="8089e-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="8089e-109">Permissions</span></span>

<span data-ttu-id="8089e-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8089e-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="8089e-112">El solicitante debe tener uno de los siguientes roles: _Administrador de roles con privilegios_, _Administrador Global_, _Administrador de seguridad_o _Lector de seguridad_.</span><span class="sxs-lookup"><span data-stu-id="8089e-112">The requestor needs to have one of the following roles: _Privileged Role Administrator_, _Global Administrator_, _Security Administrator_, or _Security Reader_.</span></span> 

|<span data-ttu-id="8089e-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8089e-113">Permission type</span></span>      | <span data-ttu-id="8089e-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8089e-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8089e-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8089e-115">Delegated (work or school account)</span></span> | <span data-ttu-id="8089e-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="8089e-116">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="8089e-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8089e-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8089e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8089e-118">Not supported.</span></span>    |
|<span data-ttu-id="8089e-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8089e-119">Application</span></span> | <span data-ttu-id="8089e-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8089e-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8089e-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8089e-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedRoles/{id}/settings
```
## <a name="optional-query-parameters"></a><span data-ttu-id="8089e-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8089e-122">Optional query parameters</span></span>
<span data-ttu-id="8089e-123">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8089e-123">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="8089e-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8089e-124">Request headers</span></span>
| <span data-ttu-id="8089e-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="8089e-125">Name</span></span>      |<span data-ttu-id="8089e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="8089e-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="8089e-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="8089e-127">Authorization</span></span>  | <span data-ttu-id="8089e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8089e-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8089e-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8089e-130">Request body</span></span>
<span data-ttu-id="8089e-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8089e-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8089e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8089e-132">Response</span></span>

<span data-ttu-id="8089e-133">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [privilegedRoleSettings](../resources/privilegedrolesettings.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8089e-133">If successful, this method returns a `200 OK` response code and [privilegedRoleSettings](../resources/privilegedrolesettings.md) object in the response body.</span></span>

<span data-ttu-id="8089e-134">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="8089e-134">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="8089e-135">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="8089e-135">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="8089e-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8089e-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8089e-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8089e-137">Request</span></span>
<span data-ttu-id="8089e-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8089e-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedrolesettings"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoles/{id}/settings
```
##### <a name="response"></a><span data-ttu-id="8089e-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8089e-139">Response</span></span>
<span data-ttu-id="8089e-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8089e-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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