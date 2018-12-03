---
title: Quitar un miembro
description: Utilice esta API para quitar a un miembro (usuario o grupo) desde una unidad administrativa.
ms.openlocfilehash: dbf8ceaf66436ff44ea014ae5383e2f669fc7466
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084352"
---
# <a name="remove-a-member"></a><span data-ttu-id="850c1-103">Quitar un miembro</span><span class="sxs-lookup"><span data-stu-id="850c1-103">Remove a member</span></span>

> <span data-ttu-id="850c1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="850c1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="850c1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="850c1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="850c1-106">Utilice esta API para quitar a un miembro (usuario o grupo) desde una unidad administrativa.</span><span class="sxs-lookup"><span data-stu-id="850c1-106">Use this API to remove a member (user or group) from an administrative unit.</span></span>

## <a name="permissions"></a><span data-ttu-id="850c1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="850c1-107">Permissions</span></span>
<span data-ttu-id="850c1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="850c1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="850c1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="850c1-110">Permission type</span></span>      | <span data-ttu-id="850c1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="850c1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="850c1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="850c1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="850c1-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="850c1-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="850c1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="850c1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="850c1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="850c1-115">Not supported.</span></span>    |
|<span data-ttu-id="850c1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="850c1-116">Application</span></span> | <span data-ttu-id="850c1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="850c1-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="850c1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="850c1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /administrativeUnits/{id}/members/{id}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="850c1-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="850c1-119">Request headers</span></span>
| <span data-ttu-id="850c1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="850c1-120">Name</span></span>      |<span data-ttu-id="850c1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="850c1-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="850c1-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="850c1-122">Authorization</span></span>  | <span data-ttu-id="850c1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="850c1-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="850c1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="850c1-125">Request body</span></span>
<span data-ttu-id="850c1-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="850c1-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="850c1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="850c1-127">Response</span></span>

<span data-ttu-id="850c1-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="850c1-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="850c1-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="850c1-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="850c1-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="850c1-131">Request</span></span>
<span data-ttu-id="850c1-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="850c1-132">Here is an example of the request.</span></span> <span data-ttu-id="850c1-133">En el ejemplo siguiente, id1 representa el identificador de la unidad de destino administrativa y id2 representa el identificador único para el usuario de miembro o el grupo que se quitará de la unidad administrativa dura.</span><span class="sxs-lookup"><span data-stu-id="850c1-133">In the example below, id1 represents the identifier for the target administrative unit, and id2 represents the unique identifier for the member user or group to be removed from the targetted administrative unit.</span></span> 

```http
DELETE https://graph.microsoft.com/beta/administrativeUnits/{id1}/members/{id2}/$ref
```

##### <a name="response"></a><span data-ttu-id="850c1-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="850c1-134">Response</span></span>
<span data-ttu-id="850c1-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="850c1-135">Here is an example of the response.</span></span>
 
```http
HTTP/1.1 204 No Content
```