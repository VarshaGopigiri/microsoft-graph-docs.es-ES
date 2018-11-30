---
title: Crear educationClass
description: Cree una clase. Esto también creará un grupo universal. Cuando se utiliza esta API para crear una clase, agregará propiedades especiales para el grupo, que se va a
ms.openlocfilehash: 81b72b5b252c323a6a91152deaafaf8a927c8bf9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083029"
---
# <a name="create-educationclass"></a><span data-ttu-id="64e83-105">Crear educationClass</span><span class="sxs-lookup"><span data-stu-id="64e83-105">Create educationClass</span></span>

> <span data-ttu-id="64e83-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="64e83-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="64e83-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="64e83-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="64e83-108">Cree una clase.</span><span class="sxs-lookup"><span data-stu-id="64e83-108">Create a new class.</span></span> <span data-ttu-id="64e83-109">Esto también creará un grupo universal.</span><span class="sxs-lookup"><span data-stu-id="64e83-109">This will also create a universal group.</span></span> <span data-ttu-id="64e83-110">Al usar esta API para crear una clase, se agregará propiedades especiales al grupo, que agregará características como, por ejemplo, tareas y un tratamiento especial en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="64e83-110">When you use this API to create a class, it will add special properties to the group, which will add features such as assignments and special handling within Microsoft Teams.</span></span>

## <a name="permissions"></a><span data-ttu-id="64e83-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="64e83-111">Permissions</span></span>
<span data-ttu-id="64e83-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="64e83-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="64e83-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="64e83-114">Permission type</span></span>      | <span data-ttu-id="64e83-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="64e83-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="64e83-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="64e83-116">Delegated (work or school account)</span></span> |  <span data-ttu-id="64e83-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="64e83-117">Not supported.</span></span>  |
|<span data-ttu-id="64e83-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="64e83-118">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="64e83-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="64e83-119">Not supported.</span></span>  |
|<span data-ttu-id="64e83-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="64e83-120">Application</span></span> | <span data-ttu-id="64e83-121">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="64e83-121">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="64e83-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="64e83-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes
```
## <a name="request-headers"></a><span data-ttu-id="64e83-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="64e83-123">Request headers</span></span>
| <span data-ttu-id="64e83-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64e83-124">Header</span></span>       | <span data-ttu-id="64e83-125">Valor</span><span class="sxs-lookup"><span data-stu-id="64e83-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="64e83-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="64e83-126">Authorization</span></span>  | <span data-ttu-id="64e83-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64e83-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="64e83-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="64e83-129">Content-Type</span></span>  | <span data-ttu-id="64e83-130">application/json</span><span class="sxs-lookup"><span data-stu-id="64e83-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="64e83-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="64e83-131">Request body</span></span>
<span data-ttu-id="64e83-132">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationClass](../resources/educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="64e83-132">In the request body, supply a JSON representation of an [educationClass](../resources/educationclass.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="64e83-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64e83-133">Response</span></span>
<span data-ttu-id="64e83-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64e83-134">If successful, this method returns a `201 Created` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="64e83-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64e83-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="64e83-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="64e83-136">Request</span></span>
<span data-ttu-id="64e83-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64e83-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationroot"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes
Content-type: application/json
Content-length: 224

{
  "description": "Health Level 1",
  "classCode": "Health 501",
  "displayName": "Health 1",
  "externalId": "11019",
  "externalName": "Health Level 1",
  "externalSource": "sis",
  "mailNickname": "fineartschool.net"
}
```

##### <a name="response"></a><span data-ttu-id="64e83-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64e83-138">Response</span></span>
<span data-ttu-id="64e83-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64e83-139">The following is an example of the response.</span></span> 

><span data-ttu-id="64e83-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="64e83-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 224

{
    "id": "11019",
    "description": "Health Level 1",
    "classCode": "Health 501",
    "createdBy": {
      "user": {
        "displayName": "Susana Rocha",
        "id": "14012",
      }
    },
    "displayName": "Health 1",
    "externalId": "11019",
    "externalName": "Health Level 1",
    "externalSource": "sis",
    "mailNickname": "fineartschool.net"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->