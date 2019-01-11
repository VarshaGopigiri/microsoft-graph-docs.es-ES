---
title: Actualizar regla
description: Cambie las propiedades modificables en un objeto messageRule y guarde los cambios.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 3b034c7c428821c23b92d78644b43de9d7a2946d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886362"
---
# <a name="update-rule"></a><span data-ttu-id="13bda-103">Actualizar regla</span><span class="sxs-lookup"><span data-stu-id="13bda-103">Update rule</span></span>

> <span data-ttu-id="13bda-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="13bda-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="13bda-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="13bda-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="13bda-106">Cambie las propiedades modificables en un objeto [messageRule](../resources/messagerule.md) y guarde los cambios.</span><span class="sxs-lookup"><span data-stu-id="13bda-106">Change writable properties on a [messageRule](../resources/messagerule.md) object and save the changes.</span></span>

## <a name="permissions"></a><span data-ttu-id="13bda-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="13bda-107">Permissions</span></span>
<span data-ttu-id="13bda-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="13bda-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="13bda-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="13bda-110">Permission type</span></span>      | <span data-ttu-id="13bda-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="13bda-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="13bda-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="13bda-112">Delegated (work or school account)</span></span> | <span data-ttu-id="13bda-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="13bda-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="13bda-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="13bda-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="13bda-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="13bda-115">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="13bda-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="13bda-116">Application</span></span> | <span data-ttu-id="13bda-117">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="13bda-117">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="13bda-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="13bda-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailFolders/inbox/messagerules/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/inbox/messagerules/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="13bda-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="13bda-119">Optional request headers</span></span>
| <span data-ttu-id="13bda-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="13bda-120">Name</span></span>       | <span data-ttu-id="13bda-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="13bda-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="13bda-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="13bda-122">Authorization</span></span>  | <span data-ttu-id="13bda-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="13bda-p103">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="13bda-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="13bda-125">Request body</span></span>
<span data-ttu-id="13bda-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="13bda-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="13bda-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="13bda-129">Property</span></span>     | <span data-ttu-id="13bda-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="13bda-130">Type</span></span>   |<span data-ttu-id="13bda-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="13bda-131">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="13bda-132">actions</span><span class="sxs-lookup"><span data-stu-id="13bda-132">actions</span></span> | [<span data-ttu-id="13bda-133">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="13bda-133">messageRuleActions</span></span>](../resources/messageruleactions.md) | <span data-ttu-id="13bda-134">Acciones que se van a realizar en un mensaje cuando se cumplan las condiciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="13bda-134">Actions to be taken on a message when the corresponding conditions are fulfilled.</span></span> |
| <span data-ttu-id="13bda-135">conditions</span><span class="sxs-lookup"><span data-stu-id="13bda-135">conditions</span></span> | [<span data-ttu-id="13bda-136">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="13bda-136">messageRulePredicates</span></span>](../resources/messagerulepredicates.md) | <span data-ttu-id="13bda-137">Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla.</span><span class="sxs-lookup"><span data-stu-id="13bda-137">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> |
| <span data-ttu-id="13bda-138">displayName</span><span class="sxs-lookup"><span data-stu-id="13bda-138">displayName</span></span> | <span data-ttu-id="13bda-139">String</span><span class="sxs-lookup"><span data-stu-id="13bda-139">String</span></span> | <span data-ttu-id="13bda-140">Nombre para mostrar de la regla.</span><span class="sxs-lookup"><span data-stu-id="13bda-140">The display name of the rule.</span></span> |
| <span data-ttu-id="13bda-141">exceptions</span><span class="sxs-lookup"><span data-stu-id="13bda-141">exceptions</span></span> | [<span data-ttu-id="13bda-142">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="13bda-142">messageRulePredicates</span></span>](../resources/messagerulepredicates.md) | <span data-ttu-id="13bda-143">Condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="13bda-143">Exception conditions for the rule.</span></span> |
| <span data-ttu-id="13bda-144">isEnabled</span><span class="sxs-lookup"><span data-stu-id="13bda-144">isEnabled</span></span> | <span data-ttu-id="13bda-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="13bda-145">Boolean</span></span> | <span data-ttu-id="13bda-146">Indica si la regla está habilitada para que se aplique a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="13bda-146">Indicates whether the rule is enabled to be applied to messages.</span></span> |
| <span data-ttu-id="13bda-147">isReadOnly</span><span class="sxs-lookup"><span data-stu-id="13bda-147">isReadOnly</span></span> | <span data-ttu-id="13bda-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="13bda-148">Boolean</span></span> | <span data-ttu-id="13bda-149">Indica si la regla es de solo lectura y la API de REST de reglas no la puede modificar ni eliminar.</span><span class="sxs-lookup"><span data-stu-id="13bda-149">Indicates if the rule is read-only and cannot be modified or deleted by the rules REST API.</span></span> |
| <span data-ttu-id="13bda-150">sequence</span><span class="sxs-lookup"><span data-stu-id="13bda-150">sequence</span></span> | <span data-ttu-id="13bda-151">Int32</span><span class="sxs-lookup"><span data-stu-id="13bda-151">Int32</span></span> | <span data-ttu-id="13bda-152">Indica el orden en que se ejecuta la regla entre otras reglas.</span><span class="sxs-lookup"><span data-stu-id="13bda-152">Indicates the order in which the rule is executed, among other rules.</span></span> |


## <a name="response"></a><span data-ttu-id="13bda-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13bda-153">Response</span></span>
<span data-ttu-id="13bda-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [messageRule](../resources/messagerule.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13bda-154">If successful, this method returns a `200 OK` response code and updated [messageRule](../resources/messagerule.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="13bda-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="13bda-155">Example</span></span>
##### <a name="request"></a><span data-ttu-id="13bda-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="13bda-156">Request</span></span>
<span data-ttu-id="13bda-157">En el ejemplo siguiente se cambia el nombre de la regla y las acciones que se realizan para esa regla en el [ejemplo](messagerule-get.md#example) de [Obtener regla](messagerule-get.md), desde reenviarla a una dirección hasta marcar su importancia como alta.</span><span class="sxs-lookup"><span data-stu-id="13bda-157">The following example changes the name of the rule, and the actions to be taken for that rule in the [example](messagerule-get.md#example) in [Get rule](messagerule-get.md), from forwarding to an address to marking its importance as high.</span></span> 
<!-- {
  "blockType": "request",
  "name": "update_messagerule"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/mailfolders/inbox/messagerules('AQAAAJ5dZqA=')

Content-type: application/json

{
    "displayName": "Important from partner",
    "actions": {
        "markImportance": "high"
     }
} 
```
##### <a name="response"></a><span data-ttu-id="13bda-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13bda-158">Response</span></span>
<span data-ttu-id="13bda-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="13bda-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#Me/mailFolders('inbox')/messageRules/$entity",
  "id":"AQAAAJ5dZqA=",
  "displayName":"Important from partner",
  "sequence":2,
  "isEnabled":true,
  "hasError":false,
  "isReadOnly":false,
  "conditions":{
    "senderContains":[
      "ADELE"
    ]
  },
  "actions":{
    "markImportance": "high"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
