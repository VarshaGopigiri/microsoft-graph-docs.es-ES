---
title: Actualizar una opción de configuración de Active directory
description: Actualizar las propiedades de un objeto de configuración de Active directory específicos.
author: lleonard-msft
ms.openlocfilehash: c4ff2401397b7a89d30f1513c504acaca5c71140
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308830"
---
# <a name="update-a-directory-setting"></a><span data-ttu-id="dba66-103">Actualizar una opción de configuración de Active directory</span><span class="sxs-lookup"><span data-stu-id="dba66-103">Update a directory setting</span></span>

> <span data-ttu-id="dba66-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dba66-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dba66-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dba66-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dba66-106">Actualizar las propiedades de un objeto de configuración de Active directory específicos.</span><span class="sxs-lookup"><span data-stu-id="dba66-106">Update the properties of a specific directory setting object.</span></span>

> <span data-ttu-id="dba66-107">**Nota**: la versión de /beta de esta API es sólo se aplica a los grupos.</span><span class="sxs-lookup"><span data-stu-id="dba66-107">**Note**: The /beta version of this API is only applies to groups.</span></span> <span data-ttu-id="dba66-108">Se ha cambiado la versión /v1.0 de esta API para *Actualizar groupSettings*.</span><span class="sxs-lookup"><span data-stu-id="dba66-108">The /v1.0 version of this API has been renamed to *Update groupSettings*.</span></span>

## <a name="permissions"></a><span data-ttu-id="dba66-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="dba66-109">Permissions</span></span>
<span data-ttu-id="dba66-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dba66-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dba66-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dba66-112">Permission type</span></span>      | <span data-ttu-id="dba66-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dba66-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dba66-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dba66-114">Delegated (work or school account)</span></span> | <span data-ttu-id="dba66-115">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="dba66-115">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="dba66-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dba66-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dba66-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dba66-117">Not supported.</span></span>    |
|<span data-ttu-id="dba66-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dba66-118">Application</span></span> | <span data-ttu-id="dba66-119">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dba66-119">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="dba66-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dba66-120">HTTP request</span></span>
<span data-ttu-id="dba66-121"><!-- { "blockType": "ignored" } -->Actualizar una amplia de inquilinos o configuración específica de grupo.</span><span class="sxs-lookup"><span data-stu-id="dba66-121"><!-- { "blockType": "ignored" } --> Update a tenant-wide or group specific setting.</span></span>
```http
PATCH /settings/{id}
PATCH /groups/{id}/settings/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="dba66-122">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="dba66-122">Optional request headers</span></span>
| <span data-ttu-id="dba66-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="dba66-123">Name</span></span>       | <span data-ttu-id="dba66-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="dba66-124">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="dba66-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="dba66-125">Authorization</span></span>  | <span data-ttu-id="dba66-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dba66-p104">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="dba66-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dba66-128">Request body</span></span>
<span data-ttu-id="dba66-129">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="dba66-129">In the request body, supply the values for relevant fields that should be updated.</span></span> 

| <span data-ttu-id="dba66-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dba66-130">Property</span></span>     | <span data-ttu-id="dba66-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="dba66-131">Type</span></span>   |<span data-ttu-id="dba66-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="dba66-132">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="dba66-133">values</span><span class="sxs-lookup"><span data-stu-id="dba66-133">values</span></span> | <span data-ttu-id="dba66-134">settingValue</span><span class="sxs-lookup"><span data-stu-id="dba66-134">settingValue</span></span> | <span data-ttu-id="dba66-p105">Conjunto actualizado de valores.  NOTA: Debe proporcionar el conjunto de toda la colección. No puede actualizar un único conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="dba66-p105">The updated set of values.  NOTE: You must supply the entire collection set. You cannot update a single set of values.</span></span> |

## <a name="response"></a><span data-ttu-id="dba66-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dba66-138">Response</span></span>

<span data-ttu-id="dba66-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 OK`.</span><span class="sxs-lookup"><span data-stu-id="dba66-139">If successful, this method returns a `204 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="dba66-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dba66-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dba66-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dba66-141">Request</span></span>
<span data-ttu-id="dba66-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dba66-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_directorysetting"
}-->
```http
PATCH https://graph.microsoft.com/beta/settings/{id}
Content-type: application/json
Content-length: 178

{
  "values": [
    {
      "name": "name-value",
      "value": "value-value"
    }
  ]
}
```
##### <a name="response"></a><span data-ttu-id="dba66-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dba66-143">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directorysetting"
} -->
```http
HTTP/1.1 204 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update directorysetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->