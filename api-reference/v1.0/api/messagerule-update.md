---
title: Actualizar regla
description: Cambie las propiedades modificables en un objeto messageRule y guarde los cambios.
ms.openlocfilehash: 1096006176b455052556de5f1afc1d882db8d8e1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031870"
---
# <a name="update-rule"></a><span data-ttu-id="72afc-103">Actualizar regla</span><span class="sxs-lookup"><span data-stu-id="72afc-103">Update rule</span></span>


<span data-ttu-id="72afc-104">Cambie las propiedades modificables en un objeto [messageRule](../resources/messagerule.md) y guarde los cambios.</span><span class="sxs-lookup"><span data-stu-id="72afc-104">Change writable properties on a [messageRule](../resources/messagerule.md) object and save the changes.</span></span>

## <a name="permissions"></a><span data-ttu-id="72afc-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="72afc-105">Permissions</span></span>
<span data-ttu-id="72afc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="72afc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="72afc-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="72afc-108">Permission type</span></span>      | <span data-ttu-id="72afc-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="72afc-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="72afc-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="72afc-110">Delegated (work or school account)</span></span> | <span data-ttu-id="72afc-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72afc-111">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="72afc-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="72afc-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="72afc-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72afc-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="72afc-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="72afc-114">Application</span></span> | <span data-ttu-id="72afc-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72afc-115">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="72afc-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="72afc-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailFolders/inbox/messageRules/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/inbox/messageRules/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="72afc-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="72afc-117">Optional request headers</span></span>
| <span data-ttu-id="72afc-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="72afc-118">Name</span></span>       | <span data-ttu-id="72afc-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="72afc-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="72afc-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="72afc-120">Authorization</span></span>  | <span data-ttu-id="72afc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="72afc-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="72afc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="72afc-123">Request body</span></span>
<span data-ttu-id="72afc-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="72afc-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="72afc-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72afc-127">Property</span></span>     | <span data-ttu-id="72afc-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="72afc-128">Type</span></span>   |<span data-ttu-id="72afc-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="72afc-129">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="72afc-130">actions</span><span class="sxs-lookup"><span data-stu-id="72afc-130">actions</span></span> | [<span data-ttu-id="72afc-131">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="72afc-131">messageRuleActions</span></span>](../resources/messageruleactions.md) | <span data-ttu-id="72afc-132">Acciones que se van a realizar en un mensaje cuando se cumplan las condiciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="72afc-132">Actions to be taken on a message when the corresponding conditions are fulfilled.</span></span> |
| <span data-ttu-id="72afc-133">conditions</span><span class="sxs-lookup"><span data-stu-id="72afc-133">conditions</span></span> | [<span data-ttu-id="72afc-134">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="72afc-134">messageRulePredicates</span></span>](../resources/messagerulepredicates.md) | <span data-ttu-id="72afc-135">Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla.</span><span class="sxs-lookup"><span data-stu-id="72afc-135">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> |
| <span data-ttu-id="72afc-136">displayName</span><span class="sxs-lookup"><span data-stu-id="72afc-136">displayName</span></span> | <span data-ttu-id="72afc-137">String</span><span class="sxs-lookup"><span data-stu-id="72afc-137">String</span></span> | <span data-ttu-id="72afc-138">Nombre para mostrar de la regla.</span><span class="sxs-lookup"><span data-stu-id="72afc-138">The display name of the rule.</span></span> |
| <span data-ttu-id="72afc-139">exceptions</span><span class="sxs-lookup"><span data-stu-id="72afc-139">exceptions</span></span> | [<span data-ttu-id="72afc-140">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="72afc-140">messageRulePredicates</span></span>](../resources/messagerulepredicates.md) | <span data-ttu-id="72afc-141">Condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="72afc-141">Exception conditions for the rule.</span></span> |
| <span data-ttu-id="72afc-142">isEnabled</span><span class="sxs-lookup"><span data-stu-id="72afc-142">isEnabled</span></span> | <span data-ttu-id="72afc-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="72afc-143">Boolean</span></span> | <span data-ttu-id="72afc-144">Indica si la regla está habilitada para que se aplique a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="72afc-144">Indicates whether the rule is enabled to be applied to messages.</span></span> |
| <span data-ttu-id="72afc-145">isReadOnly</span><span class="sxs-lookup"><span data-stu-id="72afc-145">isReadOnly</span></span> | <span data-ttu-id="72afc-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="72afc-146">Boolean</span></span> | <span data-ttu-id="72afc-147">Indica si la regla es de solo lectura y la API de REST de reglas no la puede modificar ni eliminar.</span><span class="sxs-lookup"><span data-stu-id="72afc-147">Indicates if the rule is read-only and cannot be modified or deleted by the rules REST API.</span></span> |
| <span data-ttu-id="72afc-148">sequence</span><span class="sxs-lookup"><span data-stu-id="72afc-148">sequence</span></span> | <span data-ttu-id="72afc-149">Int32</span><span class="sxs-lookup"><span data-stu-id="72afc-149">Int32</span></span> | <span data-ttu-id="72afc-150">Indica el orden en que se ejecuta la regla entre otras reglas.</span><span class="sxs-lookup"><span data-stu-id="72afc-150">Indicates the order in which the rule is executed, among other rules.</span></span> |


## <a name="response"></a><span data-ttu-id="72afc-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72afc-151">Response</span></span>
<span data-ttu-id="72afc-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [messageRule](../resources/messagerule.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72afc-152">If successful, this method returns a `200 OK` response code and updated [messageRule](../resources/messagerule.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="72afc-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72afc-153">Example</span></span>
##### <a name="request"></a><span data-ttu-id="72afc-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="72afc-154">Request</span></span>
<span data-ttu-id="72afc-155">En el ejemplo siguiente se cambia el nombre de la regla y las acciones que se realizan para esa regla en el [ejemplo](messagerule-get.md#example) de [Obtener regla](messagerule-get.md), desde reenviarla a una dirección hasta marcar su importancia como alta.</span><span class="sxs-lookup"><span data-stu-id="72afc-155">The following example changes the name of the rule, and the actions to be taken for that rule in the [example](messagerule-get.md#example) in [Get rule](messagerule-get.md), from forwarding to an address to marking its importance as high.</span></span> 
<!-- {
  "blockType": "request",
  "sampleKeys": ["inbox", "AQAAAJ5dZqA="],
  "name": "update_messagerule"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messageRules/AQAAAJ5dZqA=
Content-type: application/json

{
    "displayName": "Important from partner",
    "actions": {
        "markImportance": "high"
     }
} 
```
##### <a name="response"></a><span data-ttu-id="72afc-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72afc-156">Response</span></span>
<span data-ttu-id="72afc-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="72afc-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Me/mailFolders('inbox')/messageRules/$entity",
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