---
title: 'usuario: translateExchangeIds'
description: Traducir identificadores de recursos relacionados con Outlook entre formatos.
author: dkershaw10
ms.openlocfilehash: ca8b8b1f587e545c3ebfb46efecd9c1c093a942a
ms.sourcegitcommit: 6b1ba9b3be038cd6247de54a255bad560034fe42
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27771824"
---
# <a name="user-translateexchangeids"></a><span data-ttu-id="d0243-103">usuario: translateExchangeIds</span><span class="sxs-lookup"><span data-stu-id="d0243-103">user: translateExchangeIds</span></span>

> <span data-ttu-id="d0243-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0243-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d0243-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0243-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d0243-106">Traducir identificadores de recursos relacionados con Outlook entre formatos.</span><span class="sxs-lookup"><span data-stu-id="d0243-106">Translate identifiers of Outlook-related resources between formats.</span></span>

## <a name="permissions"></a><span data-ttu-id="d0243-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d0243-107">Permissions</span></span>

<span data-ttu-id="d0243-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d0243-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="d0243-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0243-110">Permission type</span></span> | <span data-ttu-id="d0243-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0243-111">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
| <span data-ttu-id="d0243-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0243-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d0243-113">User.ReadBasic, User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0243-113">User.ReadBasic, User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All</span></span> |
| <span data-ttu-id="d0243-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0243-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d0243-115">User.ReadBasic, User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0243-115">User.ReadBasic, User.Read, User.ReadWrite</span></span> |
| <span data-ttu-id="d0243-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0243-116">Application</span></span> | <span data-ttu-id="d0243-117">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0243-117">User.Read.All, User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d0243-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0243-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/translateExchangeIds
POST /users/{id|userPrincipalName}/translateExchangeIds
```

## <a name="request-headers"></a><span data-ttu-id="d0243-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0243-119">Request headers</span></span>

| <span data-ttu-id="d0243-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d0243-120">Name</span></span> | <span data-ttu-id="d0243-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d0243-121">Value</span></span> |
|:-----|:------|
| <span data-ttu-id="d0243-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d0243-122">Authorization</span></span> | <span data-ttu-id="d0243-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d0243-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d0243-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0243-125">Request body</span></span>

| <span data-ttu-id="d0243-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d0243-126">Parameter</span></span> | <span data-ttu-id="d0243-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0243-127">Type</span></span> | <span data-ttu-id="d0243-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0243-128">Description</span></span> |
|:----------|:-----|:------------|
| <span data-ttu-id="d0243-129">inputIds</span><span class="sxs-lookup"><span data-stu-id="d0243-129">inputIds</span></span> | <span data-ttu-id="d0243-130">Colección de Edm.String</span><span class="sxs-lookup"><span data-stu-id="d0243-130">Edm.String collection</span></span> | <span data-ttu-id="d0243-131">Una colección de identificadores para convertir.</span><span class="sxs-lookup"><span data-stu-id="d0243-131">A collection of identifiers to convert.</span></span> <span data-ttu-id="d0243-132">Todos los identificadores de la colección deben tener el mismo tipo de identificador de origen y deben ser el de los elementos en el mismo buzón.</span><span class="sxs-lookup"><span data-stu-id="d0243-132">All identifiers in the collection MUST have the same source ID type, and MUST be for items in the same mailbox.</span></span> <span data-ttu-id="d0243-133">Tamaño máximo de esta colección es 1000 cadenas.</span><span class="sxs-lookup"><span data-stu-id="d0243-133">Maximum size of this collection is 1000 strings.</span></span> |
| <span data-ttu-id="d0243-134">sourceIdType</span><span class="sxs-lookup"><span data-stu-id="d0243-134">sourceIdType</span></span> | <span data-ttu-id="d0243-135">exchangeIdFormat</span><span class="sxs-lookup"><span data-stu-id="d0243-135">exchangeIdFormat</span></span> | <span data-ttu-id="d0243-136">El tipo de identificador de los identificadores en el `InputIds` parámetro.</span><span class="sxs-lookup"><span data-stu-id="d0243-136">The ID type of the identifiers in the `InputIds` parameter.</span></span> |
| <span data-ttu-id="d0243-137">targetIdType</span><span class="sxs-lookup"><span data-stu-id="d0243-137">targetIdType</span></span> | <span data-ttu-id="d0243-138">exchangeIdFormat</span><span class="sxs-lookup"><span data-stu-id="d0243-138">exchangeIdFormat</span></span> | <span data-ttu-id="d0243-139">El tipo de identificador solicitado para convertir a.</span><span class="sxs-lookup"><span data-stu-id="d0243-139">The requested ID type to convert to.</span></span> |

### <a name="exchangeidformat-values"></a><span data-ttu-id="d0243-140">valores de exchangeIdFormat</span><span class="sxs-lookup"><span data-stu-id="d0243-140">exchangeIdFormat values</span></span>

| <span data-ttu-id="d0243-141">Valores</span><span class="sxs-lookup"><span data-stu-id="d0243-141">Values</span></span> | <span data-ttu-id="d0243-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0243-142">Description</span></span> |
|:-------|:------------|
| <span data-ttu-id="d0243-143">propiedad entryId</span><span class="sxs-lookup"><span data-stu-id="d0243-143">entryId</span></span> | <span data-ttu-id="d0243-144">El formato de identificador de entrada binario utilizado por los clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="d0243-144">The binary entry ID format used by MAPI clients.</span></span> |
| <span data-ttu-id="d0243-145">ewsId</span><span class="sxs-lookup"><span data-stu-id="d0243-145">ewsId</span></span> | <span data-ttu-id="d0243-146">El formato de identificador utilizado por los clientes de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0243-146">The ID format used by Exchange Web Services clients.</span></span> |
| <span data-ttu-id="d0243-147">immutableEntryId</span><span class="sxs-lookup"><span data-stu-id="d0243-147">immutableEntryId</span></span> | <span data-ttu-id="d0243-148">El formato binario del identificador de inmutable compatible con MAPI.</span><span class="sxs-lookup"><span data-stu-id="d0243-148">The binary MAPI-compatible immutable ID format.</span></span> |
| <span data-ttu-id="d0243-149">restId</span><span class="sxs-lookup"><span data-stu-id="d0243-149">restId</span></span> | <span data-ttu-id="d0243-150">El formato de identificador predeterminado utilizado por Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="d0243-150">The default ID format used by Microsoft Graph.</span></span> |
| <span data-ttu-id="d0243-151">restImmutableEntryId</span><span class="sxs-lookup"><span data-stu-id="d0243-151">restImmutableEntryId</span></span> | <span data-ttu-id="d0243-152">El formato de identificador inmutable utilizado por Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="d0243-152">The immutable ID format used by Microsoft Graph.</span></span> |

<span data-ttu-id="d0243-153">Los formatos binarios (`entryId` y `immutableEntryId`) están con codificación base64 de seguridad de URL.</span><span class="sxs-lookup"><span data-stu-id="d0243-153">The binary formats (`entryId` and `immutableEntryId`) are URL-safe base64 encoded.</span></span> <span data-ttu-id="d0243-154">Dirección URL safeness se implementa mediante la modificación de la codificación base64 de los datos binarios de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d0243-154">URL-safeness is implemented by modifying the base64 encoding of the binary data in the following way:</span></span>

- <span data-ttu-id="d0243-155">Reemplace `+` con`-`</span><span class="sxs-lookup"><span data-stu-id="d0243-155">Replace `+` with `-`</span></span>
- <span data-ttu-id="d0243-156">Reemplace `/` con`_`</span><span class="sxs-lookup"><span data-stu-id="d0243-156">Replace `/` with `_`</span></span>
- <span data-ttu-id="d0243-157">Quitar los caracteres de relleno final (`=`)</span><span class="sxs-lookup"><span data-stu-id="d0243-157">Remove any trailing padding characters (`=`)</span></span>
- <span data-ttu-id="d0243-158">Agregar un número entero hasta el final de la cadena que indica el número de caracteres de relleno se encontraba en el original (`0`, `1`, o `2`)</span><span class="sxs-lookup"><span data-stu-id="d0243-158">Add an integer to the end of the string indicating how many padding characters were in the original (`0`, `1`, or `2`)</span></span>

## <a name="response"></a><span data-ttu-id="d0243-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0243-159">Response</span></span>

<span data-ttu-id="d0243-160">Si tiene éxito, este método devuelve `200 OK` código de respuesta y una colección de [convertIdResult](../resources/convertidresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0243-160">If successful, this method returns `200 OK` response code and a [convertIdResult](../resources/convertidresult.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d0243-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0243-161">Example</span></span>

<span data-ttu-id="d0243-162">En el ejemplo siguiente se muestra cómo convertir varios identificadores desde el formato de la API de REST normal (`restId`) para el formato inmutable REST (`restImmutableEntryId`).</span><span class="sxs-lookup"><span data-stu-id="d0243-162">The following example shows how to convert multiple identifiers from the normal REST API format (`restId`) to the REST immutable format (`restImmutableEntryId`).</span></span>

### <a name="request"></a><span data-ttu-id="d0243-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0243-163">Request</span></span>

<span data-ttu-id="d0243-164">Aquí está la solicitud de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d0243-164">Here is the example request.</span></span>
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

### <a name="response"></a><span data-ttu-id="d0243-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0243-165">Response</span></span>

<span data-ttu-id="d0243-166">Aquí está la respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0243-166">Here is the example response</span></span>
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