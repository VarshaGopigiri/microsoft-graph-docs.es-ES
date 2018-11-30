---
title: Actualizar groupLifecyclePolicy
description: Actualiza las propiedades de un objeto groupLifecyclePolicytipo de recurso groupLifecyclePolicy.
ms.openlocfilehash: 24c0540178d4cbedbfe125405bc34b58439cb5b3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029558"
---
# <a name="update-grouplifecyclepolicy"></a><span data-ttu-id="54dc4-103">Actualizar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="54dc4-103">Update groupLifecyclePolicy</span></span>

<span data-ttu-id="54dc4-104">Actualiza las propiedades de un objeto groupLifecyclePolicy[tipo de recurso groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="54dc4-104">Update the properties of a groupLifecyclePolicy[groupLifecyclePolicy resource type](../resources/grouplifecyclepolicy.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="54dc4-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="54dc4-105">Permissions</span></span>

<span data-ttu-id="54dc4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="54dc4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>
 
|<span data-ttu-id="54dc4-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54dc4-108">Permission type</span></span>      | <span data-ttu-id="54dc4-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54dc4-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="54dc4-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54dc4-110">Delegated (work or school account)</span></span> | <span data-ttu-id="54dc4-111">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="54dc4-111">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="54dc4-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54dc4-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="54dc4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54dc4-113">Not supported.</span></span>    |
|<span data-ttu-id="54dc4-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54dc4-114">Application</span></span> | <span data-ttu-id="54dc4-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="54dc4-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="54dc4-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54dc4-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groupLifecyclePolicies/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="54dc4-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="54dc4-117">Optional request headers</span></span>
| <span data-ttu-id="54dc4-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="54dc4-118">Name</span></span> | <span data-ttu-id="54dc4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="54dc4-119">Description</span></span> |
|:-----------|:-----------|
| <span data-ttu-id="54dc4-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="54dc4-120">Authorization</span></span> | <span data-ttu-id="54dc4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="54dc4-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="54dc4-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="54dc4-123">Content-Type</span></span>  | <span data-ttu-id="54dc4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="54dc4-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="54dc4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54dc4-125">Request body</span></span>

<span data-ttu-id="54dc4-126">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="54dc4-126">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="54dc4-127">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantienen los valores anteriores o se recalculan según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="54dc4-127">Existing properties that are not included in the request body maintain their previous values or are recalculated based on changes to other property values.</span></span> <span data-ttu-id="54dc4-128">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="54dc4-128">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="54dc4-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="54dc4-129">Property</span></span> | <span data-ttu-id="54dc4-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="54dc4-130">Type</span></span> | <span data-ttu-id="54dc4-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="54dc4-131">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="54dc4-132">alternateNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="54dc4-132">alternateNotificationEmails</span></span>|<span data-ttu-id="54dc4-133">String</span><span class="sxs-lookup"><span data-stu-id="54dc4-133">String</span></span>| <span data-ttu-id="54dc4-134">Lista de direcciones de correo electrónico para enviar notificaciones para grupos sin propietarios.</span><span class="sxs-lookup"><span data-stu-id="54dc4-134">List of email address to send notifications for groups without owners.</span></span> <span data-ttu-id="54dc4-135">Se pueden definir varias direcciones de correo electrónico separando una de la otra con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="54dc4-135">Multiple email address can be defined by separating email address with a semicolon.</span></span> |
|<span data-ttu-id="54dc4-136">groupLifetimeInDays</span><span class="sxs-lookup"><span data-stu-id="54dc4-136">groupLifetimeInDays</span></span>|<span data-ttu-id="54dc4-137">Int32</span><span class="sxs-lookup"><span data-stu-id="54dc4-137">Int32</span></span>| <span data-ttu-id="54dc4-138">Número de días que faltan para que un grupo expire y necesite renovarse.</span><span class="sxs-lookup"><span data-stu-id="54dc4-138">Number of days before a group expires and needs to be renewed.</span></span> <span data-ttu-id="54dc4-139">Una vez renovado, la expiración del grupo se amplía por el número de días definidos.</span><span class="sxs-lookup"><span data-stu-id="54dc4-139">Once renewed, the group expiration is extended by the number of days defined.</span></span> |
|<span data-ttu-id="54dc4-140">managedGroupTypes</span><span class="sxs-lookup"><span data-stu-id="54dc4-140">managedGroupTypes</span></span>|<span data-ttu-id="54dc4-141">String</span><span class="sxs-lookup"><span data-stu-id="54dc4-141">String</span></span>| <span data-ttu-id="54dc4-142">El tipo de grupo al que se aplica la directiva de expiración.</span><span class="sxs-lookup"><span data-stu-id="54dc4-142">The group type for which the expiration policy applies.</span></span> <span data-ttu-id="54dc4-143">Los valores posibles son **Todos**, **Seleccionados** o **Ninguno**.</span><span class="sxs-lookup"><span data-stu-id="54dc4-143">Possible values are **All**, **Selected** or **None**.</span></span> |

## <a name="response"></a><span data-ttu-id="54dc4-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54dc4-144">Response</span></span>

<span data-ttu-id="54dc4-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54dc4-145">If successful, this method returns a `200 OK` response code and updated [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="54dc4-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54dc4-146">Example</span></span>

##### <a name="request"></a><span data-ttu-id="54dc4-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54dc4-147">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_grouplifecyclepolicy"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groupLifecyclePolicies/{id}
Content-type: application/json
Content-length: 125

{
  "groupLifetimeInDays": 180,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```
##### <a name="response"></a><span data-ttu-id="54dc4-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54dc4-148">Response</span></span>
<span data-ttu-id="54dc4-149">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="54dc4-149">Note: The response object shown here may be truncated for brevity.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 146

{
  "id": "id-value",
  "groupLifetimeInDays": 180,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update groupLifecyclePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->