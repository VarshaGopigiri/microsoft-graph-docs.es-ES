---
title: Actualizar inferenceClassificationOverride
description: 'Cambiar el campo **classifyAs** de una bandeja de entrada dirigidos a invalidar tal como se especifica. '
ms.openlocfilehash: 696b3826bf09d3e0f706a3c3fdfba620e416ef22
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090215"
---
# <a name="update-inferenceclassificationoverride"></a><span data-ttu-id="acde5-103">Actualizar inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="acde5-103">Update inferenceClassificationOverride</span></span>

> <span data-ttu-id="acde5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="acde5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="acde5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="acde5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="acde5-106">Cambiar el campo **classifyAs** de una [Bandeja de entrada dirigidos a](../resources/manage-focused-inbox.md) invalidar tal como se especifica.</span><span class="sxs-lookup"><span data-stu-id="acde5-106">Change the **classifyAs** field of a [Focused Inbox](../resources/manage-focused-inbox.md) override as specified.</span></span> 

<span data-ttu-id="acde5-107">No puede usar PATCH para cambiar ningún otro campo de una instancia [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md).</span><span class="sxs-lookup"><span data-stu-id="acde5-107">You cannot use PATCH to change any other fields in an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) instance.</span></span> 

<span data-ttu-id="acde5-108">Si hay una invalidación para un remitente y este cambia su nombre para mostrar, puede usar [POST](inferenceclassification-post-overrides.md) para forzar una actualización en el campo de nombre de la invalidación existente.</span><span class="sxs-lookup"><span data-stu-id="acde5-108">If an override exists for a sender and the sender changes his/her display name, you can use [POST](inferenceclassification-post-overrides.md) to force an update to the name field in the existing override.</span></span>

<span data-ttu-id="acde5-109">Si hay una invalidación para un remitente y este cambia su dirección SMTP, la única forma de "actualizar" la invalidación de este remitente es [eliminar](inferenceclassificationoverride-delete.md) la invalidación existente y [crear](inferenceclassification-post-overrides.md) una nueva con la nueva dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="acde5-109">If an override exists for a sender and the sender changes his/her SMTP address, [deleting](inferenceclassificationoverride-delete.md) the existing override and [creating](inferenceclassification-post-overrides.md) a new one with the new SMTP address is the only way to "update" the override for this sender.</span></span>

## <a name="permissions"></a><span data-ttu-id="acde5-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="acde5-110">Permissions</span></span>
<span data-ttu-id="acde5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="acde5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="acde5-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="acde5-113">Permission type</span></span>      | <span data-ttu-id="acde5-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="acde5-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="acde5-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="acde5-115">Delegated (work or school account)</span></span> | <span data-ttu-id="acde5-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="acde5-116">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="acde5-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="acde5-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="acde5-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="acde5-118">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="acde5-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="acde5-119">Application</span></span> | <span data-ttu-id="acde5-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="acde5-120">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="acde5-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="acde5-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/inferenceClassification/overrides/{id}
PATCH /users/{id}/inferenceClassification/overrides/{id}
```

## <a name="request-headers"></a><span data-ttu-id="acde5-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="acde5-122">Request headers</span></span>
| <span data-ttu-id="acde5-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="acde5-123">Name</span></span>       | <span data-ttu-id="acde5-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="acde5-124">Type</span></span> | <span data-ttu-id="acde5-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="acde5-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="acde5-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="acde5-126">Authorization</span></span>  | <span data-ttu-id="acde5-127">string</span><span class="sxs-lookup"><span data-stu-id="acde5-127">string</span></span>  | <span data-ttu-id="acde5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="acde5-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="acde5-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="acde5-130">Content-Type</span></span> | <span data-ttu-id="acde5-131">string</span><span class="sxs-lookup"><span data-stu-id="acde5-131">string</span></span>  | <span data-ttu-id="acde5-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="acde5-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="acde5-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="acde5-134">Request body</span></span>
<span data-ttu-id="acde5-p105">En el cuerpo de la solicitud, proporcione el nuevo valor de **classifyAs**. Para obtener el mejor rendimiento, no debe incluir valores existentes que no cambien.</span><span class="sxs-lookup"><span data-stu-id="acde5-p105">In the request body, supply the new value for **classifyAs**. For best performance you shouldn't include existing values that are not changing.</span></span>

| <span data-ttu-id="acde5-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="acde5-137">Property</span></span>     | <span data-ttu-id="acde5-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="acde5-138">Type</span></span>   |<span data-ttu-id="acde5-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="acde5-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="acde5-140">classifyAs</span><span class="sxs-lookup"><span data-stu-id="acde5-140">classifyAs</span></span>|<span data-ttu-id="acde5-141">string</span><span class="sxs-lookup"><span data-stu-id="acde5-141">string</span></span>| <span data-ttu-id="acde5-p106">Especifica cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado. Los valores posibles son: `focused`, `other`.</span><span class="sxs-lookup"><span data-stu-id="acde5-p106">Specifies how incoming messages from a specific sender should always be classified as. Possible values are: `focused`, `other`.</span></span>|

## <a name="response"></a><span data-ttu-id="acde5-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="acde5-144">Response</span></span>

<span data-ttu-id="acde5-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="acde5-145">If successful, this method returns a `200 OK` response code and updated [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="acde5-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="acde5-146">Example</span></span>
##### <a name="request"></a><span data-ttu-id="acde5-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="acde5-147">Request</span></span>
<span data-ttu-id="acde5-148">En el ejemplo siguiente, se cambia la invalidación de la dirección SMTP randiw@adatum.onmicrosoft.com de `other` a `focused`.</span><span class="sxs-lookup"><span data-stu-id="acde5-148">The following example changes the override for the SMTP address randiw@adatum.onmicrosoft.com from `other` to `focused`.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_inferenceclassificationoverride"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/inferenceClassification/overrides/{id}
Content-type: application/json

{
  "classifyAs": "focused"
}
```
##### <a name="response"></a><span data-ttu-id="acde5-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="acde5-149">Response</span></span>
<span data-ttu-id="acde5-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="acde5-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.inferenceClassificationOverride"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "classifyAs": "focused",
  "senderEmailAddress": {
    "name": "Randi Welch",
    "address": "randiw@adatum.onmicrosoft.com"
  },
  "id": "98f5bdef-576a-404d-a2ea-07a3cf34af4r"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update inferenceclassificationoverride",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->