# <a name="update-educationclass-properties"></a><span data-ttu-id="e2eb4-101">Actualizar propiedades de educationclass</span><span class="sxs-lookup"><span data-stu-id="e2eb4-101">Update educationclass properties</span></span>

<span data-ttu-id="e2eb4-102">Actualice las propiedades de una clase.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-102">Update the properties of a class.</span></span>

## <a name="permissions"></a><span data-ttu-id="e2eb4-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="e2eb4-103">Permissions</span></span>
<span data-ttu-id="e2eb4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e2eb4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e2eb4-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e2eb4-106">Permission type</span></span>      | <span data-ttu-id="e2eb4-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e2eb4-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e2eb4-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e2eb4-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="e2eb4-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-109">Not supported.</span></span>  |
|<span data-ttu-id="e2eb4-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e2eb4-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e2eb4-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-111">Not supported.</span></span>   |
|<span data-ttu-id="e2eb4-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e2eb4-112">Application</span></span> | <span data-ttu-id="e2eb4-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e2eb4-113">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="e2eb4-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e2eb4-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/classes/{id}
```
## <a name="request-headers"></a><span data-ttu-id="e2eb4-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e2eb4-115">Request headers</span></span>
| <span data-ttu-id="e2eb4-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2eb4-116">Header</span></span>       | <span data-ttu-id="e2eb4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e2eb4-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e2eb4-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="e2eb4-118">Authorization</span></span>  | <span data-ttu-id="e2eb4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="e2eb4-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e2eb4-121">Content-Type</span></span>  | <span data-ttu-id="e2eb4-122">application/json</span><span class="sxs-lookup"><span data-stu-id="e2eb4-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e2eb4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e2eb4-123">Request body</span></span>
<span data-ttu-id="e2eb4-124">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-124">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="e2eb4-125">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-125">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="e2eb4-126">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-126">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e2eb4-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2eb4-127">Property</span></span>     | <span data-ttu-id="e2eb4-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2eb4-128">Type</span></span>   |<span data-ttu-id="e2eb4-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2eb4-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e2eb4-130">description</span><span class="sxs-lookup"><span data-stu-id="e2eb4-130">description</span></span>|<span data-ttu-id="e2eb4-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2eb4-131">String</span></span>| <span data-ttu-id="e2eb4-132">Descripción de la clase</span><span class="sxs-lookup"><span data-stu-id="e2eb4-132">Description of the class.</span></span>|
|<span data-ttu-id="e2eb4-133">displayName</span><span class="sxs-lookup"><span data-stu-id="e2eb4-133">displayName</span></span>|<span data-ttu-id="e2eb4-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2eb4-134">String</span></span>| <span data-ttu-id="e2eb4-135">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-135">Name of the class.</span></span>|
|<span data-ttu-id="e2eb4-136">mailNickname</span><span class="sxs-lookup"><span data-stu-id="e2eb4-136">mailNickname</span></span>|<span data-ttu-id="e2eb4-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2eb4-137">String</span></span>| <span data-ttu-id="e2eb4-138">Alias de correo electrónico para enviar correo electrónico a todos los usuarios si esa característica está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-138">Email alias for sending email to all users if that feature is enabled.</span></span> |
<span data-ttu-id="e2eb4-139"><!-- Please verify the revised description here. --> |classCode|String| Código de clase que usa el centro educativo.| |externalId|String| Identificador de la clase en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-139"><!-- Please verify the revised description here. -->|classCode|String| Class code used by the school.| |externalId|String| ID of the class from the syncing system.</span></span> <span data-ttu-id="e2eb4-140">| |externalName|String|Nombre de la clase en el sistema de sincronización.| |externalSource|string| Forma en que se ha creado la clase.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-140">| |externalName|String|Name of the class in the syncing system.| |externalSource|string| How this class was created.</span></span> <span data-ttu-id="e2eb4-141">Los valores posibles son: `sis`, `manual` y `enum_sentinel`.|</span><span class="sxs-lookup"><span data-stu-id="e2eb4-141">The possible values are , , , , , , , , , , , or .</span></span>

## <a name="response"></a><span data-ttu-id="e2eb4-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2eb4-142">Response</span></span>
<span data-ttu-id="e2eb4-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationClass](../resources/educationclass.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-143">If successful, this method returns a `200 OK` response code and an updated [educationClass](../resources/educationclass.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e2eb4-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2eb4-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e2eb4-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e2eb4-145">Request</span></span>
<span data-ttu-id="e2eb4-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-146">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationclass"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/education/classes/{class-id}
Content-type: application/json
Content-length: 224

{
  "description": "History - World History 1",
  "displayName": "World History Level 1",
}
```
##### <a name="response"></a><span data-ttu-id="e2eb4-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2eb4-147">Response</span></span>
<span data-ttu-id="e2eb4-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-148">The following is an example of the response.</span></span> 

><span data-ttu-id="e2eb4-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e2eb4-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
  "id": "11014",
  "description": "World History Level 1",
  "classCode": "301",
  "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
  "displayName": "History - World History 1",
  "externalId": "301",
  "externalName": "World History Level 1",
  "externalSource": "Fabrikam High School",
  "mailNickname": "Fabrikam"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationclass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->