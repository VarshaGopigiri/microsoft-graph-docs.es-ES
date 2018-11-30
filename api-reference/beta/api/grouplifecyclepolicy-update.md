---
title: Actualizar groupLifecyclePolicy
description: Actualiza las propiedades de un objeto groupLifecyclePolicytipo de recurso groupLifecyclePolicy.
ms.openlocfilehash: 0cfea79762b6c15f4f710ae515a262fe56350471
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083298"
---
# <a name="update-grouplifecyclepolicy"></a><span data-ttu-id="2bfe0-103">Actualizar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="2bfe0-103">Update groupLifecyclePolicy</span></span>

> <span data-ttu-id="2bfe0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2bfe0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2bfe0-106">Actualiza las propiedades de un objeto groupLifecyclePolicy[tipo de recurso groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2bfe0-106">Update the properties of a groupLifecyclePolicy[groupLifecyclePolicy resource type](../resources/grouplifecyclepolicy.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="2bfe0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2bfe0-107">Permissions</span></span>

<span data-ttu-id="2bfe0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2bfe0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>
 

|<span data-ttu-id="2bfe0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2bfe0-110">Permission type</span></span>      | <span data-ttu-id="2bfe0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2bfe0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2bfe0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2bfe0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2bfe0-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2bfe0-113">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="2bfe0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2bfe0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2bfe0-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="2bfe0-115">Not supported</span></span> |
|<span data-ttu-id="2bfe0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2bfe0-116">Application</span></span> | <span data-ttu-id="2bfe0-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2bfe0-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2bfe0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2bfe0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groupLifecyclePolicies/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="2bfe0-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="2bfe0-119">Optional request headers</span></span>
| <span data-ttu-id="2bfe0-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2bfe0-120">Name</span></span> | <span data-ttu-id="2bfe0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bfe0-121">Description</span></span> |
|:-----------|:-----------|
| <span data-ttu-id="2bfe0-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2bfe0-122">Authorization</span></span> | <span data-ttu-id="2bfe0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2bfe0-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2bfe0-125">Content-Type</span></span>  | <span data-ttu-id="2bfe0-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2bfe0-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2bfe0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2bfe0-127">Request body</span></span>

<span data-ttu-id="2bfe0-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="2bfe0-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2bfe0-131">Property</span></span> | <span data-ttu-id="2bfe0-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="2bfe0-132">Type</span></span> | <span data-ttu-id="2bfe0-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bfe0-133">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="2bfe0-134">alternateNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="2bfe0-134">alternateNotificationEmails</span></span>|<span data-ttu-id="2bfe0-135">String</span><span class="sxs-lookup"><span data-stu-id="2bfe0-135">String</span></span>| <span data-ttu-id="2bfe0-136">Lista de direcciones de correo electrónico para enviar notificaciones para grupos sin propietarios.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-136">List of email address to send notifications for groups without owners.</span></span> <span data-ttu-id="2bfe0-137">Se pueden definir varias direcciones de correo electrónico separando una de la otra con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-137">Multiple email address can be defined by separating email address with a semicolon.</span></span> |
|<span data-ttu-id="2bfe0-138">groupLifetimeInDays</span><span class="sxs-lookup"><span data-stu-id="2bfe0-138">groupLifetimeInDays</span></span>|<span data-ttu-id="2bfe0-139">Int32</span><span class="sxs-lookup"><span data-stu-id="2bfe0-139">Int32</span></span>| <span data-ttu-id="2bfe0-140">Número de días que faltan para que un grupo expire y necesite renovarse.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-140">Number of days before a group expires and needs to be renewed.</span></span> <span data-ttu-id="2bfe0-141">Una vez renovado, la expiración del grupo se amplía por el número de días definidos.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-141">Once renewed, the group expiration is extended by the number of days defined.</span></span> |
|<span data-ttu-id="2bfe0-142">managedGroupTypes</span><span class="sxs-lookup"><span data-stu-id="2bfe0-142">managedGroupTypes</span></span>|<span data-ttu-id="2bfe0-143">String</span><span class="sxs-lookup"><span data-stu-id="2bfe0-143">String</span></span>| <span data-ttu-id="2bfe0-144">El tipo de grupo al que se aplica la directiva de expiración.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-144">The group type for which the expiration policy applies.</span></span> <span data-ttu-id="2bfe0-145">Los valores posibles son **Todos**, **Seleccionados** o **Ninguno**.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-145">Possible values are **All**, **Selected** or **None**.</span></span> |

## <a name="response"></a><span data-ttu-id="2bfe0-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bfe0-146">Response</span></span>

<span data-ttu-id="2bfe0-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-147">If successful, this method returns a `200 OK` response code and updated [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2bfe0-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2bfe0-148">Example</span></span>

##### <a name="request"></a><span data-ttu-id="2bfe0-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2bfe0-149">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_grouplifecyclepolicy"
}-->
```http
PATCH https://graph.microsoft.com/beta/groupLifecyclePolicies/{id}
Content-type: application/json
Content-length: 151

{
  "groupLifetimeInDays": 180,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```
##### <a name="response"></a><span data-ttu-id="2bfe0-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bfe0-150">Response</span></span>
<span data-ttu-id="2bfe0-151">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="2bfe0-151">Note: The response object shown here may be truncated for brevity.</span></span> 
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