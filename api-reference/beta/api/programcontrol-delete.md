---
title: Eliminar programControl
description: En AD Azure access revisiones característica, eliminar un objeto programControl.  Esto desvincula una revisión de acceso desde un programa.
localization_priority: Normal
ms.openlocfilehash: 782cc8f336e84f82d937e3180d7de6af69e67e52
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843921"
---
# <a name="delete-programcontrol"></a><span data-ttu-id="6bd7d-104">Eliminar programControl</span><span class="sxs-lookup"><span data-stu-id="6bd7d-104">Delete programControl</span></span>

> <span data-ttu-id="6bd7d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6bd7d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6bd7d-107">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, eliminar un objeto [programControl](../resources/programcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="6bd7d-107">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, delete a [programControl](../resources/programcontrol.md) object.</span></span>  <span data-ttu-id="6bd7d-108">Esto desvincula una revisión de acceso desde un programa.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-108">This unlinks an access review from a program.</span></span>
## <a name="permissions"></a><span data-ttu-id="6bd7d-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="6bd7d-109">Permissions</span></span>
<span data-ttu-id="6bd7d-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6bd7d-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6bd7d-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6bd7d-112">Permission type</span></span>                        | <span data-ttu-id="6bd7d-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6bd7d-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="6bd7d-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6bd7d-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="6bd7d-115">`ProgramControl.ReadWrite.All`.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-115"></span></span>  <span data-ttu-id="6bd7d-116">También debe ser el usuario iniciado en un rol de Active directory que le permita eliminar un programControl.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-116">The signed in user must also be in a directory role which permits them to delete a programControl.</span></span> |
|<span data-ttu-id="6bd7d-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6bd7d-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6bd7d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-118">Not supported.</span></span> |
|<span data-ttu-id="6bd7d-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6bd7d-119">Application</span></span>                            | <span data-ttu-id="6bd7d-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6bd7d-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6bd7d-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /programControls('<id>')
```
## <a name="request-headers"></a><span data-ttu-id="6bd7d-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6bd7d-122">Request headers</span></span>
| <span data-ttu-id="6bd7d-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="6bd7d-123">Name</span></span>         | <span data-ttu-id="6bd7d-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="6bd7d-124">Type</span></span>        | <span data-ttu-id="6bd7d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="6bd7d-125">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="6bd7d-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="6bd7d-126">Authorization</span></span> | <span data-ttu-id="6bd7d-127">string</span><span class="sxs-lookup"><span data-stu-id="6bd7d-127">string</span></span> | <span data-ttu-id="6bd7d-128">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-128">Bearer \{token\}.</span></span> <span data-ttu-id="6bd7d-129">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-129">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6bd7d-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6bd7d-130">Request body</span></span>
<span data-ttu-id="6bd7d-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-131">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="6bd7d-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6bd7d-132">Response</span></span>
<span data-ttu-id="6bd7d-p107">Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-p107">If successful, this method returns a `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6bd7d-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6bd7d-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6bd7d-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6bd7d-136">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_programControl"
}-->
```http
DELETE https://graph.microsoft.com/beta/programControls('7e59d237-2fb0-4e5d-b7bb-d4f9f9129213')
```
##### <a name="response"></a><span data-ttu-id="6bd7d-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6bd7d-137">Response</span></span>
><span data-ttu-id="6bd7d-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6bd7d-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-25 00:00:01 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete programControl",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
