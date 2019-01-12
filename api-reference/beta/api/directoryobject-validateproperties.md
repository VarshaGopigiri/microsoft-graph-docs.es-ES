---
title: 'directoryObject: validateProperties'
description: Validar si el alias de correo o de nombre para mostrar de un grupo de Office 365 cumplen con las políticas de nomenclatura.  Los clientes pueden usar la API para determinar si un nombre para mostrar o alias de correo sean válido antes de intentar **crear** un grupo de Office 365. Para validar las propiedades de un grupo existente, utilice la función validateProperties para grupos.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 515acb022150d091e7dcbbdecc1fb1adef849a88
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921321"
---
# <a name="directoryobject-validateproperties"></a><span data-ttu-id="7f881-105">directoryObject: validateProperties</span><span class="sxs-lookup"><span data-stu-id="7f881-105">directoryObject: validateProperties</span></span>

<span data-ttu-id="7f881-106">Validar si el alias de correo o de nombre para mostrar de un grupo de Office 365 cumplen con las políticas de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="7f881-106">Validate if an Office 365 group's display name or mail nickname complies with naming policies.</span></span>  <span data-ttu-id="7f881-107">Los clientes pueden usar la API para determinar si un nombre para mostrar o alias de correo sean válido antes de intentar **crear** un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="7f881-107">Clients can use the API to determine if a display name or mail nickname is valid before trying to **create** an Office 365 group.</span></span> <span data-ttu-id="7f881-108">Para validar las propiedades de un grupo existente, use la [función validateProperties](group-validateproperties.md) para grupos.</span><span class="sxs-lookup"><span data-stu-id="7f881-108">For validating properties of an existing group, use the [validateProperties function](group-validateproperties.md) for groups.</span></span>

<span data-ttu-id="7f881-109">Se realizan las siguientes validaciones para las propiedades de alias para mostrar, nombre y correo:</span><span class="sxs-lookup"><span data-stu-id="7f881-109">The following validations are performed for the display name and mail nickname properties:</span></span> 
1. <span data-ttu-id="7f881-110">Validar el prefijo y el sufijo de directiva de nomenclatura</span><span class="sxs-lookup"><span data-stu-id="7f881-110">Validate the prefix and suffix naming policy</span></span>
2. <span data-ttu-id="7f881-111">Validar la directiva de las palabras no permitidas personalizadas</span><span class="sxs-lookup"><span data-stu-id="7f881-111">Validate the custom banned words policy</span></span>
3. <span data-ttu-id="7f881-112">Validar el correo sobrenombre es único</span><span class="sxs-lookup"><span data-stu-id="7f881-112">Validate the mail nickname is unique</span></span>

<span data-ttu-id="7f881-113">Esta API devuelve con el primer error encontrado.</span><span class="sxs-lookup"><span data-stu-id="7f881-113">This API returns with the first failure encountered.</span></span> <span data-ttu-id="7f881-114">Si una o más propiedades producirá un error en varias validaciones, se devuelve sólo la propiedad con el primer error de validación.</span><span class="sxs-lookup"><span data-stu-id="7f881-114">If one or more properties fail multiple validations, only the property with the first validation failure is returned.</span></span> <span data-ttu-id="7f881-115">Sin embargo, puede validar el alias de correo y el nombre para mostrar y recibir una colección de errores de validación si solo va a validar el prefijo y el sufijo de directiva de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="7f881-115">However, you can validate both the mail nickname and the display name and receive a collection of validation errors if you are only validating the prefix and suffix naming policy.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7f881-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7f881-116">Prerequisites</span></span>

<span data-ttu-id="7f881-117">Se requiere el siguiente **permiso** para ejecutar esta API: *Group.Read.All*</span><span class="sxs-lookup"><span data-stu-id="7f881-117">The following **permission** is required to execute this API: *Group.Read.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="7f881-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7f881-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
``` http
POST /directoryObjects/validateProperties
```

## <a name="request-headers"></a><span data-ttu-id="7f881-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7f881-119">Request headers</span></span>

| <span data-ttu-id="7f881-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7f881-120">Name</span></span>           | <span data-ttu-id="7f881-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f881-121">Description</span></span>      |
|:---------------|:-----------------|
| <span data-ttu-id="7f881-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="7f881-122">Authorization</span></span>  | <span data-ttu-id="7f881-123">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="7f881-123">Bearer {code}</span></span>    |
| <span data-ttu-id="7f881-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7f881-124">Content-Type</span></span>   | <span data-ttu-id="7f881-125">application/json</span><span class="sxs-lookup"><span data-stu-id="7f881-125">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="7f881-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7f881-126">Request body</span></span>
<span data-ttu-id="7f881-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7f881-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7f881-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7f881-128">Parameter</span></span>    | <span data-ttu-id="7f881-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f881-129">Type</span></span>   |<span data-ttu-id="7f881-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f881-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7f881-131">entityType</span><span class="sxs-lookup"><span data-stu-id="7f881-131">entityType</span></span>|<span data-ttu-id="7f881-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="7f881-132">String</span></span>| <span data-ttu-id="7f881-133">`Group`es el tipo de entidad compatibles sólo.</span><span class="sxs-lookup"><span data-stu-id="7f881-133">`Group` is the only supported entity type.</span></span> |
|<span data-ttu-id="7f881-134">displayName</span><span class="sxs-lookup"><span data-stu-id="7f881-134">displayName</span></span>|<span data-ttu-id="7f881-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="7f881-135">String</span></span>| <span data-ttu-id="7f881-136">El nombre para mostrar del grupo para validar.</span><span class="sxs-lookup"><span data-stu-id="7f881-136">The display name of the group to validate.</span></span> <span data-ttu-id="7f881-137">La propiedad no es necesaria individualmente.</span><span class="sxs-lookup"><span data-stu-id="7f881-137">The property is not individually required.</span></span> <span data-ttu-id="7f881-138">Sin embargo, al menos una propiedad (displayName o mailNickname) es necesaria.</span><span class="sxs-lookup"><span data-stu-id="7f881-138">However, at least one property (displayName or mailNickname) is required.</span></span> |
|<span data-ttu-id="7f881-139">mailNickname</span><span class="sxs-lookup"><span data-stu-id="7f881-139">mailNickname</span></span>|<span data-ttu-id="7f881-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="7f881-140">String</span></span>| <span data-ttu-id="7f881-141">El alias de correo del grupo para validar.</span><span class="sxs-lookup"><span data-stu-id="7f881-141">The mail nickname of the group to validate.</span></span> <span data-ttu-id="7f881-142">La propiedad no es necesaria individualmente.</span><span class="sxs-lookup"><span data-stu-id="7f881-142">The property is not individually required.</span></span> <span data-ttu-id="7f881-143">Sin embargo, al menos una propiedad (displayName o mailNickname) es necesaria.</span><span class="sxs-lookup"><span data-stu-id="7f881-143">However, at least one property (displayName or mailNickname) is required.</span></span> |
|<span data-ttu-id="7f881-144">onBehalfOfUserId</span><span class="sxs-lookup"><span data-stu-id="7f881-144">onBehalfOfUserId</span></span>|<span data-ttu-id="7f881-145">Guid</span><span class="sxs-lookup"><span data-stu-id="7f881-145">Guid</span></span>| <span data-ttu-id="7f881-146">El identificador de objeto del usuario para suplantar al llamar a la API.</span><span class="sxs-lookup"><span data-stu-id="7f881-146">The object ID of the user to impersonate when calling the API.</span></span> <span data-ttu-id="7f881-147">Los resultados de validación son para los atributos y los roles de la onBehalfOfUserId.</span><span class="sxs-lookup"><span data-stu-id="7f881-147">The validation results are for the onBehalfOfUserId's attributes and roles.</span></span> |

## <a name="response"></a><span data-ttu-id="7f881-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f881-148">Response</span></span>

<span data-ttu-id="7f881-149">Si se realiza correctamente y no hay ningún error de validación, el método devuelve `204 No Content` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f881-149">If successful and there are no validation errors, the method returns `204 No Content` response code.</span></span> <span data-ttu-id="7f881-150">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f881-150">It does not return anything in the response body.</span></span>

<span data-ttu-id="7f881-151">Si la solicitud no es válida, el método devuelve `400 Bad Request` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f881-151">If the request is invalid, the method returns `400 Bad Request` response code.</span></span> <span data-ttu-id="7f881-152">Se devuelve un mensaje de error con detalles acerca de la solicitud no válida en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f881-152">An error message with details about the invalid request is returned in the response body.</span></span>

<span data-ttu-id="7f881-153">Si hay un error de validación, el método devuelve `422 Unprocessable Entity` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f881-153">If there is a validation error, the method returns `422 Unprocessable Entity` response code.</span></span> <span data-ttu-id="7f881-154">Se devuelve un mensaje de error y una colección de detalles del error en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f881-154">An error message and a collection of error details is returned in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="7f881-155">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7f881-155">Examples</span></span>

<span data-ttu-id="7f881-156">Éste es un ejemplo de una solicitud de validación correcta.</span><span class="sxs-lookup"><span data-stu-id="7f881-156">This is an example of a successful validation request.</span></span>

### <a name="request"></a><span data-ttu-id="7f881-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7f881-157">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "directoryobject_validateproperties"
}-->
``` http
POST https://graph.microsoft.com/directoryObjects/validateProperties
Content-type: application/json
Content-length: 164

{
  "entityType": "Group",
  "displayName": "Myprefix_test_mysuffix",
  "mailNickname": "Myprefix_test_mysuffix",
  "onBehalfOfUserId": "onBehalfOfUserId-value"
}
```

### <a name="response"></a><span data-ttu-id="7f881-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f881-158">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<span data-ttu-id="7f881-159">Éste es un ejemplo de una solicitud con errores de validación.</span><span class="sxs-lookup"><span data-stu-id="7f881-159">This is an example of a request with validation errors.</span></span>

### <a name="request"></a><span data-ttu-id="7f881-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7f881-160">Request</span></span>
```http
POST https://graph.microsoft.com/directoryObjects/validateProperties
Content-type: application/json
Content-length: 164

{
  "entityType": "Group",
  "displayName": "test",
  "mailNickname": "test",
  "onBehalfOfUserId": "onBehalfOfUserId-value"
}
```

### <a name="response"></a><span data-ttu-id="7f881-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f881-161">Response</span></span>
```http
HTTP/1.1 422 
Content-Type: application/json

{
  "error": {
    "code": "Request_UnprocessableEntity",
    "message": "The values provided contain one or more validation errors.",
    "innerError": {
      "request-id": "request-id-value",
      "date": "date-value"
    },
    "details": [
      {
        "target": "displayName",
        "code": "MissingPrefixSuffix",
        "message": "Property mailNickname is missing a required prefix/suffix per your organization's Group naming requirements.",
        "prefix": "Myprefix_",
        "suffix": "_mysuffix"
      },
      {
        "target": "mailNickname",
        "code": "MissingPrefixSuffix",
        "message": "Property mailNickname is missing a required prefix/suffix per your organization's Group naming requirements.",
        "prefix": "Myprefix_",
        "suffix": "_mysuffix"
      }
    ]
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: validateProperties",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
