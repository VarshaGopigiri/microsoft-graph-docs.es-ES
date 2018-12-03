---
title: Get organization
description: Recupera las propiedades y relaciones de la organización actualmente autenticada.
ms.openlocfilehash: 899021e5d38bca660b599222adfdb0bb5586eb6f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087064"
---
# <a name="get-organization"></a><span data-ttu-id="22dbd-103">Get organization</span><span class="sxs-lookup"><span data-stu-id="22dbd-103">Get organization</span></span>

> <span data-ttu-id="22dbd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="22dbd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="22dbd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="22dbd-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="22dbd-106">Recupera las propiedades y relaciones de la organización actualmente autenticada.</span><span class="sxs-lookup"><span data-stu-id="22dbd-106">Retrieve the properties and relationships of currently authenticated organization.</span></span>

<span data-ttu-id="22dbd-107">Puesto que el recurso de la **organización** admite [extensiones](/graph/extensibility-overview), también se puede usar el `GET` operación para obtener las propiedades personalizadas y los datos de extensión en una instancia de la **organización** .</span><span class="sxs-lookup"><span data-stu-id="22dbd-107">Since the **organization** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in an **organization** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="22dbd-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="22dbd-108">Permissions</span></span>
<span data-ttu-id="22dbd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="22dbd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="22dbd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="22dbd-111">Permission type</span></span> | <span data-ttu-id="22dbd-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="22dbd-112">Permissions (from least to most privileged)</span></span> |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="22dbd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="22dbd-113">Delegated (work or school account)</span></span> | <span data-ttu-id="22dbd-114">User.Read, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="22dbd-114">User.Read, Directory.Read.All</span></span> |
|<span data-ttu-id="22dbd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="22dbd-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="22dbd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="22dbd-116">Not supported.</span></span> |
|<span data-ttu-id="22dbd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="22dbd-117">Application</span></span> | <span data-ttu-id="22dbd-118">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="22dbd-118">Directory.Read.All</span></span> |

> <span data-ttu-id="22dbd-119">Nota: Las aplicaciones que tienen el permiso User.Read solamente pueden leer las propiedades *id*, *displayName* y *verifiedDomains* de la organización.</span><span class="sxs-lookup"><span data-stu-id="22dbd-119">Note: Applications granted the User.Read permission are able to read only the *id*, *displayName*, and *verifiedDomains* properties of the organization.</span></span>  <span data-ttu-id="22dbd-120">El resto de propiedades devolverá valores `null`.</span><span class="sxs-lookup"><span data-stu-id="22dbd-120">All other properties will return with `null` values.</span></span> <span data-ttu-id="22dbd-121">Para leer todas las propiedades, use Directory.Read.All.</span><span class="sxs-lookup"><span data-stu-id="22dbd-121">To read all properties, use Directory.Read.All.</span></span>

## <a name="http-request"></a><span data-ttu-id="22dbd-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="22dbd-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /organization

```
## <a name="optional-query-parameters"></a><span data-ttu-id="22dbd-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="22dbd-123">Optional query parameters</span></span>
<span data-ttu-id="22dbd-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22dbd-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="22dbd-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="22dbd-125">Request headers</span></span>
| <span data-ttu-id="22dbd-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="22dbd-126">Name</span></span>       | <span data-ttu-id="22dbd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="22dbd-127">Type</span></span> | <span data-ttu-id="22dbd-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="22dbd-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="22dbd-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="22dbd-129">Authorization</span></span>  | <span data-ttu-id="22dbd-130">string</span><span class="sxs-lookup"><span data-stu-id="22dbd-130">string</span></span>  | <span data-ttu-id="22dbd-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="22dbd-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="22dbd-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="22dbd-133">Request body</span></span>
<span data-ttu-id="22dbd-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="22dbd-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="22dbd-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22dbd-135">Response</span></span>

<span data-ttu-id="22dbd-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22dbd-136">If successful, this method returns a `200 OK` response code and [organization](../resources/organization.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="22dbd-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22dbd-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="22dbd-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="22dbd-138">Request</span></span>
<span data-ttu-id="22dbd-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="22dbd-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->
```http
GET https://graph.microsoft.com/beta/organization
```
##### <a name="response"></a><span data-ttu-id="22dbd-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22dbd-140">Response</span></span>
<span data-ttu-id="22dbd-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="22dbd-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 411

{
  "assignedPlans": [
    {
      "assignedDateTime": "2016-10-19T10:37:00Z",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "servicePlanId-value"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "country": "country-value",
  "countryLetterCode": "countryLetterCode-value",
  "displayName": "displayName-value"
}
```

## <a name="see-also"></a><span data-ttu-id="22dbd-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="22dbd-144">See also</span></span>

- [<span data-ttu-id="22dbd-145">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="22dbd-145">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="22dbd-146">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="22dbd-146">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->