---
title: Directiva de actualización
description: Actualizar las propiedades de una directiva existente.
ms.openlocfilehash: 426476b5545e511fe2da111acb1f47f38f32c96f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090282"
---
# <a name="update-policy"></a><span data-ttu-id="8ae24-103">Directiva de actualización</span><span class="sxs-lookup"><span data-stu-id="8ae24-103">Update Policy</span></span>

> <span data-ttu-id="8ae24-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8ae24-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8ae24-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8ae24-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8ae24-106">Actualizar las propiedades de una [Directiva](../resources/policy.md)de ya existente.</span><span class="sxs-lookup"><span data-stu-id="8ae24-106">Update properties in a preexisting [policy](../resources/policy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="8ae24-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="8ae24-107">Permissions</span></span>
<span data-ttu-id="8ae24-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8ae24-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8ae24-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8ae24-110">Permission type</span></span>      | <span data-ttu-id="8ae24-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8ae24-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8ae24-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8ae24-112">Delegated (work or school account)</span></span> | <span data-ttu-id="8ae24-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="8ae24-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="8ae24-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8ae24-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8ae24-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ae24-115">Not supported.</span></span>    |
|<span data-ttu-id="8ae24-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8ae24-116">Application</span></span> | <span data-ttu-id="8ae24-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ae24-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8ae24-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8ae24-118">HTTP request</span></span>

```http
PATCH /policies/{id}
```
## <a name="request-headers"></a><span data-ttu-id="8ae24-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ae24-119">Request headers</span></span>
| <span data-ttu-id="8ae24-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="8ae24-120">Name</span></span>       | <span data-ttu-id="8ae24-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ae24-121">Type</span></span> | <span data-ttu-id="8ae24-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ae24-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="8ae24-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8ae24-123">Authorization</span></span>  | <span data-ttu-id="8ae24-124">string</span><span class="sxs-lookup"><span data-stu-id="8ae24-124">string</span></span>  | <span data-ttu-id="8ae24-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ae24-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8ae24-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8ae24-127">Content-Type</span></span> | <span data-ttu-id="8ae24-128">application/json</span><span class="sxs-lookup"><span data-stu-id="8ae24-128">application/json</span></span>  | <span data-ttu-id="8ae24-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ae24-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8ae24-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8ae24-131">Request body</span></span>
<span data-ttu-id="8ae24-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los parámetros que necesitan actualizarse.</span><span class="sxs-lookup"><span data-stu-id="8ae24-132">In the request body, provide a JSON object with the parameters that need to be updated.</span></span> <span data-ttu-id="8ae24-133">La siguiente tabla muestran los posibles parámetros.</span><span class="sxs-lookup"><span data-stu-id="8ae24-133">The following table shows the possible parameters.</span></span>

| <span data-ttu-id="8ae24-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8ae24-134">Parameter</span></span>    | <span data-ttu-id="8ae24-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ae24-135">Type</span></span>   |<span data-ttu-id="8ae24-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ae24-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8ae24-137">definición</span><span class="sxs-lookup"><span data-stu-id="8ae24-137">definition</span></span>|<span data-ttu-id="8ae24-138">String</span><span class="sxs-lookup"><span data-stu-id="8ae24-138">String</span></span>|<span data-ttu-id="8ae24-139">La versión stringified del objeto de [Directiva](../resources/policy.md) .</span><span class="sxs-lookup"><span data-stu-id="8ae24-139">The stringified version of the [policy](../resources/policy.md) object.</span></span>|
|<span data-ttu-id="8ae24-140">displayName</span><span class="sxs-lookup"><span data-stu-id="8ae24-140">displayName</span></span>|<span data-ttu-id="8ae24-141">String</span><span class="sxs-lookup"><span data-stu-id="8ae24-141">String</span></span>|<span data-ttu-id="8ae24-142">Un nombre personalizado para la directiva.</span><span class="sxs-lookup"><span data-stu-id="8ae24-142">A custom name for the policy.</span></span>|
|<span data-ttu-id="8ae24-143">isOrganizationDefault</span><span class="sxs-lookup"><span data-stu-id="8ae24-143">isOrganizationDefault</span></span>|<span data-ttu-id="8ae24-144">Booleano</span><span class="sxs-lookup"><span data-stu-id="8ae24-144">Boolean</span></span>|<span data-ttu-id="8ae24-145">Especifica si se aplica esta directiva de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8ae24-145">Specifies if this policy is applied by default.</span></span>|
|<span data-ttu-id="8ae24-146">type</span><span class="sxs-lookup"><span data-stu-id="8ae24-146">type</span></span>|<span data-ttu-id="8ae24-147">String</span><span class="sxs-lookup"><span data-stu-id="8ae24-147">String</span></span>|<span data-ttu-id="8ae24-148">Especifica el tipo de directiva.</span><span class="sxs-lookup"><span data-stu-id="8ae24-148">Specifies the type of policy.</span></span> <span data-ttu-id="8ae24-149">Actualmente, debe ser "TokenLifetimePolicy"</span><span class="sxs-lookup"><span data-stu-id="8ae24-149">Currently must be "TokenLifetimePolicy"</span></span>|

## <a name="response"></a><span data-ttu-id="8ae24-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ae24-150">Response</span></span>

<span data-ttu-id="8ae24-151">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="8ae24-151">If successful, this method returns `204 No Content` response code.</span></span> <span data-ttu-id="8ae24-152">Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.</span><span class="sxs-lookup"><span data-stu-id="8ae24-152">If unsuccessful, a `4xx` error will be returned with specific details.</span></span>

## <a name="example"></a><span data-ttu-id="8ae24-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ae24-153">Example</span></span>
<span data-ttu-id="8ae24-154">En el ejemplo siguiente se actualiza la definición de la directiva de duración del token y se establece como el valor predeterminado de la organización.</span><span class="sxs-lookup"><span data-stu-id="8ae24-154">The following example updates the definition of the token lifetime policy and sets it as the organization default.</span></span>

##### <a name="request"></a><span data-ttu-id="8ae24-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ae24-155">Request</span></span>
<span data-ttu-id="8ae24-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ae24-156">Here is an example of the request.</span></span>

```http
PATCH https://graph.microsoft.com/beta/policies/{id}
Content-Type: application/json
{
    "definition":["{\"TokenLifetimePolicy\":{\"Version\":1,\"AccessTokenLifetime\":\"8:00:00\",\"MaxInactiveTime\":\"20:00:00\",}}"],
    "isOrganizationDefault":true
}
```

##### <a name="response"></a><span data-ttu-id="8ae24-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ae24-157">Response</span></span>
<span data-ttu-id="8ae24-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ae24-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 204 No Content
```
