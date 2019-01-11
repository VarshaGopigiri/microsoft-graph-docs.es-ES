---
title: Obtener educationClass
description: "  los administradores de grupo representan los profesores en la clase. Si usa el token delegado, el usuario solo verá las clases en las que son miembros."
localization_priority: Normal
ms.openlocfilehash: 56717404d996e04c57ff194dafdb8231cf96f55f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849591"
---
# <a name="get-educationclass"></a><span data-ttu-id="2718d-104">Obtener educationClass</span><span class="sxs-lookup"><span data-stu-id="2718d-104">Get educationClass</span></span>

<span data-ttu-id="2718d-105">Recupere una clase del sistema.</span><span class="sxs-lookup"><span data-stu-id="2718d-105">Retrieve a class from the system.</span></span> <span data-ttu-id="2718d-106">Una clase es un grupo universal con una propiedad especial que indica al sistema que el grupo es una clase.</span><span class="sxs-lookup"><span data-stu-id="2718d-106">A class is a universal group with a special property that indicates to the system that the group is a class.</span></span> <span data-ttu-id="2718d-107">Los miembros del grupo representan a los alumnos; los administradores representan a los profesores de la clase.</span><span class="sxs-lookup"><span data-stu-id="2718d-107">Group members represent the students;  group admins represent the teachers in the class.</span></span> <span data-ttu-id="2718d-108">Si usa el token delegado, el usuario solo verá las clases en las que son miembros.</span><span class="sxs-lookup"><span data-stu-id="2718d-108">If you're using the delegated token, the user will only see classes in which they are members.</span></span>

## <a name="permissions"></a><span data-ttu-id="2718d-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="2718d-109">Permissions</span></span>
<span data-ttu-id="2718d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2718d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2718d-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2718d-112">Permission type</span></span>      | <span data-ttu-id="2718d-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2718d-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2718d-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2718d-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="2718d-115">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="2718d-115">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="2718d-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2718d-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="2718d-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="2718d-117">Not supported</span></span>  |
|<span data-ttu-id="2718d-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2718d-118">Application</span></span> | <span data-ttu-id="2718d-119">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2718d-119">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="2718d-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2718d-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2718d-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2718d-121">Optional query parameters</span></span>
<span data-ttu-id="2718d-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2718d-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2718d-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2718d-123">Request headers</span></span>
| <span data-ttu-id="2718d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2718d-124">Header</span></span>       | <span data-ttu-id="2718d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2718d-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2718d-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="2718d-126">Authorization</span></span>  | <span data-ttu-id="2718d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2718d-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2718d-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2718d-129">Request body</span></span>
<span data-ttu-id="2718d-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2718d-130">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="2718d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2718d-131">Response</span></span>
<span data-ttu-id="2718d-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2718d-132">If successful, this method returns a `200 OK` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2718d-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2718d-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2718d-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2718d-134">Request</span></span>
<span data-ttu-id="2718d-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2718d-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationclass"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/classes/{class-id}
```
##### <a name="response"></a><span data-ttu-id="2718d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2718d-136">Response</span></span>
<span data-ttu-id="2718d-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2718d-137">The following is an example of the response.</span></span> 

><span data-ttu-id="2718d-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2718d-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 224

{
  "id": "11023",
  "description": "English Level 2",
  "classCode": "11023",
  "createdBy": {
    "user": {
      "displayName": "Susana Rocha",
      "id": "14012",
    }
  },
  "displayName": "English - Language 2",
  "externalId": "301",
  "externalName": "English Level 1",
  "externalSource": "School of Fine Art",
  "mailNickname": "fineartschool.net "
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
