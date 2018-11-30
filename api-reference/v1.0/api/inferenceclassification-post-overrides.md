---
title: Crear inferenceClassificationOverride
description: 'Crear un reemplazo para un remitente identificado por una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasifica de forma coherente '
ms.openlocfilehash: f068984598ce841b2e7af52c1ed1d25c0e101d10
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031949"
---
# <a name="create-inferenceclassificationoverride"></a><span data-ttu-id="ab3cb-104">Crear inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="ab3cb-104">Create inferenceClassificationOverride</span></span>

<span data-ttu-id="ab3cb-p102">Cree una invalidación para un remitente que se ha identificado mediante una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasificarán sistemáticamente como se especifica en la invalidación.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-p102">Create an override for a sender identified by an SMTP address. Future messages from that SMTP address will be consistently classified as specified in the override.</span></span>

<span data-ttu-id="ab3cb-107">**Nota**</span><span class="sxs-lookup"><span data-stu-id="ab3cb-107">**Note**</span></span>

- <span data-ttu-id="ab3cb-108">Si ya existe una invalidación con la misma dirección SMTP, los campos **classifyAs** y **name** de esa invalidación se actualizan con los valores proporcionados.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-108">If an override already exists with the same STMP address, then the **classifyAs** and **name** fields of that override are updated with the provided values.</span></span>
- <span data-ttu-id="ab3cb-109">El número máximo de invalidaciones que admite un buzón es de 1000, basado en direcciones SMTP de remitentes únicos.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-109">The maximum number of overrides supported for a mailbox is 1000, based on unique sender SMTP addresses.</span></span>
- <span data-ttu-id="ab3cb-110">La operación POST solo admite la creación de invalidaciones de una en una.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-110">The POST operation supports creating only one override at a time.</span></span>

## <a name="permissions"></a><span data-ttu-id="ab3cb-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="ab3cb-111">Permissions</span></span>
<span data-ttu-id="ab3cb-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ab3cb-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ab3cb-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ab3cb-114">Permission type</span></span>      | <span data-ttu-id="ab3cb-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ab3cb-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ab3cb-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ab3cb-116">Delegated (work or school account)</span></span> | <span data-ttu-id="ab3cb-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ab3cb-117">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ab3cb-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ab3cb-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ab3cb-119">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ab3cb-119">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ab3cb-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab3cb-120">Application</span></span> | <span data-ttu-id="ab3cb-121">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ab3cb-121">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ab3cb-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ab3cb-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/inferenceClassification/overrides
POST /users/{id}/inferenceClassification/overrides
```
## <a name="request-headers"></a><span data-ttu-id="ab3cb-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ab3cb-123">Request headers</span></span>
| <span data-ttu-id="ab3cb-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="ab3cb-124">Name</span></span>       | <span data-ttu-id="ab3cb-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab3cb-125">Type</span></span> | <span data-ttu-id="ab3cb-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab3cb-126">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ab3cb-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="ab3cb-127">Authorization</span></span>  | <span data-ttu-id="ab3cb-128">string</span><span class="sxs-lookup"><span data-stu-id="ab3cb-128">string</span></span>  | <span data-ttu-id="ab3cb-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ab3cb-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ab3cb-131">Content-Type</span></span> | <span data-ttu-id="ab3cb-132">string</span><span class="sxs-lookup"><span data-stu-id="ab3cb-132">string</span></span>  | <span data-ttu-id="ab3cb-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ab3cb-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ab3cb-135">Request body</span></span>
<span data-ttu-id="ab3cb-136">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md).</span><span class="sxs-lookup"><span data-stu-id="ab3cb-136">In the request body, supply a JSON representation of [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="ab3cb-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab3cb-137">Response</span></span>

<span data-ttu-id="ab3cb-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-138">If successful, this method returns `201 Created` response code and an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ab3cb-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab3cb-139">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ab3cb-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab3cb-140">Request</span></span>
<span data-ttu-id="ab3cb-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_inferenceclassificationoverride_from_inferenceclassification"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides
Content-type: application/json

{
  "classifyAs": "focused",
  "senderEmailAddress": {
    "name": "Samantha Booth",
    "address": "samanthab@adatum.onmicrosoft.com"
  }
}
```

##### <a name="response"></a><span data-ttu-id="ab3cb-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab3cb-142">Response</span></span>
<span data-ttu-id="ab3cb-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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