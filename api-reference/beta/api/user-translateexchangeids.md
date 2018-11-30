---
title: 'usuario: translateExchangeIds'
description: Traducir identificadores de recursos relacionados con Outlook entre formatos.
ms.openlocfilehash: 0c6e74ad0bb9676f261ed0202757b1e036b09c85
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087586"
---
# <a name="user-translateexchangeids"></a><span data-ttu-id="0f114-103">usuario: translateExchangeIds</span><span class="sxs-lookup"><span data-stu-id="0f114-103">user: translateExchangeIds</span></span>

> <span data-ttu-id="0f114-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0f114-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0f114-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0f114-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0f114-106">Traducir identificadores de recursos relacionados con Outlook entre formatos.</span><span class="sxs-lookup"><span data-stu-id="0f114-106">Translate identifiers of Outlook-related resources between formats.</span></span>

## <a name="permissions"></a><span data-ttu-id="0f114-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0f114-107">Permissions</span></span>

<span data-ttu-id="0f114-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0f114-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="0f114-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0f114-110">Permission type</span></span> | <span data-ttu-id="0f114-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0f114-111">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
| <span data-ttu-id="0f114-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0f114-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0f114-113">User.ReadBasic, User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0f114-113">User.ReadBasic, User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All</span></span> |
| <span data-ttu-id="0f114-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0f114-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0f114-115">User.ReadBasic, User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0f114-115">User.ReadBasic, User.Read, User.ReadWrite</span></span> |
| <span data-ttu-id="0f114-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0f114-116">Application</span></span> | <span data-ttu-id="0f114-117">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0f114-117">User.Read.All, User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0f114-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0f114-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/translateExchangeIds
POST /users/{id|userPrincipalName}/translateExchangeIds
```

## <a name="request-headers"></a><span data-ttu-id="0f114-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0f114-119">Request headers</span></span>

| <span data-ttu-id="0f114-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="0f114-120">Name</span></span> | <span data-ttu-id="0f114-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0f114-121">Value</span></span> |
|:-----|:------|
| <span data-ttu-id="0f114-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="0f114-122">Authorization</span></span> | <span data-ttu-id="0f114-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0f114-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0f114-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0f114-125">Request body</span></span>

| <span data-ttu-id="0f114-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0f114-126">Parameter</span></span> | <span data-ttu-id="0f114-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f114-127">Type</span></span> | <span data-ttu-id="0f114-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f114-128">Description</span></span> |
|:----------|:-----|:------------|
| <span data-ttu-id="0f114-129">inputIds</span><span class="sxs-lookup"><span data-stu-id="0f114-129">inputIds</span></span> | <span data-ttu-id="0f114-130">Colección de Edm.String</span><span class="sxs-lookup"><span data-stu-id="0f114-130">Edm.String collection</span></span> | <span data-ttu-id="0f114-131">Una colección de identificadores para convertir.</span><span class="sxs-lookup"><span data-stu-id="0f114-131">A collection of identifiers to convert.</span></span> <span data-ttu-id="0f114-132">Todos los identificadores de la colección deben tener el mismo tipo de identificador de origen y deben ser el de los elementos en el mismo buzón.</span><span class="sxs-lookup"><span data-stu-id="0f114-132">All identifiers in the collection MUST have the same source ID type, and MUST be for items in the same mailbox.</span></span> <span data-ttu-id="0f114-133">Tamaño máximo de esta colección es 1000 cadenas.</span><span class="sxs-lookup"><span data-stu-id="0f114-133">Maximum size of this collection is 1000 strings.</span></span> |
| <span data-ttu-id="0f114-134">sourceIdType</span><span class="sxs-lookup"><span data-stu-id="0f114-134">sourceIdType</span></span> | <span data-ttu-id="0f114-135">exchangeIdFormat</span><span class="sxs-lookup"><span data-stu-id="0f114-135">exchangeIdFormat</span></span> | <span data-ttu-id="0f114-136">El tipo de identificador de los identificadores en el `InputIds` parámetro.</span><span class="sxs-lookup"><span data-stu-id="0f114-136">The ID type of the identifiers in the `InputIds` parameter.</span></span> |
| <span data-ttu-id="0f114-137">targetIdType</span><span class="sxs-lookup"><span data-stu-id="0f114-137">targetIdType</span></span> | <span data-ttu-id="0f114-138">exchangeIdFormat</span><span class="sxs-lookup"><span data-stu-id="0f114-138">exchangeIdFormat</span></span> | <span data-ttu-id="0f114-139">El tipo de identificador solicitado para convertir a.</span><span class="sxs-lookup"><span data-stu-id="0f114-139">The requested ID type to convert to.</span></span> |

### <a name="exchangeidformat-values"></a><span data-ttu-id="0f114-140">valores de exchangeIdFormat</span><span class="sxs-lookup"><span data-stu-id="0f114-140">exchangeIdFormat values</span></span>

| <span data-ttu-id="0f114-141">Valores</span><span class="sxs-lookup"><span data-stu-id="0f114-141">Values</span></span> | <span data-ttu-id="0f114-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f114-142">Description</span></span> |
|:-------|:------------|
| <span data-ttu-id="0f114-143">propiedad entryId</span><span class="sxs-lookup"><span data-stu-id="0f114-143">entryId</span></span> | <span data-ttu-id="0f114-144">El formato de identificador de entrada binario utilizado por los clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f114-144">The binary entry ID format used by MAPI clients.</span></span> |
| <span data-ttu-id="0f114-145">ewsId</span><span class="sxs-lookup"><span data-stu-id="0f114-145">ewsId</span></span> | <span data-ttu-id="0f114-146">El formato de identificador utilizado por los clientes de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0f114-146">The ID format used by Exchange Web Services clients.</span></span> |
| <span data-ttu-id="0f114-147">immutableEntryId</span><span class="sxs-lookup"><span data-stu-id="0f114-147">immutableEntryId</span></span> | <span data-ttu-id="0f114-148">El formato de identificador inmutable compatible con MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f114-148">The MAPI-compatible immutable ID format.</span></span> |
| <span data-ttu-id="0f114-149">restId</span><span class="sxs-lookup"><span data-stu-id="0f114-149">restId</span></span> | <span data-ttu-id="0f114-150">El formato de identificador predeterminado utilizado por Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="0f114-150">The default ID format used by Microsoft Graph.</span></span> |
| <span data-ttu-id="0f114-151">restImmutableEntryId</span><span class="sxs-lookup"><span data-stu-id="0f114-151">restImmutableEntryId</span></span> | <span data-ttu-id="0f114-152">El formato de identificador inmutable utilizado por Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="0f114-152">The immutable ID format used by Microsoft Graph.</span></span> |

## <a name="response"></a><span data-ttu-id="0f114-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f114-153">Response</span></span>

<span data-ttu-id="0f114-154">Si tiene éxito, este método devuelve `200 OK` código de respuesta y una colección de [convertIdResult](../resources/meetingtimesuggestionsresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0f114-154">If successful, this method returns `200 OK` response code and a [convertIdResult](../resources/meetingtimesuggestionsresult.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0f114-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f114-155">Example</span></span>

<span data-ttu-id="0f114-156">En el ejemplo siguiente se muestra cómo convertir varios identificadores desde el formato de la API de REST normal (`restId`) para el formato inmutable REST (`restImmutableEntryId`).</span><span class="sxs-lookup"><span data-stu-id="0f114-156">The following example shows how to convert multiple identifiers from the normal REST API format (`restId`) to the REST immutable format (`restImmutableEntryId`).</span></span>

##### <a name="request"></a><span data-ttu-id="0f114-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0f114-157">Request</span></span>

<span data-ttu-id="0f114-158">Aquí está la solicitud de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0f114-158">Here is the example request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_translateexchangeids"
}-->

```http
POST https://graph.microsoft.com/beta/me/translateExchangeIds
Content-Type: application/json

{
  "inputIds" : [
    "{rest-formatted-id-1}",
    "{rest-formatted-id-2}"
  ],
  "sourceIdType": "restId",
  "targetIdType": "restImmutableEntryId"
}
```

##### <a name="response"></a><span data-ttu-id="0f114-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f114-159">Response</span></span>

<span data-ttu-id="0f114-160">Aquí está la respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f114-160">Here is the example response</span></span>
<!-- {
  "blockType": "response",
  "@odata.type": "microsoft.graph.convertIdResult",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/testexchangebeta/$metadata#Collection(microsoft.graph.convertIdResult)",
  "value": [
    {
      "sourceId": "{rest-formatted-id-1},
      "targetId": "{rest-immutable-formatted-id-1}"
    },
    {
      "sourceId": "{rest-formatted-id-2},
      "targetId": "{rest-immutable-formatted-id-2}"
    }
  ]
}
```