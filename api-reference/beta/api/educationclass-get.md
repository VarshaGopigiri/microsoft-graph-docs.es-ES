---
title: Obtener educationClass
description: "  los administradores de grupo representan los profesores en la clase. Si usa el token delegado, el usuario solo verá las clases en las que son miembros."
ms.openlocfilehash: 931c47a0885d8b82411410721fb0729aa250a422
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088071"
---
# <a name="get-educationclass"></a><span data-ttu-id="b1187-104">Obtener educationClass</span><span class="sxs-lookup"><span data-stu-id="b1187-104">Get educationClass</span></span>

> <span data-ttu-id="b1187-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b1187-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b1187-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b1187-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b1187-107">Recupere una clase del sistema.</span><span class="sxs-lookup"><span data-stu-id="b1187-107">Retrieve a class from the system.</span></span> <span data-ttu-id="b1187-108">Una clase es un grupo universal con una propiedad especial que indica al sistema que el grupo es una clase.</span><span class="sxs-lookup"><span data-stu-id="b1187-108">A class is a universal group with a special property that indicates to the system that the group is a class.</span></span> <span data-ttu-id="b1187-109">Los miembros del grupo representan a los alumnos; los administradores representan a los profesores de la clase.</span><span class="sxs-lookup"><span data-stu-id="b1187-109">Group members represent the students;  group admins represent the teachers in the class.</span></span> <span data-ttu-id="b1187-110">Si usa el token delegado, el usuario solo verá las clases en las que son miembros.</span><span class="sxs-lookup"><span data-stu-id="b1187-110">If you're using the delegated token, the user will only see classes in which they are members.</span></span>

## <a name="permissions"></a><span data-ttu-id="b1187-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="b1187-111">Permissions</span></span>
<span data-ttu-id="b1187-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b1187-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b1187-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b1187-114">Permission type</span></span>      | <span data-ttu-id="b1187-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b1187-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b1187-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b1187-116">Delegated (work or school account)</span></span> |  <span data-ttu-id="b1187-117">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="b1187-117">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="b1187-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b1187-118">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="b1187-119">No admitido</span><span class="sxs-lookup"><span data-stu-id="b1187-119">Not supported</span></span>  |
|<span data-ttu-id="b1187-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b1187-120">Application</span></span> | <span data-ttu-id="b1187-121">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b1187-121">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="b1187-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b1187-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b1187-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b1187-123">Optional query parameters</span></span>
<span data-ttu-id="b1187-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1187-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b1187-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b1187-125">Request headers</span></span>
| <span data-ttu-id="b1187-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1187-126">Header</span></span>       | <span data-ttu-id="b1187-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b1187-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b1187-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="b1187-128">Authorization</span></span>  | <span data-ttu-id="b1187-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b1187-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b1187-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b1187-131">Request body</span></span>
<span data-ttu-id="b1187-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b1187-132">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="b1187-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1187-133">Response</span></span>
<span data-ttu-id="b1187-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1187-134">If successful, this method returns a `200 OK` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b1187-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1187-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b1187-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b1187-136">Request</span></span>
<span data-ttu-id="b1187-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b1187-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationclass"
}-->
```http
GET https://graph.microsoft.com/beta/education/classes/11023
```
##### <a name="response"></a><span data-ttu-id="b1187-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1187-138">Response</span></span>
<span data-ttu-id="b1187-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1187-139">The following is an example of the response.</span></span> 

><span data-ttu-id="b1187-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b1187-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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