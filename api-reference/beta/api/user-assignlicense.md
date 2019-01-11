---
title: assignLicense
description: Agregar o quitar licencias para el usuario habilitar o deshabilitar el uso de las ofertas de nube de Microsoft. Por ejemplo, una organización puede tener una suscripción a Office 365 Enterprise E3 con 100 licencias, y esta solicitud de una de las licencias asigna a un usuario determinado. También puede habilitar y deshabilitar planes específicos asociados a una suscripción. Para obtener más información acerca de las suscripciones y las licencias, consulte este artículo de Technet.
localization_priority: Normal
ms.openlocfilehash: 71287b47a0a42ce4f89635fe6a1769c78874ae36
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876205"
---
# <a name="assignlicense"></a><span data-ttu-id="4d788-106">assignLicense</span><span class="sxs-lookup"><span data-stu-id="4d788-106">assignLicense</span></span>

> <span data-ttu-id="4d788-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4d788-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4d788-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4d788-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4d788-109">Agregar o quitar licencias para el usuario habilitar o deshabilitar el uso de las ofertas de nube de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4d788-109">Add or remove licenses for the user to enable or disable their use of Microsoft cloud offerings.</span></span> <span data-ttu-id="4d788-110">Por ejemplo, una organización puede tener una suscripción a Office 365 Enterprise E3 con 100 licencias, y esta solicitud de una de las licencias asigna a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="4d788-110">For example, an organization can have an Office 365 Enterprise E3 subscription with 100 licenses, and this request assigns one of those licenses to a specific user.</span></span> <span data-ttu-id="4d788-111">También puede habilitar y deshabilitar planes específicos asociados a una suscripción.</span><span class="sxs-lookup"><span data-stu-id="4d788-111">You can also enable and disable specific plans associated with a subscription.</span></span> <span data-ttu-id="4d788-112">Para obtener más información acerca de las suscripciones y las licencias, vea este [artículo de Technet](https://technet.microsoft.com/en-us/library/mt765146.aspx).</span><span class="sxs-lookup"><span data-stu-id="4d788-112">To learn more about subscriptions and licenses, see this [Technet article](https://technet.microsoft.com/en-us/library/mt765146.aspx).</span></span>

<span data-ttu-id="4d788-113">Para obtener las suscripciones disponibles en el directorio, lleve a cabo una [solicitud de subscribedSkus](subscribedsku-list.md).</span><span class="sxs-lookup"><span data-stu-id="4d788-113">To get the subscriptions available in the directory, perform a [GET subscribedSkus request](subscribedsku-list.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="4d788-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="4d788-114">Permissions</span></span>
<span data-ttu-id="4d788-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4d788-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4d788-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d788-117">Permission type</span></span>      | <span data-ttu-id="4d788-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d788-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4d788-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d788-119">Delegated (work or school account)</span></span> | <span data-ttu-id="4d788-120">User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4d788-120">User.ReadWrite.All, Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="4d788-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d788-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4d788-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d788-122">Not supported.</span></span>    |
|<span data-ttu-id="4d788-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d788-123">Application</span></span> | <span data-ttu-id="4d788-124">User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4d788-124">User.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4d788-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d788-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/assignLicense
```
## <a name="request-headers"></a><span data-ttu-id="4d788-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d788-126">Request headers</span></span>
| <span data-ttu-id="4d788-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d788-127">Header</span></span>       | <span data-ttu-id="4d788-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4d788-128">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4d788-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d788-129">Authorization</span></span>  | <span data-ttu-id="4d788-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4d788-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="4d788-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4d788-132">Content-Type</span></span>  | <span data-ttu-id="4d788-133">application/json</span><span class="sxs-lookup"><span data-stu-id="4d788-133">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4d788-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d788-134">Request body</span></span>
<span data-ttu-id="4d788-135">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4d788-135">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4d788-136">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4d788-136">Parameter</span></span>    | <span data-ttu-id="4d788-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d788-137">Type</span></span>   |<span data-ttu-id="4d788-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d788-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4d788-139">addLicenses</span><span class="sxs-lookup"><span data-stu-id="4d788-139">addLicenses</span></span>|<span data-ttu-id="4d788-140">Colección [assignedLicense](../resources/assignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="4d788-140">[assignedLicense](../resources/assignedlicense.md) collection</span></span>|<span data-ttu-id="4d788-141">Una colección de objetos [assignedLicense](../resources/assignedlicense.md) que especifican las licencias para agregar.</span><span class="sxs-lookup"><span data-stu-id="4d788-141">A collection of [assignedLicense](../resources/assignedlicense.md) objects that specify the licenses to add.</span></span> <span data-ttu-id="4d788-142">Puede deshabilitar servicePlans asociado con una licencia estableciendo la propiedad **disabledPlans** en un objeto [assignedLicense](../resources/assignedlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="4d788-142">You can disable servicePlans associated with a license by setting the **disabledPlans** property on an [assignedLicense](../resources/assignedlicense.md) object.</span></span>|
|<span data-ttu-id="4d788-143">removeLicenses</span><span class="sxs-lookup"><span data-stu-id="4d788-143">removeLicenses</span></span>|<span data-ttu-id="4d788-144">Guid</span><span class="sxs-lookup"><span data-stu-id="4d788-144">Guid</span></span>|<span data-ttu-id="4d788-145">Una colección de skuIds que identifican las licencias para quitar.</span><span class="sxs-lookup"><span data-stu-id="4d788-145">A collection of skuIds that identify the licenses to remove.</span></span>|

## <a name="response"></a><span data-ttu-id="4d788-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d788-146">Response</span></span>

<span data-ttu-id="4d788-147">Si tiene éxito, este método devuelve `200 OK` código de respuesta y un objeto de [usuario](../resources/user.md) de actualizada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d788-147">If successful, this method returns `200 OK` response code and an updated [user](../resources/user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4d788-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d788-148">Example</span></span>
<span data-ttu-id="4d788-149">Agregar licencias para el usuario.</span><span class="sxs-lookup"><span data-stu-id="4d788-149">Add licenses to the user.</span></span>
##### <a name="request"></a><span data-ttu-id="4d788-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d788-150">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "user_assignlicense"
}-->
```http
POST https://graph.microsoft.com/beta/me/assignLicense
Content-type: application/json
Content-length: 185

{
  "addLicenses": [
    {
      "disabledPlans": [ "11b0131d-43c8-4bbb-b2c8-e80f9a50834a" ],
      "skuId": "skuId-value-1"
    },
    {
      "disabledPlans": [ "a571ebcc-fqe0-4ca2-8c8c-7a284fd6c235" ],
      "skuId": "skuId-value-2"
    }
  ],
  "removeLicenses": []
}
```

## <a name="example"></a><span data-ttu-id="4d788-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d788-151">Example</span></span>
<span data-ttu-id="4d788-152">Quitar licencias de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d788-152">Remove licenses from the user.</span></span>

#####<a name="request"></a><span data-ttu-id="4d788-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d788-153">Request</span></span>
```http
POST https://graph.microsoft.com/beta/me/assignLicense
Content-type: application/json
Content-length: 185

{
  "addLicenses": [],
  "removeLicenses": ["skuId-value-1", "skuId-value-2"]
}
```

##### <a name="response"></a><span data-ttu-id="4d788-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d788-154">Response</span></span>
<span data-ttu-id="4d788-155">En ambos ejemplos, la respuesta es el objeto de usuario actualizada.</span><span class="sxs-lookup"><span data-stu-id="4d788-155">In both examples, the response is the updated user object.</span></span> <span data-ttu-id="4d788-156">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="4d788-156">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="4d788-157">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4d788-157">All of the properties will be returned from an actual call.</span></span>
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
      "skuId": "skuId-value"
    }
  ],
  "assignedPlans": [
    {
      "assignedDateTime": "2016-10-19T10:37:00Z",
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
