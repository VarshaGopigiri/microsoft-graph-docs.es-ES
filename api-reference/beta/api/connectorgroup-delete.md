---
title: Eliminar connectorGroup
description: Eliminar un connectorGroup.
ms.openlocfilehash: 3ba4a5a06e25f2fb1568ab9d7d6e92104ea083de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084051"
---
# <a name="delete-connectorgroup"></a><span data-ttu-id="e3cfb-103">Eliminar connectorGroup</span><span class="sxs-lookup"><span data-stu-id="e3cfb-103">Delete connectorGroup</span></span>

> <span data-ttu-id="e3cfb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e3cfb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e3cfb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e3cfb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e3cfb-106">Eliminar un connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="e3cfb-106">Delete a connectorGroup.</span></span>
## <a name="permissions"></a><span data-ttu-id="e3cfb-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e3cfb-107">Permissions</span></span>
<span data-ttu-id="e3cfb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e3cfb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="e3cfb-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e3cfb-110">Permission type</span></span>      | <span data-ttu-id="e3cfb-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e3cfb-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e3cfb-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e3cfb-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e3cfb-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e3cfb-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="e3cfb-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3cfb-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e3cfb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3cfb-115">Not supported.</span></span>    |
|<span data-ttu-id="e3cfb-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e3cfb-116">Application</span></span> | <span data-ttu-id="e3cfb-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e3cfb-117">Directory.ReadWrite.All</span></span> |

> <span data-ttu-id="e3cfb-118">**Nota:** El grupo de conector no debe tener todos los conectores asociados con él.</span><span class="sxs-lookup"><span data-stu-id="e3cfb-118">**Note:** The connector group must not have any connectors associated with it.</span></span>

## <a name="http-request"></a><span data-ttu-id="e3cfb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3cfb-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /connectorGroups/{id}
```
## <a name="request-headers"></a><span data-ttu-id="e3cfb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3cfb-120">Request headers</span></span>
| <span data-ttu-id="e3cfb-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3cfb-121">Name</span></span>       | <span data-ttu-id="e3cfb-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3cfb-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e3cfb-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e3cfb-123">Authorization</span></span>  | <span data-ttu-id="e3cfb-124">Bearer.</span><span class="sxs-lookup"><span data-stu-id="e3cfb-124">Bearer.</span></span> <span data-ttu-id="e3cfb-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e3cfb-125">Required</span></span>|

## <a name="request-body"></a><span data-ttu-id="e3cfb-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e3cfb-126">Request body</span></span>
<span data-ttu-id="e3cfb-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e3cfb-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e3cfb-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3cfb-128">Response</span></span>

<span data-ttu-id="e3cfb-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3cfb-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e3cfb-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3cfb-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e3cfb-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e3cfb-132">Request</span></span>
<span data-ttu-id="e3cfb-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3cfb-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_connectorgroup"
}-->
```http
DELETE https://graph.microsoft.com/{ver}/connectorGroups/{id}
```
##### <a name="response"></a><span data-ttu-id="e3cfb-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3cfb-134">Response</span></span>
<span data-ttu-id="e3cfb-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e3cfb-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete connectorGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
