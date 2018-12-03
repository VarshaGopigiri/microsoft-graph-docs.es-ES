---
title: Crear inferenceClassificationOverride
description: 'Crear un reemplazo dirigidos a Bandeja de entrada para un remitente identificado por una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasifica de forma coherente '
ms.openlocfilehash: e15793bc8c7012628659144bd503bd8cf979ef61
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085933"
---
# <a name="create-inferenceclassificationoverride"></a><span data-ttu-id="26223-104">Crear inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="26223-104">Create inferenceClassificationOverride</span></span>

> <span data-ttu-id="26223-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="26223-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="26223-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="26223-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="26223-107">Crear un reemplazo [Dirigidos a Bandeja de entrada](../resources/manage-focused-inbox.md) para un remitente identificado por una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="26223-107">Create a [Focused Inbox](../resources/manage-focused-inbox.md) override for a sender identified by an SMTP address.</span></span> <span data-ttu-id="26223-108">Mensajes futuros de la que se va a clasificar coherentemente dirección SMTP como se especifica en el reemplazo.</span><span class="sxs-lookup"><span data-stu-id="26223-108">Future messages from that SMTP address will be consistently classified as specified in the override.</span></span>

<span data-ttu-id="26223-109">**Nota**</span><span class="sxs-lookup"><span data-stu-id="26223-109">**Note**</span></span>

- <span data-ttu-id="26223-110">Si ya existe una invalidación con la misma dirección SMTP, los campos **classifyAs** y **name** de esa invalidación se actualizan con los valores proporcionados.</span><span class="sxs-lookup"><span data-stu-id="26223-110">If an override already exists with the same STMP address, then the **classifyAs** and **name** fields of that override are updated with the provided values.</span></span>
- <span data-ttu-id="26223-111">El número máximo de invalidaciones que admite un buzón es de 1000, basado en direcciones SMTP de remitentes únicos.</span><span class="sxs-lookup"><span data-stu-id="26223-111">The maximum number of overrides supported for a mailbox is 1000, based on unique sender SMTP addresses.</span></span>
- <span data-ttu-id="26223-112">La operación POST solo admite la creación de invalidaciones de una en una.</span><span class="sxs-lookup"><span data-stu-id="26223-112">The POST operation supports creating only one override at a time.</span></span>

## <a name="permissions"></a><span data-ttu-id="26223-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="26223-113">Permissions</span></span>
<span data-ttu-id="26223-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="26223-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="26223-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="26223-116">Permission type</span></span>      | <span data-ttu-id="26223-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="26223-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="26223-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="26223-118">Delegated (work or school account)</span></span> | <span data-ttu-id="26223-119">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="26223-119">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="26223-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="26223-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="26223-121">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="26223-121">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="26223-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="26223-122">Application</span></span> | <span data-ttu-id="26223-123">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="26223-123">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="26223-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="26223-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/inferenceClassification/overrides
POST /users/{id}/inferenceClassification/overrides
```
## <a name="request-headers"></a><span data-ttu-id="26223-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="26223-125">Request headers</span></span>
| <span data-ttu-id="26223-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="26223-126">Name</span></span>       | <span data-ttu-id="26223-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="26223-127">Type</span></span> | <span data-ttu-id="26223-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="26223-128">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="26223-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="26223-129">Authorization</span></span>  | <span data-ttu-id="26223-130">string</span><span class="sxs-lookup"><span data-stu-id="26223-130">string</span></span>  | <span data-ttu-id="26223-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="26223-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="26223-133">Content-Type</span><span class="sxs-lookup"><span data-stu-id="26223-133">Content-Type</span></span> | <span data-ttu-id="26223-134">string</span><span class="sxs-lookup"><span data-stu-id="26223-134">string</span></span>  | <span data-ttu-id="26223-p106">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="26223-p106">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="26223-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="26223-137">Request body</span></span>
<span data-ttu-id="26223-138">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md).</span><span class="sxs-lookup"><span data-stu-id="26223-138">In the request body, supply a JSON representation of [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="26223-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26223-139">Response</span></span>

<span data-ttu-id="26223-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26223-140">If successful, this method returns `201 Created` response code and an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="26223-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="26223-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="26223-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="26223-142">Request</span></span>
<span data-ttu-id="26223-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="26223-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_inferenceclassificationoverride_from_inferenceclassification"
}-->
```http
POST https://graph.microsoft.com/beta/me/inferenceClassification/overrides
Content-type: application/json

{
  "classifyAs": "focused",
  "senderEmailAddress": {
    "name": "Samantha Booth",
    "address": "samanthab@adatum.onmicrosoft.com"
  }
}
```

##### <a name="response"></a><span data-ttu-id="26223-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26223-144">Response</span></span>
<span data-ttu-id="26223-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="26223-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.inferenceClassificationOverride"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "classifyAs": "focused",
  "senderEmailAddress": {
    "name": "Samantha Booth",
    "address": "samanthab@adatum.onmicrosoft.com"
  },
  "id": "98f5bdef-576a-404d-a2ea-07a3cf11a9b9"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create inferenceClassificationOverride",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->