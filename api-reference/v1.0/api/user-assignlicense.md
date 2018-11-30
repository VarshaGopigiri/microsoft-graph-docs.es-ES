---
title: assignLicense
description: Agrega o quita suscripciones del usuario. También puede habilitar y deshabilitar los planes específicos asociados a una suscripción.
ms.openlocfilehash: 93b28385296d2ef3b05b200b3b63d77369647df7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029226"
---
# <a name="assignlicense"></a><span data-ttu-id="2d3b9-104">assignLicense</span><span class="sxs-lookup"><span data-stu-id="2d3b9-104">assignLicense</span></span>
<span data-ttu-id="2d3b9-p102">Agrega o quita suscripciones del usuario. También puede habilitar y deshabilitar los planes específicos asociados a una suscripción.</span><span class="sxs-lookup"><span data-stu-id="2d3b9-p102">Add or remove subscriptions for the user. You can also enable and disable specific plans associated with a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="2d3b9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2d3b9-107">Permissions</span></span>
<span data-ttu-id="2d3b9-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2d3b9-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2d3b9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2d3b9-110">Permission type</span></span>      | <span data-ttu-id="2d3b9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2d3b9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2d3b9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2d3b9-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2d3b9-113">User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2d3b9-113">User.ReadWrite.All, Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="2d3b9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2d3b9-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2d3b9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d3b9-115">Not supported.</span></span>    |
|<span data-ttu-id="2d3b9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2d3b9-116">Application</span></span> | <span data-ttu-id="2d3b9-117">User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2d3b9-117">User.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2d3b9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d3b9-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/assignLicense
```
## <a name="request-headers"></a><span data-ttu-id="2d3b9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2d3b9-119">Request headers</span></span>
| <span data-ttu-id="2d3b9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d3b9-120">Header</span></span>       | <span data-ttu-id="2d3b9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2d3b9-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2d3b9-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2d3b9-122">Authorization</span></span>  | <span data-ttu-id="2d3b9-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2d3b9-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="2d3b9-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2d3b9-125">Content-Type</span></span>  | <span data-ttu-id="2d3b9-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2d3b9-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2d3b9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2d3b9-127">Request body</span></span>
<span data-ttu-id="2d3b9-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2d3b9-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2d3b9-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2d3b9-129">Parameter</span></span>    | <span data-ttu-id="2d3b9-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d3b9-130">Type</span></span>   |<span data-ttu-id="2d3b9-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d3b9-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2d3b9-132">addLicenses</span><span class="sxs-lookup"><span data-stu-id="2d3b9-132">addLicenses</span></span>|<span data-ttu-id="2d3b9-133">Colección de AssignedLicense</span><span class="sxs-lookup"><span data-stu-id="2d3b9-133">AssignedLicense collection</span></span>|<span data-ttu-id="2d3b9-p105">Colección de objetos [assignedLicense](../resources/assignedlicense.md) que especifican las licencias que se van a agregar. Puede deshabilitar planes asociados a una licencia estableciendo la propiedad **disabledPlans** en un objeto [assignedLicense](../resources/assignedlicense.md).</span><span class="sxs-lookup"><span data-stu-id="2d3b9-p105">A collection of [assignedLicense](../resources/assignedlicense.md) objects that specify the licenses to add. You can disable plans associated with a license by setting the **disabledPlans** property on an [assignedLicense](../resources/assignedlicense.md) object.</span></span>|
|<span data-ttu-id="2d3b9-136">removeLicenses</span><span class="sxs-lookup"><span data-stu-id="2d3b9-136">removeLicenses</span></span>|<span data-ttu-id="2d3b9-137">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="2d3b9-137">Guid collection</span></span>|<span data-ttu-id="2d3b9-138">Colección de GUID que identifican las licencias que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="2d3b9-138">A collection of GUIDs that identify the licenses to remove.</span></span>|

## <a name="response"></a><span data-ttu-id="2d3b9-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d3b9-139">Response</span></span>

<span data-ttu-id="2d3b9-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d3b9-140">If successful, this method returns `200 OK` response code and [user](../resources/user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2d3b9-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d3b9-141">Example</span></span>
<span data-ttu-id="2d3b9-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2d3b9-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2d3b9-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d3b9-143">Request</span></span>
<span data-ttu-id="2d3b9-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2d3b9-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_assignlicense"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/assignLicense
Content-type: application/json
Content-length: 185

{
  "addLicenses": [
    {
      "disabledPlans": [ "11b0131d-43c8-4bbb-b2c8-e80f9a50834a" ],
      "skuId": "guid"
    }
  ],
  "removeLicenses": [ "bea13e0c-3828-4daa-a392-28af7ff61a0f" ]
}
```

##### <a name="response"></a><span data-ttu-id="2d3b9-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d3b9-145">Response</span></span>
<span data-ttu-id="2d3b9-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2d3b9-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
  "accountEnabled": true,
  "assignedLicenses": [
    {
      "disabledPlans": [ "11b0131d-43c8-4bbb-b2c8-e80f9a50834a" ],
      "skuId": "0118A350-71FC-4EC3-8F0C-6A1CB8867561"
    }
  ],
  "assignedPlans": [
    {
      "assignedDateTime": "2016-10-02T12:13:14Z",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "bea13e0c-3828-4daa-a392-28af7ff61a0f"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "companyName": "companyName-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: assignLicense",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
