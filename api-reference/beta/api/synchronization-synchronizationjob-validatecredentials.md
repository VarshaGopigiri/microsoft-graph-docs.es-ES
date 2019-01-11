---
title: 'synchronizationJob: validateCredentials'
description: Validar que las credenciales son válidas en el inquilino.
localization_priority: Normal
ms.openlocfilehash: b78d6f7b3ff197607897fbdce123aa1e7e646afc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834925"
---
# <a name="synchronizationjob-validatecredentials"></a><span data-ttu-id="1c4c0-103">synchronizationJob: validateCredentials</span><span class="sxs-lookup"><span data-stu-id="1c4c0-103">synchronizationJob: validateCredentials</span></span>

> <span data-ttu-id="1c4c0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1c4c0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1c4c0-106">Validar que las credenciales son válidas en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-106">Validate that the credentials are valid in the tenant.</span></span>

## <a name="permissions"></a><span data-ttu-id="1c4c0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1c4c0-107">Permissions</span></span>
<span data-ttu-id="1c4c0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1c4c0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1c4c0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1c4c0-110">Permission type</span></span>                        | <span data-ttu-id="1c4c0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1c4c0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="1c4c0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1c4c0-112">Delegated (work or school account)</span></span>     |<span data-ttu-id="1c4c0-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1c4c0-113">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="1c4c0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1c4c0-114">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="1c4c0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-115">Not supported.</span></span> |
|<span data-ttu-id="1c4c0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1c4c0-116">Application</span></span>                            |<span data-ttu-id="1c4c0-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-117">Not supported.</span></span>| 

## <a name="http-request"></a><span data-ttu-id="1c4c0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1c4c0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/{id}/validateCredentials

```
## <a name="request-headers"></a><span data-ttu-id="1c4c0-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1c4c0-119">Request headers</span></span>
| <span data-ttu-id="1c4c0-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="1c4c0-120">Name</span></span>       | <span data-ttu-id="1c4c0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c4c0-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1c4c0-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="1c4c0-122">Authorization</span></span>  | <span data-ttu-id="1c4c0-123">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="1c4c0-123">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="1c4c0-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1c4c0-124">Request body</span></span>
<span data-ttu-id="1c4c0-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="1c4c0-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1c4c0-126">Parameter</span></span>    | <span data-ttu-id="1c4c0-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c4c0-127">Type</span></span>   |<span data-ttu-id="1c4c0-128">Description</span><span class="sxs-lookup"><span data-stu-id="1c4c0-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1c4c0-129">useSavedCredentials</span><span class="sxs-lookup"><span data-stu-id="1c4c0-129">useSavedCredentials</span></span>|<span data-ttu-id="1c4c0-130">Booleano</span><span class="sxs-lookup"><span data-stu-id="1c4c0-130">Boolean</span></span>|<span data-ttu-id="1c4c0-131">Cuando `true`, el `credentials` se ignorará el parámetro y en su lugar se validará las credenciales guardadas anteriormente (si hay alguno).</span><span class="sxs-lookup"><span data-stu-id="1c4c0-131">When `true`, the `credentials` parameter will be ignored and the previously saved credentials (if any) will be validated instead.</span></span> |
|<span data-ttu-id="1c4c0-132">credenciales</span><span class="sxs-lookup"><span data-stu-id="1c4c0-132">credentials</span></span>|<span data-ttu-id="1c4c0-133">colección de [synchronizationSecretKeyStringValuePair](../resources/synchronization-secretkeystringvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="1c4c0-133">[synchronizationSecretKeyStringValuePair](../resources/synchronization-secretkeystringvaluepair.md) collection</span></span>|<span data-ttu-id="1c4c0-134">Credenciales para validar.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-134">Credentials to validate.</span></span> <span data-ttu-id="1c4c0-135">Cuándo se omite la `useSavedCredentials` parámetro es `true`.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-135">Ignored when the `useSavedCredentials` parameter is `true`.</span></span>|

## <a name="response"></a><span data-ttu-id="1c4c0-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c4c0-136">Response</span></span>
<span data-ttu-id="1c4c0-137">Si la validación es correcta, este método devuelve una `204, No Content` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-137">If validation is successful, this method returns a `204, No Content` response code.</span></span> <span data-ttu-id="1c4c0-138">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-138">It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1c4c0-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1c4c0-139">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1c4c0-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c4c0-140">Request</span></span>
<span data-ttu-id="1c4c0-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-141">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "synchronizationjob_validatecredentials"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{id}/validateCredentials
Content-type: application/json
Content-length: 218

{ 
    credentials: [ 
        { key: "UserName", value: "user@domain.com" },
        { key: "Password", value: "password-value" }
    ]
}
```

##### <a name="response"></a><span data-ttu-id="1c4c0-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c4c0-142">Response</span></span>
<span data-ttu-id="1c4c0-143">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c4c0-143">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationJob: validateCredentials",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
