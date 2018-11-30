---
title: Eliminar directiva
description: Eliminar una directiva.
ms.openlocfilehash: 37ed08e7f53db726a46821c08d68c955afdacc5a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090444"
---
# <a name="delete-policy"></a><span data-ttu-id="b29e7-103">Eliminar directiva</span><span class="sxs-lookup"><span data-stu-id="b29e7-103">Delete Policy</span></span>

> <span data-ttu-id="b29e7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b29e7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b29e7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b29e7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b29e7-106">Eliminar una [Directiva](../resources/policy.md).</span><span class="sxs-lookup"><span data-stu-id="b29e7-106">Delete a [policy](../resources/policy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="b29e7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b29e7-107">Permissions</span></span>
<span data-ttu-id="b29e7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b29e7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b29e7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b29e7-110">Permission type</span></span>      | <span data-ttu-id="b29e7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b29e7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b29e7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b29e7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b29e7-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="b29e7-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="b29e7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b29e7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b29e7-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b29e7-115">Not supported.</span></span>    |
|<span data-ttu-id="b29e7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b29e7-116">Application</span></span> | <span data-ttu-id="b29e7-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b29e7-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b29e7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b29e7-118">HTTP request</span></span>

```http
DELETE /policies/{id}
```
## <a name="request-headers"></a><span data-ttu-id="b29e7-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b29e7-119">Request headers</span></span>
| <span data-ttu-id="b29e7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b29e7-120">Name</span></span>       | <span data-ttu-id="b29e7-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b29e7-121">Type</span></span> | <span data-ttu-id="b29e7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b29e7-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b29e7-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b29e7-123">Authorization</span></span>  | <span data-ttu-id="b29e7-124">string</span><span class="sxs-lookup"><span data-stu-id="b29e7-124">string</span></span>  | <span data-ttu-id="b29e7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b29e7-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b29e7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b29e7-127">Request body</span></span>
<span data-ttu-id="b29e7-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b29e7-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b29e7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b29e7-129">Response</span></span>

<span data-ttu-id="b29e7-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b29e7-130">If successful, this method returns `204 No Content` response code.</span></span> <span data-ttu-id="b29e7-131">Si no lo consigue...</span><span class="sxs-lookup"><span data-stu-id="b29e7-131">If unsuccessful...</span></span>

## <a name="example"></a><span data-ttu-id="b29e7-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b29e7-132">Example</span></span>
<span data-ttu-id="b29e7-133">En el ejemplo siguiente se elimina una directiva.</span><span class="sxs-lookup"><span data-stu-id="b29e7-133">The following example deletes a policy.</span></span>

##### <a name="request"></a><span data-ttu-id="b29e7-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b29e7-134">Request</span></span>
<span data-ttu-id="b29e7-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b29e7-135">Here is an example of the request.</span></span>

```http
DELETE https://graph.microsoft.com/beta/policies/{id}
```

##### <a name="response"></a><span data-ttu-id="b29e7-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b29e7-136">Response</span></span>
<span data-ttu-id="b29e7-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b29e7-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 204 No Content
```
