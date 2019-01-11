---
title: Asignar directiva
description: Asigna una directiva a una aplicación o entidad de seguridad de servicio.
localization_priority: Normal
ms.openlocfilehash: 30ba92c1d0308f9c4846702008a203821ae2b7b0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27865460"
---
# <a name="assign-policy"></a><span data-ttu-id="28810-103">Asignar directiva</span><span class="sxs-lookup"><span data-stu-id="28810-103">Assign Policy</span></span>

> <span data-ttu-id="28810-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="28810-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="28810-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="28810-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="28810-106">Asigna una [Directiva](../resources/policy.md) a una aplicación o entidad de seguridad de servicio.</span><span class="sxs-lookup"><span data-stu-id="28810-106">Assigns a [policy](../resources/policy.md) to an application or service principal.</span></span>

><span data-ttu-id="28810-107">Nota: Actualmente, asignación de directivas solo se aplica a la directiva de duración del Token.</span><span class="sxs-lookup"><span data-stu-id="28810-107">Note: Currently, policy assignment only applies to Token lifetime Policy.</span></span> <span data-ttu-id="28810-108">Este tipo de directiva se describe en la [Directiva](../resources/policy.md).</span><span class="sxs-lookup"><span data-stu-id="28810-108">This type of policy is described in [policy](../resources/policy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="28810-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="28810-109">Permissions</span></span>
<span data-ttu-id="28810-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="28810-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="28810-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="28810-112">Permission type</span></span>      | <span data-ttu-id="28810-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="28810-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="28810-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="28810-114">Delegated (work or school account)</span></span> | <span data-ttu-id="28810-115">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="28810-115">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="28810-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="28810-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="28810-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="28810-117">Not supported.</span></span>    |
|<span data-ttu-id="28810-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="28810-118">Application</span></span> | <span data-ttu-id="28810-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="28810-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="28810-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="28810-120">HTTP request</span></span>

```http
POST /applications/{id}/policies/$ref
POST /serviceprincipals/{id}/policies/$ref
```

> <span data-ttu-id="28810-121">Nota: El identificador de"" en la solicitud es la propiedad "id" de la aplicación o el servicio de entidad de seguridad, no la propiedad "appid".</span><span class="sxs-lookup"><span data-stu-id="28810-121">Note: The "id" in the request is the "id" property of the application or service principal, not the "appid" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="28810-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="28810-122">Request headers</span></span>
| <span data-ttu-id="28810-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="28810-123">Name</span></span>       | <span data-ttu-id="28810-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="28810-124">Type</span></span> | <span data-ttu-id="28810-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="28810-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="28810-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="28810-126">Authorization</span></span>  | <span data-ttu-id="28810-127">string</span><span class="sxs-lookup"><span data-stu-id="28810-127">string</span></span>  | <span data-ttu-id="28810-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="28810-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="28810-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="28810-130">Content-Type</span></span> | <span data-ttu-id="28810-131">application/json</span><span class="sxs-lookup"><span data-stu-id="28810-131">application/json</span></span>  | <span data-ttu-id="28810-p105">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="28810-p105">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="28810-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="28810-134">Request body</span></span>
<span data-ttu-id="28810-135">En el cuerpo de la solicitud, proporcionan una representación JSON del objeto de directiva que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="28810-135">In the request body, provide a JSON representation of the policy object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="28810-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28810-136">Response</span></span>

<span data-ttu-id="28810-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="28810-137">If successful, this method returns `204 No Content` response code.</span></span> <span data-ttu-id="28810-138">Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.</span><span class="sxs-lookup"><span data-stu-id="28810-138">If unsuccessful, a `4xx` error will be returned with specific details.</span></span>

## <a name="example"></a><span data-ttu-id="28810-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28810-139">Example</span></span>
<span data-ttu-id="28810-140">El siguiente ejemplo asigna una directiva a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="28810-140">The following example assigns a policy to an application.</span></span>

##### <a name="request"></a><span data-ttu-id="28810-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="28810-141">Request</span></span>
<span data-ttu-id="28810-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="28810-142">Here is an example of the request.</span></span>

```http
POST /applications/{id}/policies/$ref
Content-type: application/json
{
    "@odata.id":"https://graph.microsoft.com/beta/policies/{policyid}"
}
```

##### <a name="response"></a><span data-ttu-id="28810-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28810-143">Response</span></span>
<span data-ttu-id="28810-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="28810-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 204 No Content
```
