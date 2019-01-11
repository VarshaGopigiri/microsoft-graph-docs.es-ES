---
title: Crear directiva
description: Crear un nuevo objeto de directiva mediante la especificación de nombre para mostrar, el tipo de directiva y la descripción de la directiva.
localization_priority: Normal
ms.openlocfilehash: 4850b2899bfd9add703af912f16602960b2657f4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831237"
---
# <a name="create-policy"></a><span data-ttu-id="4a221-103">Crear directiva</span><span class="sxs-lookup"><span data-stu-id="4a221-103">Create Policy</span></span>

> <span data-ttu-id="4a221-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4a221-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4a221-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4a221-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4a221-106">Crear un nuevo objeto de [Directiva](../resources/policy.md) mediante la especificación de nombre para mostrar, el tipo de directiva y la descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="4a221-106">Create a new [policy](../resources/policy.md) object by specifying display name, policy type, and policy description.</span></span>

><span data-ttu-id="4a221-107">Nota: Los detalles de la directiva se validará antes de que se almacenan.</span><span class="sxs-lookup"><span data-stu-id="4a221-107">Note: The policy details will be validated before being stored.</span></span> <span data-ttu-id="4a221-108">Si no pasa la validación, un 400 Solicitud incorrecta se devolverá.</span><span class="sxs-lookup"><span data-stu-id="4a221-108">If it does not pass validation, a 400 Bad Request will be returned.</span></span>

## <a name="permissions"></a><span data-ttu-id="4a221-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="4a221-109">Permissions</span></span>
<span data-ttu-id="4a221-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4a221-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4a221-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a221-112">Permission type</span></span>      | <span data-ttu-id="4a221-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a221-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4a221-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a221-114">Delegated (work or school account)</span></span> | <span data-ttu-id="4a221-115">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4a221-115">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4a221-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a221-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4a221-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a221-117">Not supported.</span></span>    |
|<span data-ttu-id="4a221-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a221-118">Application</span></span> | <span data-ttu-id="4a221-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a221-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4a221-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a221-120">HTTP request</span></span>

```http
POST /policies
```
## <a name="request-headers"></a><span data-ttu-id="4a221-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4a221-121">Request headers</span></span>
| <span data-ttu-id="4a221-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="4a221-122">Name</span></span>       | <span data-ttu-id="4a221-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a221-123">Type</span></span> | <span data-ttu-id="4a221-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a221-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4a221-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="4a221-125">Authorization</span></span>  | <span data-ttu-id="4a221-126">string</span><span class="sxs-lookup"><span data-stu-id="4a221-126">string</span></span>  | <span data-ttu-id="4a221-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4a221-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4a221-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4a221-129">Content-Type</span></span> | <span data-ttu-id="4a221-130">application/json</span><span class="sxs-lookup"><span data-stu-id="4a221-130">application/json</span></span>  | <span data-ttu-id="4a221-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4a221-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4a221-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4a221-133">Request body</span></span>
<span data-ttu-id="4a221-134">En el cuerpo de la solicitud, proporcionan una representación JSON de objeto de [Directiva](../resources/policy.md) .</span><span class="sxs-lookup"><span data-stu-id="4a221-134">In the request body, provide a JSON representation of [policy](../resources/policy.md) object.</span></span>

<span data-ttu-id="4a221-135">En la siguiente tabla se muestra las propiedades que son necesarias para crear una directiva.</span><span class="sxs-lookup"><span data-stu-id="4a221-135">The following table shows the properties that are required when you create a policy.</span></span>

| <span data-ttu-id="4a221-136">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4a221-136">Parameter</span></span>    | <span data-ttu-id="4a221-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a221-137">Type</span></span>   |<span data-ttu-id="4a221-138">Description</span><span class="sxs-lookup"><span data-stu-id="4a221-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4a221-139">definición</span><span class="sxs-lookup"><span data-stu-id="4a221-139">definition</span></span>|<span data-ttu-id="4a221-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="4a221-140">String</span></span>|<span data-ttu-id="4a221-141">La versión de cadena del objeto de [Directiva](../resources/policy.md) .</span><span class="sxs-lookup"><span data-stu-id="4a221-141">The string version of the [policy](../resources/policy.md) object.</span></span>|
|<span data-ttu-id="4a221-142">displayName</span><span class="sxs-lookup"><span data-stu-id="4a221-142">displayName</span></span>|<span data-ttu-id="4a221-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="4a221-143">String</span></span>|<span data-ttu-id="4a221-144">Un nombre personalizado para la directiva.</span><span class="sxs-lookup"><span data-stu-id="4a221-144">A custom name for the policy.</span></span>|
|<span data-ttu-id="4a221-145">type</span><span class="sxs-lookup"><span data-stu-id="4a221-145">type</span></span>|<span data-ttu-id="4a221-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="4a221-146">String</span></span>|<span data-ttu-id="4a221-147">Especifica el tipo de directiva.</span><span class="sxs-lookup"><span data-stu-id="4a221-147">Specifies the type of policy.</span></span> <span data-ttu-id="4a221-148">Actualmente, debe ser "TokenLifetimePolicy"</span><span class="sxs-lookup"><span data-stu-id="4a221-148">Currently must be "TokenLifetimePolicy"</span></span>|

## <a name="response"></a><span data-ttu-id="4a221-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a221-149">Response</span></span>

<span data-ttu-id="4a221-150">Si tiene éxito, este método devuelve `201 Created` objeto de código y la [Directiva](../resources/policy.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a221-150">If successful, this method returns `201 Created` response code and [policy](../resources/policy.md) object in the response body.</span></span> <span data-ttu-id="4a221-151">Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.</span><span class="sxs-lookup"><span data-stu-id="4a221-151">If unsuccessful, a `4xx` error will be returned with specific details.</span></span>  

## <a name="example"></a><span data-ttu-id="4a221-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a221-152">Example</span></span>
<span data-ttu-id="4a221-153">En el ejemplo siguiente se crea una nueva duración del token directiva.</span><span class="sxs-lookup"><span data-stu-id="4a221-153">The following example creates a new token lifetime Policy.</span></span> <span data-ttu-id="4a221-154">Tenga en cuenta que el parámetro de cadena de definición se con caracteres de escape comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="4a221-154">Notice the string definition parameter has escaped double quotes.</span></span>

##### <a name="request"></a><span data-ttu-id="4a221-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4a221-155">Request</span></span>
<span data-ttu-id="4a221-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a221-156">Here is an example of the request.</span></span>

```http
POST https://graph.microsoft.com/beta/policies
Content-Type: application/json

{
  "displayName":"CustomTokenLifetimePolicy",
  "definition":["{\"TokenLifetimePolicy\":{\"Version\":1,\"AccessTokenLifetime\":\"8:00:00\"}}"],
  "type":"TokenLifetimePolicy"
}
```

##### <a name="response"></a><span data-ttu-id="4a221-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a221-157">Response</span></span>
<span data-ttu-id="4a221-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4a221-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#policies/$entity",
  "id":"id-value",
  "alternativeIdentifier":null,
  "definition":["{\"TokenLifetimePolicy\":{\"Version\":1,\"AccessTokenLifetime\":\"8:00:00\"}}"],
  "displayName":"name-value",
  "isOrganizationDefault":false,
  "keyCredentials",
  "type":"TokenLifetimePolicy"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: createReply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
