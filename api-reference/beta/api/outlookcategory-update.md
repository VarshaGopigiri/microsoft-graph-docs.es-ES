---
title: Actualizar categoría de Outlook
description: 'Actualizar la propiedad modificable **color** del objeto outlookCategory especificado. No se puede modificar la propiedad **displayName** '
localization_priority: Normal
ms.openlocfilehash: 55252f376f3314689d3dc7a67b54b4fc00c98c80
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885942"
---
# <a name="update-outlook-category"></a><span data-ttu-id="388a6-104">Actualizar categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="388a6-104">Update Outlook category</span></span>

> <span data-ttu-id="388a6-105">**Importante**: las API de la versión de /beta en Microsoft Graph está en vista preliminar y están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="388a6-105">**Important**: APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="388a6-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="388a6-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="388a6-107">Actualizar la propiedad modificable **color** del objeto [outlookCategory](../resources/outlookcategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="388a6-107">Update the writable property, **color**, of the specified [outlookCategory](../resources/outlookcategory.md) object.</span></span> <span data-ttu-id="388a6-108">No puede modificar la propiedad **displayName** después de haber creado la categoría.</span><span class="sxs-lookup"><span data-stu-id="388a6-108">You cannot modify the **displayName** property once you have created the category.</span></span>

## <a name="permissions"></a><span data-ttu-id="388a6-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="388a6-109">Permissions</span></span>
<span data-ttu-id="388a6-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="388a6-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="388a6-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="388a6-112">Permission type</span></span>      | <span data-ttu-id="388a6-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="388a6-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="388a6-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="388a6-114">Delegated (work or school account)</span></span> | <span data-ttu-id="388a6-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="388a6-115">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="388a6-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="388a6-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="388a6-117">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="388a6-117">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="388a6-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="388a6-118">Application</span></span> | <span data-ttu-id="388a6-119">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="388a6-119">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="388a6-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="388a6-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/outlook/masterCategories/{id}
PATCH /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```

## <a name="request-headers"></a><span data-ttu-id="388a6-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="388a6-121">Request headers</span></span>
| <span data-ttu-id="388a6-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="388a6-122">Name</span></span>      |<span data-ttu-id="388a6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="388a6-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="388a6-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="388a6-124">Authorization</span></span>  | <span data-ttu-id="388a6-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="388a6-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="388a6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="388a6-127">Request body</span></span>
<span data-ttu-id="388a6-p106">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="388a6-p106">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="388a6-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="388a6-131">Property</span></span>     | <span data-ttu-id="388a6-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="388a6-132">Type</span></span>   |<span data-ttu-id="388a6-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="388a6-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="388a6-134">color</span><span class="sxs-lookup"><span data-stu-id="388a6-134">color</span></span>|<span data-ttu-id="388a6-135">String</span><span class="sxs-lookup"><span data-stu-id="388a6-135">String</span></span>|<span data-ttu-id="388a6-136">Constante de color preestablecida que caracteriza a una categoría y a la que se asigna uno de los 25 colores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="388a6-136">A pre-set color constant that characterizes a category, and that is mapped to one of 25 predefined colors.</span></span> |

## <a name="response"></a><span data-ttu-id="388a6-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="388a6-137">Response</span></span>

<span data-ttu-id="388a6-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [outlookCategory](../resources/outlookcategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="388a6-138">If successful, this method returns a `200 OK` response code and updated [outlookCategory](../resources/outlookcategory.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="388a6-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="388a6-139">Example</span></span>
##### <a name="request"></a><span data-ttu-id="388a6-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="388a6-140">Request</span></span>
<span data-ttu-id="388a6-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="388a6-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_outlookcategory"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/outlook/masterCategories('bac262b7-485d-4739-b436-e31467d64fac')
Content-type: application/json
Content-length: 30

{
  "color":"preset15"
}
```
##### <a name="response"></a><span data-ttu-id="388a6-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="388a6-142">Response</span></span>
<span data-ttu-id="388a6-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="388a6-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookCategory"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 251

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories/$entity",
  "id":"bac262b7-485d-4739-b436-e31467d64fac",
  "displayName":"Project expenses",
  "color":"preset15"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update outlookCategory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
