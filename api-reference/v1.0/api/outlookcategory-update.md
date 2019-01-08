---
title: Actualizar categoría de Outlook
description: 'Actualizar la propiedad modificable **color** del objeto outlookCategory especificado. No se puede modificar la propiedad **displayName** '
ms.openlocfilehash: c69dc260127938bd4afa33e7406ac38862ef837d
ms.sourcegitcommit: 37591c2299c80e7675cd2b5f781e1eeeba628a60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27748251"
---
# <a name="update-outlook-category"></a><span data-ttu-id="42702-104">Actualizar categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="42702-104">Update Outlook category</span></span>


<span data-ttu-id="42702-105">Actualizar la propiedad modificable **color** del objeto [outlookCategory](../resources/outlookcategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="42702-105">Update the writable property, **color**, of the specified [outlookCategory](../resources/outlookcategory.md) object.</span></span> <span data-ttu-id="42702-106">No puede modificar la propiedad **displayName** después de haber creado la categoría.</span><span class="sxs-lookup"><span data-stu-id="42702-106">You cannot modify the **displayName** property once you have created the category.</span></span>

## <a name="permissions"></a><span data-ttu-id="42702-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="42702-107">Permissions</span></span>
<span data-ttu-id="42702-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="42702-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="42702-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="42702-110">Permission type</span></span>      | <span data-ttu-id="42702-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="42702-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="42702-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="42702-112">Delegated (work or school account)</span></span> | <span data-ttu-id="42702-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="42702-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="42702-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="42702-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="42702-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="42702-115">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="42702-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="42702-116">Application</span></span> | <span data-ttu-id="42702-117">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="42702-117">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="42702-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="42702-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/outlook/masterCategories/{id}
PATCH /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```

## <a name="request-headers"></a><span data-ttu-id="42702-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="42702-119">Request headers</span></span>
| <span data-ttu-id="42702-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="42702-120">Name</span></span>      |<span data-ttu-id="42702-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="42702-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="42702-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="42702-122">Authorization</span></span>  | <span data-ttu-id="42702-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="42702-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="42702-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="42702-125">Request body</span></span>
<span data-ttu-id="42702-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="42702-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="42702-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="42702-129">Property</span></span>     | <span data-ttu-id="42702-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="42702-130">Type</span></span>   |<span data-ttu-id="42702-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="42702-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="42702-132">color</span><span class="sxs-lookup"><span data-stu-id="42702-132">color</span></span>|<span data-ttu-id="42702-133">String</span><span class="sxs-lookup"><span data-stu-id="42702-133">String</span></span>|<span data-ttu-id="42702-134">Constante de color preestablecida que caracteriza a una categoría y a la que se asigna uno de los 25 colores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="42702-134">A pre-set color constant that characterizes a category, and that is mapped to one of 25 predefined colors.</span></span> |

## <a name="response"></a><span data-ttu-id="42702-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42702-135">Response</span></span>

<span data-ttu-id="42702-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [outlookCategory](../resources/outlookcategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="42702-136">If successful, this method returns a `200 OK` response code and updated [outlookCategory](../resources/outlookcategory.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="42702-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="42702-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="42702-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="42702-138">Request</span></span>
<span data-ttu-id="42702-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="42702-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["bac262b7-485d-4739-b436-e31467d64fac"],
  "name": "update_outlookcategory"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/outlook/masterCategories/bac262b7-485d-4739-b436-e31467d64fac
Content-type: application/json
Content-length: 30

{
  "color":"preset15"
}
```
##### <a name="response"></a><span data-ttu-id="42702-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42702-140">Response</span></span>
<span data-ttu-id="42702-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="42702-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories/$entity",
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