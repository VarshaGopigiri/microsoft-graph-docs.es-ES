---
title: Crear educationClass
description: Cree una clase. Esto también creará un grupo universal. Cuando se utiliza esta API para crear una clase, agregará propiedades especiales para el grupo, que se va a
localization_priority: Normal
ms.openlocfilehash: 9a9a9b13560530adfe26b83af3025ce85be299c7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880720"
---
# <a name="create-educationclass"></a><span data-ttu-id="04774-105">Crear educationClass</span><span class="sxs-lookup"><span data-stu-id="04774-105">Create educationClass</span></span>

<span data-ttu-id="04774-106">Cree una clase.</span><span class="sxs-lookup"><span data-stu-id="04774-106">Create a new class.</span></span> <span data-ttu-id="04774-107">Esto también creará un grupo universal.</span><span class="sxs-lookup"><span data-stu-id="04774-107">This will also create a universal group.</span></span> <span data-ttu-id="04774-108">Al usar esta API para crear una clase, se agregará propiedades especiales al grupo, que agregará características como, por ejemplo, tareas y un tratamiento especial en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="04774-108">When you use this API to create a class, it will add special properties to the group, which will add features such as assignments and special handling within Microsoft Teams.</span></span>

## <a name="permissions"></a><span data-ttu-id="04774-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="04774-109">Permissions</span></span>
<span data-ttu-id="04774-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="04774-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="04774-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="04774-112">Permission type</span></span>      | <span data-ttu-id="04774-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="04774-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="04774-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="04774-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="04774-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04774-115">Not supported.</span></span>  |
|<span data-ttu-id="04774-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="04774-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="04774-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04774-117">Not supported.</span></span>  |
|<span data-ttu-id="04774-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="04774-118">Application</span></span> | <span data-ttu-id="04774-119">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="04774-119">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="04774-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="04774-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes
```
## <a name="request-headers"></a><span data-ttu-id="04774-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="04774-121">Request headers</span></span>
| <span data-ttu-id="04774-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04774-122">Header</span></span>       | <span data-ttu-id="04774-123">Valor</span><span class="sxs-lookup"><span data-stu-id="04774-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="04774-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="04774-124">Authorization</span></span>  | <span data-ttu-id="04774-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="04774-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="04774-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="04774-127">Content-Type</span></span>  | <span data-ttu-id="04774-128">application/json</span><span class="sxs-lookup"><span data-stu-id="04774-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="04774-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="04774-129">Request body</span></span>
<span data-ttu-id="04774-130">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationClass](../resources/educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="04774-130">In the request body, supply a JSON representation of an [educationClass](../resources/educationclass.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="04774-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04774-131">Response</span></span>
<span data-ttu-id="04774-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04774-132">If successful, this method returns a `201 Created` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="04774-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04774-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="04774-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="04774-134">Request</span></span>
<span data-ttu-id="04774-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04774-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationroot"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/classes
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

##### <a name="response"></a><span data-ttu-id="04774-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04774-136">Response</span></span>
<span data-ttu-id="04774-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04774-137">The following is an example of the response.</span></span> 

><span data-ttu-id="04774-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="04774-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
