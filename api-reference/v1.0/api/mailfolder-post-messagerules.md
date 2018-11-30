---
title: Crear regla
description: 'Crear un objeto messageRule especificando un conjunto de condiciones y acciones. '
ms.openlocfilehash: fdea3920e272581c8d08e04c01c385575e6c6df1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030377"
---
# <a name="create-rule"></a><span data-ttu-id="a5e8e-103">Crear regla</span><span class="sxs-lookup"><span data-stu-id="a5e8e-103">Create rule</span></span>


<span data-ttu-id="a5e8e-104">Crear un objeto [messageRule](../resources/messagerule.md) especificando un conjunto de condiciones y acciones.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-104">Create a [messageRule](../resources/messagerule.md) object by specifying a set of conditions and actions.</span></span> 

<span data-ttu-id="a5e8e-105">Outlook lleva a cabo esas acciones si un mensaje entrante en la Bandeja de entrada del usuario cumple las condiciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-105">Outlook carries out those actions if an incoming message in the user's Inbox meets the specified conditions.</span></span>

## <a name="permissions"></a><span data-ttu-id="a5e8e-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="a5e8e-106">Permissions</span></span>
<span data-ttu-id="a5e8e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5e8e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5e8e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5e8e-109">Permission type</span></span>      | <span data-ttu-id="a5e8e-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5e8e-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a5e8e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5e8e-111">Delegated (work or school account)</span></span> | <span data-ttu-id="a5e8e-112">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a5e8e-112">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="a5e8e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5e8e-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a5e8e-114">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a5e8e-114">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="a5e8e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5e8e-115">Application</span></span> | <span data-ttu-id="a5e8e-116">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a5e8e-116">MailboxSettings.ReadWrite</span></span> |


## <a name="http-request"></a><span data-ttu-id="a5e8e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5e8e-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/inbox/messageRules
POST /users/{id | userPrincipalName}/mailFolders/inbox/messageRules
```
## <a name="request-headers"></a><span data-ttu-id="a5e8e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5e8e-118">Request headers</span></span>
| <span data-ttu-id="a5e8e-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="a5e8e-119">Name</span></span>       | <span data-ttu-id="a5e8e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5e8e-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a5e8e-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5e8e-121">Authorization</span></span>  | <span data-ttu-id="a5e8e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="a5e8e-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5e8e-124">Request body</span></span>
<span data-ttu-id="a5e8e-125">En el cuerpo de la solicitud, proporcione los parámetros que se aplican a la regla.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-125">In the request body, supply the parameters that are applicable to your rule.</span></span> <span data-ttu-id="a5e8e-126">Estos son los parámetros de cuerpo que suelen usarse al crear reglas.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-126">The following are body parameters that are typically used when creating rules.</span></span> <span data-ttu-id="a5e8e-127">Puede especificar cualquier otra propiedad **messageRule** modificable que corresponda en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-127">You can specify any other writable **messageRule** properties as appropriate in the request body.</span></span>

| <span data-ttu-id="a5e8e-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="a5e8e-128">Name</span></span>       | <span data-ttu-id="a5e8e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5e8e-129">Type</span></span>|<span data-ttu-id="a5e8e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5e8e-130">Description</span></span>|
|:--------|:-------|:----------|
|<span data-ttu-id="a5e8e-131">actions</span><span class="sxs-lookup"><span data-stu-id="a5e8e-131">actions</span></span>|[<span data-ttu-id="a5e8e-132">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="a5e8e-132">messageRuleActions</span></span>](../resources/messageruleactions.md)|<span data-ttu-id="a5e8e-133">Acciones que se van a realizar en un mensaje cuando las condiciones correspondientes, si las hubiera, se cumplan.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-133">Actions to be taken on a message when the corresponding conditions, if any, are fulfilled.</span></span> <span data-ttu-id="a5e8e-134">Necesario.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-134">Required.</span></span>|
|<span data-ttu-id="a5e8e-135">conditions</span><span class="sxs-lookup"><span data-stu-id="a5e8e-135">conditions</span></span>|[<span data-ttu-id="a5e8e-136">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="a5e8e-136">messageRulePredicates</span></span>](../resources/messagerulepredicates.md)|<span data-ttu-id="a5e8e-137">Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-137">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> <span data-ttu-id="a5e8e-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-138">Optional.</span></span>|
|<span data-ttu-id="a5e8e-139">displayName</span><span class="sxs-lookup"><span data-stu-id="a5e8e-139">displayName</span></span>| <span data-ttu-id="a5e8e-140">String</span><span class="sxs-lookup"><span data-stu-id="a5e8e-140">String</span></span>  | <span data-ttu-id="a5e8e-141">Nombre para mostrar de la regla.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-141">The display name of the rule.</span></span> <span data-ttu-id="a5e8e-142">Necesario.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-142">Required.</span></span>|
|<span data-ttu-id="a5e8e-143">exceptions</span><span class="sxs-lookup"><span data-stu-id="a5e8e-143">exceptions</span></span>| [<span data-ttu-id="a5e8e-144">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="a5e8e-144">messageRulePredicates</span></span>](../resources/messagerulepredicates.md)| <span data-ttu-id="a5e8e-145">Representa las condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-145">Represents exception conditions for the rule.</span></span> <span data-ttu-id="a5e8e-146">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-146">Optional.</span></span> |
|<span data-ttu-id="a5e8e-147">isEnabled</span><span class="sxs-lookup"><span data-stu-id="a5e8e-147">isEnabled</span></span> | <span data-ttu-id="a5e8e-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="a5e8e-148">Boolean</span></span> | <span data-ttu-id="a5e8e-149">Indica si la regla está habilitada para que se aplique a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-149">Indicates whether the rule is enabled to be applied to messages.</span></span> <span data-ttu-id="a5e8e-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-150">Optional.</span></span> |
|<span data-ttu-id="a5e8e-151">sequence</span><span class="sxs-lookup"><span data-stu-id="a5e8e-151">sequence</span></span>| <span data-ttu-id="a5e8e-152">Int32</span><span class="sxs-lookup"><span data-stu-id="a5e8e-152">Int32</span></span> | <span data-ttu-id="a5e8e-153">Indica el orden en que se ejecuta la regla entre otras reglas.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-153">Indicates the order in which the rule is executed, among other rules.</span></span> <span data-ttu-id="a5e8e-154">Necesario.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-154">Required.</span></span>|

## <a name="response"></a><span data-ttu-id="a5e8e-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5e8e-155">Response</span></span>
<span data-ttu-id="a5e8e-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto **messageRule** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-156">If successful, this method returns `201 Created` response code and a **messageRule** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a5e8e-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5e8e-157">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a5e8e-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5e8e-158">Request</span></span>
<span data-ttu-id="a5e8e-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-159">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["inbox"],
  "name": "create_messagerule_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messageRules
Content-type: application/json

{      
    "displayName": "From partner",      
    "sequence": 2,      
    "isEnabled": true,          
    "conditions": {
        "senderContains": [
          "adele"       
        ]
     },
     "actions": {
        "forwardTo": [
          {
             "emailAddress": {
                "name": "Alex Wilbur",
                "address": "AlexW@contoso.onmicrosoft.com"
              }
           }
        ],
        "stopProcessingRules": true
     }    
}

```
##### <a name="response"></a><span data-ttu-id="a5e8e-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5e8e-160">Response</span></span>
<span data-ttu-id="a5e8e-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a5e8e-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id":"AQAAAJ5dZqA=",
  "displayName":"From partner",
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
      "stopProcessingRules":true,
      "forwardTo":[
        {
          "emailAddress":{
            "name":"Alex Wilbur",
            "address":"AlexW@contoso.onmicrosoft.com"
          }
        }
      ]
  }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->