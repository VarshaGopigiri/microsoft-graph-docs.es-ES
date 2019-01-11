---
title: Crear inferenceClassificationOverride
description: 'Crear un reemplazo para un remitente identificado por una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasifica de forma coherente '
localization_priority: Normal
ms.openlocfilehash: 37648d699d4d54b2995af6bf847347c6537a414d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848695"
---
# <a name="create-inferenceclassificationoverride"></a><span data-ttu-id="74093-104">Crear inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="74093-104">Create inferenceClassificationOverride</span></span>

<span data-ttu-id="74093-p102">Cree una invalidación para un remitente que se ha identificado mediante una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasificarán sistemáticamente como se especifica en la invalidación.</span><span class="sxs-lookup"><span data-stu-id="74093-p102">Create an override for a sender identified by an SMTP address. Future messages from that SMTP address will be consistently classified as specified in the override.</span></span>

<span data-ttu-id="74093-107">**Nota**</span><span class="sxs-lookup"><span data-stu-id="74093-107">**Note**</span></span>

- <span data-ttu-id="74093-108">Si ya existe una invalidación con la misma dirección SMTP, los campos **classifyAs** y **name** de esa invalidación se actualizan con los valores proporcionados.</span><span class="sxs-lookup"><span data-stu-id="74093-108">If an override already exists with the same STMP address, then the **classifyAs** and **name** fields of that override are updated with the provided values.</span></span>
- <span data-ttu-id="74093-109">El número máximo de invalidaciones que admite un buzón es de 1000, basado en direcciones SMTP de remitentes únicos.</span><span class="sxs-lookup"><span data-stu-id="74093-109">The maximum number of overrides supported for a mailbox is 1000, based on unique sender SMTP addresses.</span></span>
- <span data-ttu-id="74093-110">La operación POST solo admite la creación de invalidaciones de una en una.</span><span class="sxs-lookup"><span data-stu-id="74093-110">The POST operation supports creating only one override at a time.</span></span>

## <a name="permissions"></a><span data-ttu-id="74093-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="74093-111">Permissions</span></span>
<span data-ttu-id="74093-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="74093-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="74093-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74093-114">Permission type</span></span>      | <span data-ttu-id="74093-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74093-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="74093-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74093-116">Delegated (work or school account)</span></span> | <span data-ttu-id="74093-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="74093-117">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="74093-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74093-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="74093-119">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="74093-119">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="74093-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74093-120">Application</span></span> | <span data-ttu-id="74093-121">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="74093-121">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="74093-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74093-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/inferenceClassification/overrides
POST /users/{id}/inferenceClassification/overrides
```
## <a name="request-headers"></a><span data-ttu-id="74093-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74093-123">Request headers</span></span>
| <span data-ttu-id="74093-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="74093-124">Name</span></span>       | <span data-ttu-id="74093-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="74093-125">Type</span></span> | <span data-ttu-id="74093-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="74093-126">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="74093-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="74093-127">Authorization</span></span>  | <span data-ttu-id="74093-128">string</span><span class="sxs-lookup"><span data-stu-id="74093-128">string</span></span>  | <span data-ttu-id="74093-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="74093-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="74093-131">Content-Type</span><span class="sxs-lookup"><span data-stu-id="74093-131">Content-Type</span></span> | <span data-ttu-id="74093-132">string</span><span class="sxs-lookup"><span data-stu-id="74093-132">string</span></span>  | <span data-ttu-id="74093-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="74093-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="74093-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74093-135">Request body</span></span>
<span data-ttu-id="74093-136">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md).</span><span class="sxs-lookup"><span data-stu-id="74093-136">In the request body, supply a JSON representation of [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="74093-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74093-137">Response</span></span>

<span data-ttu-id="74093-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74093-138">If successful, this method returns `201 Created` response code and an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74093-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74093-139">Example</span></span>
##### <a name="request"></a><span data-ttu-id="74093-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74093-140">Request</span></span>
<span data-ttu-id="74093-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74093-141">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="74093-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74093-142">Response</span></span>
<span data-ttu-id="74093-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74093-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
