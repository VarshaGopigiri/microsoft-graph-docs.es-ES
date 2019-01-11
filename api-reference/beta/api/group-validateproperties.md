---
title: 'grupo: validateProperties'
description: Validar si el alias de correo o de nombre para mostrar de un grupo de Office 365 cumplen con las políticas de nomenclatura. Los clientes pueden usar la API para determinar si un nombre para mostrar o alias de correo sean válido antes de intentar **Actualizar** un grupo de Office 365. Para validar las propiedades antes de crear un grupo, utilice la función validateProperties para los objetos de Active directory.
localization_priority: Normal
ms.openlocfilehash: 0ffdf44f687ad047d952e00c268239432244006d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833904"
---
# <a name="group-validateproperties"></a><span data-ttu-id="7e6d0-105">grupo: validateProperties</span><span class="sxs-lookup"><span data-stu-id="7e6d0-105">group: validateProperties</span></span>

<span data-ttu-id="7e6d0-106">Validar si el alias de correo o de nombre para mostrar de un grupo de Office 365 cumplen con las políticas de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-106">Validate if an Office 365 group's display name or mail nickname complies with naming policies.</span></span> <span data-ttu-id="7e6d0-107">Los clientes pueden usar la API para determinar si un nombre para mostrar o alias de correo sean válido antes de intentar **Actualizar** un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-107">Clients can use the API to determine if a display name or mail nickname is valid before trying to **update** an Office 365 group.</span></span> <span data-ttu-id="7e6d0-108">Para validar las propiedades antes de crear un grupo, use la [función validateProperties](directoryobject-validateproperties.md) para los objetos de Active directory.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-108">For validating properties before creating a group, use the [validateProperties function](directoryobject-validateproperties.md) for directory objects.</span></span>

<span data-ttu-id="7e6d0-109">Se realizan las siguientes validaciones para las propiedades de alias para mostrar, nombre y correo:</span><span class="sxs-lookup"><span data-stu-id="7e6d0-109">The following validations are performed for the display name and mail nickname properties:</span></span> 
1. <span data-ttu-id="7e6d0-110">Validar el prefijo y el sufijo de directiva de nomenclatura</span><span class="sxs-lookup"><span data-stu-id="7e6d0-110">Validate the prefix and suffix naming policy</span></span>
2. <span data-ttu-id="7e6d0-111">Validar la directiva de las palabras no permitidas personalizadas</span><span class="sxs-lookup"><span data-stu-id="7e6d0-111">Validate the custom banned words policy</span></span>

<span data-ttu-id="7e6d0-112">Esta API devuelve con el primer error encontrado.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-112">This API returns with the first failure encountered.</span></span> <span data-ttu-id="7e6d0-113">Si una o más propiedades producirá un error en varias validaciones, se devuelve sólo la propiedad con el primer error de validación.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-113">If one or more properties fail multiple validations, only the property with the first validation failure is returned.</span></span> <span data-ttu-id="7e6d0-114">Sin embargo, puede validar el alias de correo y el nombre para mostrar y recibir una colección de errores de validación si solo va a validar el prefijo y el sufijo de directiva de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-114">However, you can validate both the mail nickname and the display name and receive a collection of validation errors if you are only validating the prefix and suffix naming policy.</span></span>

## <a name="permissions"></a><span data-ttu-id="7e6d0-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="7e6d0-115">Permissions</span></span>

<span data-ttu-id="7e6d0-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7e6d0-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7e6d0-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7e6d0-118">Permission type</span></span>      | <span data-ttu-id="7e6d0-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7e6d0-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7e6d0-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7e6d0-120">Delegated (work or school account)</span></span> | <span data-ttu-id="7e6d0-121">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7e6d0-121">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="7e6d0-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7e6d0-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7e6d0-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-123">Not supported.</span></span>    |
|<span data-ttu-id="7e6d0-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7e6d0-124">Application</span></span> | <span data-ttu-id="7e6d0-125">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7e6d0-125">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7e6d0-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7e6d0-126">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
``` http
POST /groups/<id>/validateProperties
```

## <a name="request-headers"></a><span data-ttu-id="7e6d0-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7e6d0-127">Request headers</span></span>

| <span data-ttu-id="7e6d0-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="7e6d0-128">Name</span></span>           | <span data-ttu-id="7e6d0-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e6d0-129">Description</span></span>      |
|:---------------|:-----------------|
| <span data-ttu-id="7e6d0-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="7e6d0-130">Authorization</span></span>  | <span data-ttu-id="7e6d0-131">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="7e6d0-131">Bearer {code}</span></span>    |
| <span data-ttu-id="7e6d0-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7e6d0-132">Content-Type</span></span>   | <span data-ttu-id="7e6d0-133">application/json</span><span class="sxs-lookup"><span data-stu-id="7e6d0-133">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="7e6d0-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7e6d0-134">Request body</span></span>

<span data-ttu-id="7e6d0-135">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-135">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7e6d0-136">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7e6d0-136">Parameter</span></span>    | <span data-ttu-id="7e6d0-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e6d0-137">Type</span></span>   |<span data-ttu-id="7e6d0-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e6d0-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7e6d0-139">displayName</span><span class="sxs-lookup"><span data-stu-id="7e6d0-139">displayName</span></span>|<span data-ttu-id="7e6d0-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="7e6d0-140">String</span></span>| <span data-ttu-id="7e6d0-141">El nombre para mostrar del grupo para validar.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-141">The display name of the group to validate.</span></span> <span data-ttu-id="7e6d0-142">La propiedad no es necesaria individualmente.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-142">The property is not individually required.</span></span> <span data-ttu-id="7e6d0-143">Sin embargo, al menos una propiedad (displayName o mailNickname) es necesaria.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-143">However, at least one property (displayName or mailNickname) is required.</span></span> |
|<span data-ttu-id="7e6d0-144">mailNickname</span><span class="sxs-lookup"><span data-stu-id="7e6d0-144">mailNickname</span></span>|<span data-ttu-id="7e6d0-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="7e6d0-145">String</span></span>| <span data-ttu-id="7e6d0-146">El alias de correo del grupo para validar.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-146">The mail nickname of the group to validate.</span></span> <span data-ttu-id="7e6d0-147">La propiedad no es necesaria individualmente.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-147">The property is not individually required.</span></span> <span data-ttu-id="7e6d0-148">Sin embargo, al menos una propiedad (displayName o mailNickname) es necesaria.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-148">However, at least one property (displayName or mailNickname) is required.</span></span> |
|<span data-ttu-id="7e6d0-149">onBehalfOfUserId</span><span class="sxs-lookup"><span data-stu-id="7e6d0-149">onBehalfOfUserId</span></span>|<span data-ttu-id="7e6d0-150">Guid</span><span class="sxs-lookup"><span data-stu-id="7e6d0-150">Guid</span></span>| <span data-ttu-id="7e6d0-151">El identificador de objeto del usuario para suplantar al llamar a la API.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-151">The object ID of the user to impersonate when calling the API.</span></span> <span data-ttu-id="7e6d0-152">Los resultados de validación son para los atributos y los roles de la onBehalfOfUserId.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-152">The validation results are for the onBehalfOfUserId's attributes and roles.</span></span> |

## <a name="response"></a><span data-ttu-id="7e6d0-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e6d0-153">Response</span></span>
<span data-ttu-id="7e6d0-154">Si se realiza correctamente y no hay ningún error de validación, el método devuelve `204 No Content` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-154">If successful and there are no validation errors, the method returns `204 No Content` response code.</span></span> <span data-ttu-id="7e6d0-155">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-155">It does not return anything in the response body.</span></span>

<span data-ttu-id="7e6d0-156">Si la solicitud no es válida, el método devuelve `400 Bad Request` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-156">If the request is invalid, the method returns `400 Bad Request` response code.</span></span> <span data-ttu-id="7e6d0-157">Se devuelve un mensaje de error con detalles acerca de la solicitud no válida en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-157">An error message with details about the invalid request is returned in the response body.</span></span>

<span data-ttu-id="7e6d0-158">Si se ha producido un error de validación.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-158">If there is a validation error.</span></span> <span data-ttu-id="7e6d0-159">El método devuelve `422 Unprocessable Entity` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-159">The method returns `422 Unprocessable Entity` response code.</span></span> <span data-ttu-id="7e6d0-160">Se devuelve un mensaje de error y una colección de detalles del error en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-160">An error message and a collection of error details is returned in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="7e6d0-161">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7e6d0-161">Examples</span></span>

<span data-ttu-id="7e6d0-162">Éste es un ejemplo de una solicitud de validación correcta.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-162">This is an example of a successful validation request.</span></span>

### <a name="request"></a><span data-ttu-id="7e6d0-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7e6d0-163">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "group_validateproperties"
}-->
``` http
POST https://graph.microsoft.com/beta/groups/{id}/validateProperties
Content-type: application/json
Content-length: 132

{
  "displayName": "Myprefix_test_mysuffix",
  "mailNickname": "Myprefix_test_mysuffix",
  "onBehalfOfUserId": "onBehalfOfUserId-value"
}
```

### <a name="response"></a><span data-ttu-id="7e6d0-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e6d0-164">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
} -->
```http
HTTP/1.1 204 No Content
```

<span data-ttu-id="7e6d0-165">Éste es un ejemplo de una solicitud con errores de validación.</span><span class="sxs-lookup"><span data-stu-id="7e6d0-165">This is an example of a request with validation errors.</span></span>

### <a name="request"></a><span data-ttu-id="7e6d0-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7e6d0-166">Request</span></span>
``` http
POST https://graph.microsoft.com/beta/groups/{id}/validateProperties
Content-type: application/json
Content-length: 128

{
  "displayName": "MyPrefix_test_mysuffix",
  "mailNickname": "MyPrefix_test_mysuffix"
}
```

### <a name="response"></a><span data-ttu-id="7e6d0-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e6d0-167">Response</span></span>
```http
HTTP/1.1 422
Content-type: application/json
Content-length: 223

{
  "error": {
    "code": "Request_UnprocessableEntity",
    "message": "The values provided contain one or more validation errors.",
    "innerError": {
      "request-id": "id-value",
      "date": "date-value"
    },
    "details": [
      {
        "target": "mailNickname",
        "code": "PropertyConflict",
        "message": "Another object with the same value for property mailNickname already exists."
      }
    ]
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: validateProperties",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
