---
title: Agregar un miembro
description: Utilice esta API para agregar a un miembro (usuario o grupo) a una unidad administrativa.
author: lleonard-msft
ms.openlocfilehash: be47dbf06c5f59c0a4aaaea4f8c8b4aa8c3ce902
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339231"
---
# <a name="add-a-member"></a><span data-ttu-id="53987-103">Agregar un miembro</span><span class="sxs-lookup"><span data-stu-id="53987-103">Add a member</span></span>

> <span data-ttu-id="53987-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53987-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53987-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53987-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="53987-106">Utilice esta API para agregar a un miembro (usuario o grupo) a una unidad administrativa.</span><span class="sxs-lookup"><span data-stu-id="53987-106">Use this API to add a member (user or group) to an administrative unit.</span></span>

`NOTE: Currently it's only possible to add one member at a time to an administrative unit.`

## <a name="permissions"></a><span data-ttu-id="53987-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="53987-107">Permissions</span></span>
<span data-ttu-id="53987-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="53987-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="53987-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53987-110">Permission type</span></span>      | <span data-ttu-id="53987-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53987-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="53987-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53987-112">Delegated (work or school account)</span></span> | <span data-ttu-id="53987-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="53987-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="53987-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53987-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="53987-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53987-115">Not supported.</span></span>    |
|<span data-ttu-id="53987-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53987-116">Application</span></span> | <span data-ttu-id="53987-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53987-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="53987-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53987-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /administrativeUnits/{id}/members/$ref
```
## <a name="request-headers"></a><span data-ttu-id="53987-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53987-119">Request headers</span></span>
| <span data-ttu-id="53987-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="53987-120">Name</span></span>      |<span data-ttu-id="53987-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="53987-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="53987-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="53987-122">Authorization</span></span>  | <span data-ttu-id="53987-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="53987-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="53987-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53987-125">Request body</span></span>
<span data-ttu-id="53987-126">En el cuerpo de la solicitud, proporcionar una representación JSON de un [usuario](../resources/user.md), [grupo](../resources/group.md) o [directoryObject](../resources/directoryobject.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="53987-126">In the request body, supply a JSON representation of a [user](../resources/user.md),  [group](../resources/group.md) or [directoryObject](../resources/directoryobject.md) to be added.</span></span>

## <a name="response"></a><span data-ttu-id="53987-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53987-127">Response</span></span>

<span data-ttu-id="53987-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53987-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53987-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53987-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="53987-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53987-131">Request</span></span>
<span data-ttu-id="53987-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53987-132">Here is an example of the request.</span></span>

```http
POST https://graph.microsoft.com/beta/administrativeUnits/{id}/members/$ref
Content-type: application/json
Content-length: 109

{
  "@odata.id":"https://graph.microsoft.com/beta/groups/{id}"
}

```
<span data-ttu-id="53987-133">En el cuerpo de la solicitud, proporcionar una representación JSON de la `id` del objeto de [usuario](../resources/user.md) o [grupo](../resources/group.md) que desea agregar.</span><span class="sxs-lookup"><span data-stu-id="53987-133">In the request body, supply a JSON representation of the `id` of the [user](../resources/user.md) or [group](../resources/group.md) object you want to add.</span></span>

##### <a name="response"></a><span data-ttu-id="53987-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53987-134">Response</span></span>
<span data-ttu-id="53987-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53987-135">Here is an example of the response.</span></span>
 
```http
HTTP/1.1 204 No Content
```
