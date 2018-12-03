---
title: Crear contrato
description: Crear un nuevo objeto de contrato.
ms.openlocfilehash: bfcab53b4233d133309c99a4825e184a42670458
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084372"
---
# <a name="create-agreement"></a><span data-ttu-id="c0a66-103">Crear contrato</span><span class="sxs-lookup"><span data-stu-id="c0a66-103">Create agreement</span></span>

> <span data-ttu-id="c0a66-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c0a66-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c0a66-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c0a66-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c0a66-106">Crear un nuevo objeto de [contrato](../resources/agreement.md) .</span><span class="sxs-lookup"><span data-stu-id="c0a66-106">Create a new [agreement](../resources/agreement.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c0a66-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c0a66-107">Permissions</span></span>
<span data-ttu-id="c0a66-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0a66-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c0a66-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c0a66-110">Permission type</span></span>                        | <span data-ttu-id="c0a66-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c0a66-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="c0a66-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c0a66-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="c0a66-113">Agreement.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c0a66-113">Agreement.ReadWrite.All</span></span> |
|<span data-ttu-id="c0a66-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0a66-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0a66-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0a66-115">Not supported.</span></span> |
|<span data-ttu-id="c0a66-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c0a66-116">Application</span></span>                            | <span data-ttu-id="c0a66-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0a66-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c0a66-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0a66-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /agreements
```
## <a name="request-headers"></a><span data-ttu-id="c0a66-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0a66-119">Request headers</span></span>
| <span data-ttu-id="c0a66-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c0a66-120">Name</span></span>         | <span data-ttu-id="c0a66-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0a66-121">Type</span></span>        | <span data-ttu-id="c0a66-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0a66-122">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="c0a66-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c0a66-123">Authorization</span></span> | <span data-ttu-id="c0a66-124">string</span><span class="sxs-lookup"><span data-stu-id="c0a66-124">string</span></span> | <span data-ttu-id="c0a66-125">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="c0a66-125">Bearer \{token\}.</span></span> <span data-ttu-id="c0a66-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0a66-126">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c0a66-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0a66-127">Request body</span></span>
<span data-ttu-id="c0a66-128">En el cuerpo de la solicitud, proporcionar una representación JSON de objeto de [acuerdo](../resources/agreement.md) .</span><span class="sxs-lookup"><span data-stu-id="c0a66-128">In the request body, supply a JSON representation of [agreement](../resources/agreement.md) object.</span></span>

<span data-ttu-id="c0a66-129">En la tabla siguiente, se muestran las propiedades necesarias al crear un usuario.</span><span class="sxs-lookup"><span data-stu-id="c0a66-129">The following table shows the properties that are required when you create a user.</span></span>

| <span data-ttu-id="c0a66-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c0a66-130">Property</span></span>     | <span data-ttu-id="c0a66-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0a66-131">Type</span></span>        | <span data-ttu-id="c0a66-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0a66-132">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="c0a66-133">displayName</span><span class="sxs-lookup"><span data-stu-id="c0a66-133">displayName</span></span>|<span data-ttu-id="c0a66-134">String</span><span class="sxs-lookup"><span data-stu-id="c0a66-134">String</span></span>|<span data-ttu-id="c0a66-135">Nombre para mostrar del contrato.</span><span class="sxs-lookup"><span data-stu-id="c0a66-135">Display name of the agreement.</span></span>|
|<span data-ttu-id="c0a66-136">isViewingBeforeAcceptanceRequired</span><span class="sxs-lookup"><span data-stu-id="c0a66-136">isViewingBeforeAcceptanceRequired</span></span>|<span data-ttu-id="c0a66-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="c0a66-137">Boolean</span></span>|<span data-ttu-id="c0a66-138">Indica si el usuario tiene que expandir y ver el contrato antes de Aceptar.</span><span class="sxs-lookup"><span data-stu-id="c0a66-138">Indicates whether the user has to expand and view the agreement before accepting.</span></span>|
|<span data-ttu-id="c0a66-139">archivos/nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="c0a66-139">files/fileName</span></span>|<span data-ttu-id="c0a66-140">String</span><span class="sxs-lookup"><span data-stu-id="c0a66-140">String</span></span>|<span data-ttu-id="c0a66-141">Nombre del archivo de contrato (por ejemplo, TOU.pdf).</span><span class="sxs-lookup"><span data-stu-id="c0a66-141">Name of the agreement file (for example, TOU.pdf).</span></span>|
|<span data-ttu-id="c0a66-142">archivos/isDefault</span><span class="sxs-lookup"><span data-stu-id="c0a66-142">files/isDefault</span></span>|<span data-ttu-id="c0a66-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="c0a66-143">Boolean</span></span>|<span data-ttu-id="c0a66-144">Indica si este es el archivo del contrato de forma predeterminada si ninguno de la referencia cultural coincide con la preferencia de cliente.</span><span class="sxs-lookup"><span data-stu-id="c0a66-144">Indicates whether this is the default agreement file if none of the culture matches the client preference.</span></span> <span data-ttu-id="c0a66-145">Si ninguno de los archivos se marca como predeterminada, el primero de ellos se tratará como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c0a66-145">If none of the file is marked as default, the first one will be treated as default.</span></span>|
|<span data-ttu-id="c0a66-146">los archivos y el idioma</span><span class="sxs-lookup"><span data-stu-id="c0a66-146">files/language</span></span>|<span data-ttu-id="c0a66-147">String</span><span class="sxs-lookup"><span data-stu-id="c0a66-147">String</span></span>|<span data-ttu-id="c0a66-148">Referencia cultural del archivo de contrato en el formato languagecode2-país/regioncode2.</span><span class="sxs-lookup"><span data-stu-id="c0a66-148">Culture of the agreement file in the format languagecode2-country/regioncode2.</span></span> <span data-ttu-id="c0a66-149">languagecode2 es un código de dos letras en minúsculas proveniente de ISO 639-1.</span><span class="sxs-lookup"><span data-stu-id="c0a66-149">languagecode2 is a lowercase two-letter code derived from ISO 639-1.</span></span> <span data-ttu-id="c0a66-150">país/regioncode2 se deriva de ISO 3166 y normalmente consta de dos letras en mayúsculas, o una etiqueta de idioma BCP 47 (por ejemplo, en-US).</span><span class="sxs-lookup"><span data-stu-id="c0a66-150">country/regioncode2 is derived from ISO 3166 and usually consists of two uppercase letters, or a BCP-47 language tag (for example, en-US).</span></span>|
|<span data-ttu-id="c0a66-151">archivos, fileData/datos</span><span class="sxs-lookup"><span data-stu-id="c0a66-151">files/fileData/data</span></span>|<span data-ttu-id="c0a66-152">Binario</span><span class="sxs-lookup"><span data-stu-id="c0a66-152">Binary</span></span>|<span data-ttu-id="c0a66-153">Datos que representan las condiciones de uso del documento PDF.</span><span class="sxs-lookup"><span data-stu-id="c0a66-153">Data representing the terms of use the PDF document.</span></span>|

## <a name="response"></a><span data-ttu-id="c0a66-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0a66-154">Response</span></span>
<span data-ttu-id="c0a66-155">Si tiene éxito, este método devuelve una `201, Created` objeto de [acuerdo](../resources/agreement.md) y código de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0a66-155">If successful, this method returns a `201, Created` response code and [agreement](../resources/agreement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c0a66-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0a66-156">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c0a66-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c0a66-157">Request</span></span>
<span data-ttu-id="c0a66-158">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [contrato](../resources/agreement.md) .</span><span class="sxs-lookup"><span data-stu-id="c0a66-158">In the request body, supply a JSON representation of the [agreement](../resources/agreement.md) object.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_agreement_from_agreements"
}-->
```http
POST https://graph.microsoft.com/beta/agreements
Content-type: application/json

{
  "displayName": "MSGraph Sample",
  "isViewingBeforeAcceptanceRequired": true,
  "files": [
    {
      "fileName": "TOU.pdf",
      "language": "en",
      "isDefault": true,
      "fileData": {
        "data": "SGVsbG8gd29ybGQ="
      }
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="c0a66-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0a66-159">Response</span></span>
><span data-ttu-id="c0a66-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c0a66-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.agreement"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "displayName": "MSGraph Sample",
  "isViewingBeforeAcceptanceRequired": true,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create agreement",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->