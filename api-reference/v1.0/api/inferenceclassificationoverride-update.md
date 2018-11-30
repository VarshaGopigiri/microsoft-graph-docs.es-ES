---
title: Actualizar inferenceclassificationoverride
description: 'Cambie el campo **classifyAs** de una invalidación tal y como se especifica. '
ms.openlocfilehash: c88b750275a1a3c52edf356ecd93a5c3ba6a3770
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030029"
---
# <a name="update-inferenceclassificationoverride"></a><span data-ttu-id="bccef-103">Actualizar inferenceclassificationoverride</span><span class="sxs-lookup"><span data-stu-id="bccef-103">Update inferenceclassificationoverride</span></span>

<span data-ttu-id="bccef-104">Cambie el campo **classifyAs** de una invalidación tal y como se especifica.</span><span class="sxs-lookup"><span data-stu-id="bccef-104">Change the **classifyAs** field of an override as specified.</span></span> 

<span data-ttu-id="bccef-105">No puede usar PATCH para cambiar ningún otro campo de una instancia [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md).</span><span class="sxs-lookup"><span data-stu-id="bccef-105">You cannot use PATCH to change any other fields in an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) instance.</span></span> 

<span data-ttu-id="bccef-106">Si hay una invalidación para un remitente y este cambia su nombre para mostrar, puede usar [POST](inferenceclassification-post-overrides.md) para forzar una actualización en el campo de nombre de la invalidación existente.</span><span class="sxs-lookup"><span data-stu-id="bccef-106">If an override exists for a sender and the sender changes his/her display name, you can use [POST](inferenceclassification-post-overrides.md) to force an update to the name field in the existing override.</span></span>

<span data-ttu-id="bccef-107">Si hay una invalidación para un remitente y este cambia su dirección SMTP, la única forma de "actualizar" la invalidación de este remitente es [eliminar](inferenceclassificationoverride-delete.md) la invalidación existente y [crear](inferenceclassification-post-overrides.md) una nueva con la nueva dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="bccef-107">If an override exists for a sender and the sender changes his/her SMTP address, [deleting](inferenceclassificationoverride-delete.md) the existing override and [creating](inferenceclassification-post-overrides.md) a new one with the new SMTP address is the only way to "update" the override for this sender.</span></span>

## <a name="permissions"></a><span data-ttu-id="bccef-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="bccef-108">Permissions</span></span>
<span data-ttu-id="bccef-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bccef-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bccef-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bccef-111">Permission type</span></span>      | <span data-ttu-id="bccef-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bccef-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bccef-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bccef-113">Delegated (work or school account)</span></span> | <span data-ttu-id="bccef-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bccef-114">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="bccef-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bccef-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bccef-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bccef-116">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="bccef-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bccef-117">Application</span></span> | <span data-ttu-id="bccef-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bccef-118">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="bccef-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bccef-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/inferenceClassification/overrides/{id}
PATCH /users/{id}/inferenceClassification/overrides/{id}
```

## <a name="request-headers"></a><span data-ttu-id="bccef-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bccef-120">Request headers</span></span>
| <span data-ttu-id="bccef-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="bccef-121">Name</span></span>       | <span data-ttu-id="bccef-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="bccef-122">Type</span></span> | <span data-ttu-id="bccef-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="bccef-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="bccef-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="bccef-124">Authorization</span></span>  | <span data-ttu-id="bccef-125">string</span><span class="sxs-lookup"><span data-stu-id="bccef-125">string</span></span>  | <span data-ttu-id="bccef-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bccef-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bccef-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="bccef-128">Content-Type</span></span> | <span data-ttu-id="bccef-129">string</span><span class="sxs-lookup"><span data-stu-id="bccef-129">string</span></span>  | <span data-ttu-id="bccef-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bccef-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bccef-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bccef-132">Request body</span></span>
<span data-ttu-id="bccef-p104">En el cuerpo de la solicitud, proporcione el nuevo valor de **classifyAs**. Para obtener el mejor rendimiento, no debe incluir valores existentes que no cambien.</span><span class="sxs-lookup"><span data-stu-id="bccef-p104">In the request body, supply the new value for **classifyAs**. For best performance you shouldn't include existing values that are not changing.</span></span>

| <span data-ttu-id="bccef-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bccef-135">Property</span></span>     | <span data-ttu-id="bccef-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="bccef-136">Type</span></span>   |<span data-ttu-id="bccef-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="bccef-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bccef-138">classifyAs</span><span class="sxs-lookup"><span data-stu-id="bccef-138">classifyAs</span></span>|<span data-ttu-id="bccef-139">string</span><span class="sxs-lookup"><span data-stu-id="bccef-139">string</span></span>| <span data-ttu-id="bccef-140">Especifica cómo los mensajes entrantes de una determinada siempre debe clasificarse como remitente.</span><span class="sxs-lookup"><span data-stu-id="bccef-140">Specifies how incoming messages from a specific sender should always be classified as.</span></span> <span data-ttu-id="bccef-141">Los valores posibles son: `focused`, `other`.</span><span class="sxs-lookup"><span data-stu-id="bccef-141">The possible values are: `focused`, `other`.</span></span>|

## <a name="response"></a><span data-ttu-id="bccef-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bccef-142">Response</span></span>

<span data-ttu-id="bccef-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bccef-143">If successful, this method returns a `200 OK` response code and updated [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bccef-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bccef-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bccef-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bccef-145">Request</span></span>
<span data-ttu-id="bccef-146">En el ejemplo siguiente, se cambia la invalidación de la dirección SMTP randiw@adatum.onmicrosoft.com de `other` a `focused`.</span><span class="sxs-lookup"><span data-stu-id="bccef-146">The following example changes the override for the SMTP address randiw@adatum.onmicrosoft.com from `other` to `focused`.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_inferenceclassificationoverride"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides/{id}
Content-type: application/json

{
  "classifyAs": "focused"
}
```
##### <a name="response"></a><span data-ttu-id="bccef-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bccef-147">Response</span></span>
<span data-ttu-id="bccef-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bccef-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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