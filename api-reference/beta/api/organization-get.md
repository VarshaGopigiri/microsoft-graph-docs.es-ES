---
title: Get organization
description: Recupera las propiedades y relaciones de la organización actualmente autenticada.
localization_priority: Normal
ms.openlocfilehash: f8076d36c47ea9d517b43eb827d702350c364132
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826756"
---
# <a name="get-organization"></a><span data-ttu-id="a541b-103">Get organization</span><span class="sxs-lookup"><span data-stu-id="a541b-103">Get organization</span></span>

> <span data-ttu-id="a541b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a541b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a541b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a541b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a541b-106">Recupera las propiedades y relaciones de la organización actualmente autenticada.</span><span class="sxs-lookup"><span data-stu-id="a541b-106">Retrieve the properties and relationships of currently authenticated organization.</span></span>

<span data-ttu-id="a541b-107">Puesto que el recurso de la **organización** admite [extensiones](/graph/extensibility-overview), también se puede usar el `GET` operación para obtener las propiedades personalizadas y los datos de extensión en una instancia de la **organización** .</span><span class="sxs-lookup"><span data-stu-id="a541b-107">Since the **organization** resource supports [extensions](/graph/extensibility-overview), you can also use the `GET` operation to get custom properties and extension data in an **organization** instance.</span></span>

## <a name="permissions"></a><span data-ttu-id="a541b-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a541b-108">Permissions</span></span>

<span data-ttu-id="a541b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a541b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a541b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a541b-111">Permission type</span></span> | <span data-ttu-id="a541b-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a541b-112">Permissions (from least to most privileged)</span></span> |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a541b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a541b-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a541b-114">User.Read, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="a541b-114">User.Read, Directory.Read.All</span></span> |
|<span data-ttu-id="a541b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a541b-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a541b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a541b-116">Not supported.</span></span> |
|<span data-ttu-id="a541b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a541b-117">Application</span></span> | <span data-ttu-id="a541b-118">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="a541b-118">Directory.Read.All</span></span> |

> <span data-ttu-id="a541b-119">Nota: Las aplicaciones que tienen el permiso User.Read solamente pueden leer las propiedades *id*, *displayName* y *verifiedDomains* de la organización.</span><span class="sxs-lookup"><span data-stu-id="a541b-119">Note: Applications granted the User.Read permission are able to read only the *id*, *displayName*, and *verifiedDomains* properties of the organization.</span></span>  <span data-ttu-id="a541b-120">El resto de propiedades devolverá valores `null`.</span><span class="sxs-lookup"><span data-stu-id="a541b-120">All other properties will return with `null` values.</span></span> <span data-ttu-id="a541b-121">Para leer todas las propiedades, use Directory.Read.All.</span><span class="sxs-lookup"><span data-stu-id="a541b-121">To read all properties, use Directory.Read.All.</span></span>

## <a name="http-request"></a><span data-ttu-id="a541b-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a541b-122">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /organization
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a541b-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a541b-123">Optional query parameters</span></span>

<span data-ttu-id="a541b-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a541b-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a541b-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a541b-125">Request headers</span></span>

| <span data-ttu-id="a541b-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="a541b-126">Name</span></span>       | <span data-ttu-id="a541b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a541b-127">Type</span></span> | <span data-ttu-id="a541b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a541b-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a541b-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="a541b-129">Authorization</span></span>  | <span data-ttu-id="a541b-130">string</span><span class="sxs-lookup"><span data-stu-id="a541b-130">string</span></span>  | <span data-ttu-id="a541b-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a541b-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a541b-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a541b-133">Request body</span></span>

<span data-ttu-id="a541b-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a541b-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a541b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a541b-135">Response</span></span>

<span data-ttu-id="a541b-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a541b-136">If successful, this method returns a `200 OK` response code and [organization](../resources/organization.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a541b-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a541b-137">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a541b-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a541b-138">Request</span></span>

<span data-ttu-id="a541b-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a541b-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->

```http
GET https://graph.microsoft.com/beta/organization
```

##### <a name="response"></a><span data-ttu-id="a541b-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a541b-140">Response</span></span>

<span data-ttu-id="a541b-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a541b-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#organization",
  "value": [
    {
      "assignedPlans": [
        {
          "assignedDateTime": "datetime-value",
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
  ]
}
```

## <a name="see-also"></a><span data-ttu-id="a541b-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a541b-144">See also</span></span>

- [<span data-ttu-id="a541b-145">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="a541b-145">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="a541b-146">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="a541b-146">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
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
