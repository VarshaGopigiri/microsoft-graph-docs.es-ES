---
title: Crear regla
description: 'Crear un objeto messageRule especificando un conjunto de condiciones y acciones. '
ms.openlocfilehash: f725aa0a078938cf111782aedf1feb041a5a0e19
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090901"
---
# <a name="create-rule"></a><span data-ttu-id="787db-103">Crear regla</span><span class="sxs-lookup"><span data-stu-id="787db-103">Create rule</span></span>

> <span data-ttu-id="787db-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="787db-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="787db-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="787db-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="787db-106">Crear un objeto [messageRule](../resources/messagerule.md) especificando un conjunto de condiciones y acciones.</span><span class="sxs-lookup"><span data-stu-id="787db-106">Create a [messageRule](../resources/messagerule.md) object by specifying a set of conditions and actions.</span></span> 

<span data-ttu-id="787db-107">Outlook lleva a cabo esas acciones si un mensaje entrante en la Bandeja de entrada del usuario cumple las condiciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="787db-107">Outlook carries out those actions if an incoming message in the user's Inbox meets the specified conditions.</span></span>

## <a name="permissions"></a><span data-ttu-id="787db-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="787db-108">Permissions</span></span>
<span data-ttu-id="787db-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="787db-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="787db-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="787db-111">Permission type</span></span>      | <span data-ttu-id="787db-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="787db-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="787db-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="787db-113">Delegated (work or school account)</span></span> | <span data-ttu-id="787db-114">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="787db-114">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="787db-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="787db-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="787db-116">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="787db-116">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="787db-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="787db-117">Application</span></span> | <span data-ttu-id="787db-118">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="787db-118">MailboxSettings.ReadWrite</span></span> |


## <a name="http-request"></a><span data-ttu-id="787db-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="787db-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/inbox/messagerules
POST /users/{id | userPrincipalName}/mailFolders/inbox/messagerules
```
## <a name="request-headers"></a><span data-ttu-id="787db-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="787db-120">Request headers</span></span>
| <span data-ttu-id="787db-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="787db-121">Name</span></span>       | <span data-ttu-id="787db-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="787db-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="787db-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="787db-123">Authorization</span></span>  | <span data-ttu-id="787db-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="787db-p103">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="787db-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="787db-126">Request body</span></span>
<span data-ttu-id="787db-127">En el cuerpo de la solicitud, proporcione los parámetros que se aplican a la regla.</span><span class="sxs-lookup"><span data-stu-id="787db-127">In the request body, supply the parameters that are applicable to your rule.</span></span> <span data-ttu-id="787db-128">Estos son los parámetros de cuerpo que suelen usarse al crear reglas.</span><span class="sxs-lookup"><span data-stu-id="787db-128">The following are body parameters that are typically used when creating rules.</span></span> <span data-ttu-id="787db-129">Puede especificar cualquier otra propiedad **messageRule** modificable que corresponda en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="787db-129">You can specify any other writable **messageRule** properties as appropriate in the request body.</span></span>

| <span data-ttu-id="787db-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="787db-130">Parameter</span></span>       | <span data-ttu-id="787db-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="787db-131">Type</span></span>|<span data-ttu-id="787db-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="787db-132">Description</span></span>|
|:--------|:-------|:----------|
|<span data-ttu-id="787db-133">actions</span><span class="sxs-lookup"><span data-stu-id="787db-133">actions</span></span>|[<span data-ttu-id="787db-134">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="787db-134">messageRuleActions</span></span>](../resources/messageruleactions.md)|<span data-ttu-id="787db-135">Acciones que se van a realizar en un mensaje cuando las condiciones correspondientes, si las hubiera, se cumplan.</span><span class="sxs-lookup"><span data-stu-id="787db-135">Actions to be taken on a message when the corresponding conditions, if any, are fulfilled.</span></span> <span data-ttu-id="787db-136">Necesario.</span><span class="sxs-lookup"><span data-stu-id="787db-136">Required.</span></span>|
|<span data-ttu-id="787db-137">conditions</span><span class="sxs-lookup"><span data-stu-id="787db-137">conditions</span></span>|[<span data-ttu-id="787db-138">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="787db-138">messageRulePredicates</span></span>](../resources/messagerulepredicates.md)|<span data-ttu-id="787db-139">Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla.</span><span class="sxs-lookup"><span data-stu-id="787db-139">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> <span data-ttu-id="787db-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="787db-140">Optional.</span></span>|
|<span data-ttu-id="787db-141">displayName</span><span class="sxs-lookup"><span data-stu-id="787db-141">displayName</span></span>| <span data-ttu-id="787db-142">String</span><span class="sxs-lookup"><span data-stu-id="787db-142">String</span></span>  | <span data-ttu-id="787db-143">Nombre para mostrar de la regla.</span><span class="sxs-lookup"><span data-stu-id="787db-143">The display name of the rule.</span></span> <span data-ttu-id="787db-144">Necesario.</span><span class="sxs-lookup"><span data-stu-id="787db-144">Required.</span></span>|
|<span data-ttu-id="787db-145">exceptions</span><span class="sxs-lookup"><span data-stu-id="787db-145">exceptions</span></span>| [<span data-ttu-id="787db-146">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="787db-146">messageRulePredicates</span></span>](../resources/messagerulepredicates.md)| <span data-ttu-id="787db-147">Representa las condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="787db-147">Represents exception conditions for the rule.</span></span> <span data-ttu-id="787db-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="787db-148">Optional.</span></span> |
|<span data-ttu-id="787db-149">isEnabled</span><span class="sxs-lookup"><span data-stu-id="787db-149">isEnabled</span></span> | <span data-ttu-id="787db-150">Boolean</span><span class="sxs-lookup"><span data-stu-id="787db-150">Boolean</span></span> | <span data-ttu-id="787db-151">Indica si la regla está habilitada para que se aplique a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="787db-151">Indicates whether the rule is enabled to be applied to messages.</span></span> <span data-ttu-id="787db-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="787db-152">Optional.</span></span> |
|<span data-ttu-id="787db-153">sequence</span><span class="sxs-lookup"><span data-stu-id="787db-153">sequence</span></span>| <span data-ttu-id="787db-154">Int32</span><span class="sxs-lookup"><span data-stu-id="787db-154">Int32</span></span> | <span data-ttu-id="787db-155">Indica el orden en que se ejecuta la regla entre otras reglas.</span><span class="sxs-lookup"><span data-stu-id="787db-155">Indicates the order in which the rule is executed, among other rules.</span></span> <span data-ttu-id="787db-156">Necesario.</span><span class="sxs-lookup"><span data-stu-id="787db-156">Required.</span></span>|

## <a name="response"></a><span data-ttu-id="787db-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="787db-157">Response</span></span>
<span data-ttu-id="787db-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto **messageRule** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="787db-158">If successful, this method returns `201 Created` response code and a **messageRule** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="787db-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="787db-159">Example</span></span>
##### <a name="request"></a><span data-ttu-id="787db-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="787db-160">Request</span></span>
<span data-ttu-id="787db-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="787db-161">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_messagerule_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/beta/me/mailFolders/inbox/messagerules
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
##### <a name="response"></a><span data-ttu-id="787db-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="787db-162">Response</span></span>
<span data-ttu-id="787db-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="787db-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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