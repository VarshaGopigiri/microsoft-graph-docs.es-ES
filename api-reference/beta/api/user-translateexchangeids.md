---
title: 'usuario: translateExchangeIds'
description: Traducir identificadores de recursos relacionados con Outlook entre formatos.
author: dkershaw10
ms.openlocfilehash: 6dd18fe041c2a303be4ad333b8beeaef168682b1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360581"
---
# <a name="user-translateexchangeids"></a><span data-ttu-id="3892c-103">usuario: translateExchangeIds</span><span class="sxs-lookup"><span data-stu-id="3892c-103">user: translateExchangeIds</span></span>

> <span data-ttu-id="3892c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3892c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3892c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3892c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3892c-106">Traducir identificadores de recursos relacionados con Outlook entre formatos.</span><span class="sxs-lookup"><span data-stu-id="3892c-106">Translate identifiers of Outlook-related resources between formats.</span></span>

## <a name="permissions"></a><span data-ttu-id="3892c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3892c-107">Permissions</span></span>

<span data-ttu-id="3892c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3892c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="3892c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3892c-110">Permission type</span></span> | <span data-ttu-id="3892c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3892c-111">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
| <span data-ttu-id="3892c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3892c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3892c-113">User.ReadBasic, User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3892c-113">User.ReadBasic, User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All</span></span> |
| <span data-ttu-id="3892c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3892c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3892c-115">User.ReadBasic, User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3892c-115">User.ReadBasic, User.Read, User.ReadWrite</span></span> |
| <span data-ttu-id="3892c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3892c-116">Application</span></span> | <span data-ttu-id="3892c-117">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3892c-117">User.Read.All, User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3892c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3892c-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/translateExchangeIds
POST /users/{id|userPrincipalName}/translateExchangeIds
```

## <a name="request-headers"></a><span data-ttu-id="3892c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3892c-119">Request headers</span></span>

| <span data-ttu-id="3892c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3892c-120">Name</span></span> | <span data-ttu-id="3892c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3892c-121">Value</span></span> |
|:-----|:------|
| <span data-ttu-id="3892c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3892c-122">Authorization</span></span> | <span data-ttu-id="3892c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3892c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3892c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3892c-125">Request body</span></span>

| <span data-ttu-id="3892c-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3892c-126">Parameter</span></span> | <span data-ttu-id="3892c-127">Type</span><span class="sxs-lookup"><span data-stu-id="3892c-127">Type</span></span> | <span data-ttu-id="3892c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="3892c-128">Description</span></span> |
|:----------|:-----|:------------|
| <span data-ttu-id="3892c-129">inputIds</span><span class="sxs-lookup"><span data-stu-id="3892c-129">inputIds</span></span> | <span data-ttu-id="3892c-130">Colección de Edm.String</span><span class="sxs-lookup"><span data-stu-id="3892c-130">Edm.String collection</span></span> | <span data-ttu-id="3892c-131">Una colección de identificadores para convertir.</span><span class="sxs-lookup"><span data-stu-id="3892c-131">A collection of identifiers to convert.</span></span> <span data-ttu-id="3892c-132">Todos los identificadores de la colección deben tener el mismo tipo de identificador de origen y deben ser el de los elementos en el mismo buzón.</span><span class="sxs-lookup"><span data-stu-id="3892c-132">All identifiers in the collection MUST have the same source ID type, and MUST be for items in the same mailbox.</span></span> <span data-ttu-id="3892c-133">Tamaño máximo de esta colección es 1000 cadenas.</span><span class="sxs-lookup"><span data-stu-id="3892c-133">Maximum size of this collection is 1000 strings.</span></span> |
| <span data-ttu-id="3892c-134">sourceIdType</span><span class="sxs-lookup"><span data-stu-id="3892c-134">sourceIdType</span></span> | <span data-ttu-id="3892c-135">exchangeIdFormat</span><span class="sxs-lookup"><span data-stu-id="3892c-135">exchangeIdFormat</span></span> | <span data-ttu-id="3892c-136">El tipo de identificador de los identificadores en el `InputIds` parámetro.</span><span class="sxs-lookup"><span data-stu-id="3892c-136">The ID type of the identifiers in the `InputIds` parameter.</span></span> |
| <span data-ttu-id="3892c-137">targetIdType</span><span class="sxs-lookup"><span data-stu-id="3892c-137">targetIdType</span></span> | <span data-ttu-id="3892c-138">exchangeIdFormat</span><span class="sxs-lookup"><span data-stu-id="3892c-138">exchangeIdFormat</span></span> | <span data-ttu-id="3892c-139">El tipo de identificador solicitado para convertir a.</span><span class="sxs-lookup"><span data-stu-id="3892c-139">The requested ID type to convert to.</span></span> |

### <a name="exchangeidformat-values"></a><span data-ttu-id="3892c-140">valores de exchangeIdFormat</span><span class="sxs-lookup"><span data-stu-id="3892c-140">exchangeIdFormat values</span></span>

| <span data-ttu-id="3892c-141">Valores</span><span class="sxs-lookup"><span data-stu-id="3892c-141">Values</span></span> | <span data-ttu-id="3892c-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="3892c-142">Description</span></span> |
|:-------|:------------|
| <span data-ttu-id="3892c-143">propiedad entryId</span><span class="sxs-lookup"><span data-stu-id="3892c-143">entryId</span></span> | <span data-ttu-id="3892c-144">El formato de identificador de entrada binario utilizado por los clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="3892c-144">The binary entry ID format used by MAPI clients.</span></span> |
| <span data-ttu-id="3892c-145">ewsId</span><span class="sxs-lookup"><span data-stu-id="3892c-145">ewsId</span></span> | <span data-ttu-id="3892c-146">El formato de identificador utilizado por los clientes de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3892c-146">The ID format used by Exchange Web Services clients.</span></span> |
| <span data-ttu-id="3892c-147">immutableEntryId</span><span class="sxs-lookup"><span data-stu-id="3892c-147">immutableEntryId</span></span> | <span data-ttu-id="3892c-148">El formato de identificador inmutable compatible con MAPI.</span><span class="sxs-lookup"><span data-stu-id="3892c-148">The MAPI-compatible immutable ID format.</span></span> |
| <span data-ttu-id="3892c-149">restId</span><span class="sxs-lookup"><span data-stu-id="3892c-149">restId</span></span> | <span data-ttu-id="3892c-150">El formato de identificador predeterminado utilizado por Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3892c-150">The default ID format used by Microsoft Graph.</span></span> |
| <span data-ttu-id="3892c-151">restImmutableEntryId</span><span class="sxs-lookup"><span data-stu-id="3892c-151">restImmutableEntryId</span></span> | <span data-ttu-id="3892c-152">El formato de identificador inmutable utilizado por Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3892c-152">The immutable ID format used by Microsoft Graph.</span></span> |

## <a name="response"></a><span data-ttu-id="3892c-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3892c-153">Response</span></span>

<span data-ttu-id="3892c-154">Si tiene éxito, este método devuelve `200 OK` código de respuesta y una colección de [convertIdResult](../resources/convertidresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3892c-154">If successful, this method returns `200 OK` response code and a [convertIdResult](../resources/convertidresult.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3892c-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3892c-155">Example</span></span>

<span data-ttu-id="3892c-156">En el ejemplo siguiente se muestra cómo convertir varios identificadores desde el formato de la API de REST normal (`restId`) para el formato inmutable REST (`restImmutableEntryId`).</span><span class="sxs-lookup"><span data-stu-id="3892c-156">The following example shows how to convert multiple identifiers from the normal REST API format (`restId`) to the REST immutable format (`restImmutableEntryId`).</span></span>

##### <a name="request"></a><span data-ttu-id="3892c-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3892c-157">Request</span></span>

<span data-ttu-id="3892c-158">Aquí está la solicitud de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3892c-158">Here is the example request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="3892c-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3892c-159">Response</span></span>

<span data-ttu-id="3892c-160">Aquí está la respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3892c-160">Here is the example response</span></span>
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