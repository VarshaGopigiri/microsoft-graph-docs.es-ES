# <a name="update-educationclass-properties"></a><span data-ttu-id="a4dfd-101">Actualizar propiedades de educationclass</span><span class="sxs-lookup"><span data-stu-id="a4dfd-101">Update educationclass properties</span></span>

<span data-ttu-id="a4dfd-102">Actualice las propiedades de una clase.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-102">Update the properties of a registered device.</span></span>

## <a name="permissions"></a><span data-ttu-id="a4dfd-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a4dfd-103">Permissions</span></span>
<span data-ttu-id="a4dfd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a4dfd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a4dfd-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4dfd-106">Permission type</span></span>      | <span data-ttu-id="a4dfd-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4dfd-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a4dfd-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4dfd-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="a4dfd-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-109">Not supported.</span></span>  |
|<span data-ttu-id="a4dfd-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4dfd-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a4dfd-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-111">Not supported.</span></span>   |
|<span data-ttu-id="a4dfd-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4dfd-112">Application</span></span> | <span data-ttu-id="a4dfd-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a4dfd-113">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="a4dfd-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4dfd-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/classes/{id}
```
## <a name="request-headers"></a><span data-ttu-id="a4dfd-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4dfd-115">Request headers</span></span>
| <span data-ttu-id="a4dfd-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4dfd-116">Header</span></span>       | <span data-ttu-id="a4dfd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a4dfd-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a4dfd-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="a4dfd-118">Authorization</span></span>  | <span data-ttu-id="a4dfd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a4dfd-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a4dfd-121">Content-Type</span></span>  | <span data-ttu-id="a4dfd-122">application/json</span><span class="sxs-lookup"><span data-stu-id="a4dfd-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a4dfd-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4dfd-123">Request body</span></span>
<span data-ttu-id="a4dfd-124">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-124">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="a4dfd-125">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-125">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="a4dfd-126">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-126">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="a4dfd-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4dfd-127">Property</span></span>     | <span data-ttu-id="a4dfd-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4dfd-128">Type</span></span>   |<span data-ttu-id="a4dfd-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4dfd-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a4dfd-130">description</span><span class="sxs-lookup"><span data-stu-id="a4dfd-130">description</span></span>|<span data-ttu-id="a4dfd-131">String</span><span class="sxs-lookup"><span data-stu-id="a4dfd-131">String</span></span>| <span data-ttu-id="a4dfd-132">Descripción de la clase</span><span class="sxs-lookup"><span data-stu-id="a4dfd-132">Description of the template.</span></span>|
|<span data-ttu-id="a4dfd-133">displayName</span><span class="sxs-lookup"><span data-stu-id="a4dfd-133">displayName</span></span>|<span data-ttu-id="a4dfd-134">String</span><span class="sxs-lookup"><span data-stu-id="a4dfd-134">String</span></span>| <span data-ttu-id="a4dfd-135">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-135">Name of the class.</span></span>|
|<span data-ttu-id="a4dfd-136">mailNickname</span><span class="sxs-lookup"><span data-stu-id="a4dfd-136">mailNickname</span></span>|<span data-ttu-id="a4dfd-137">String</span><span class="sxs-lookup"><span data-stu-id="a4dfd-137">String</span></span>| <span data-ttu-id="a4dfd-138">Alias de correo electrónico para enviar correo electrónico a todos los usuarios si esa característica está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-138">Email alias for sending email to all users if that feature is enabled.</span></span> |
<!-- Please verify the revised description here. -->
<span data-ttu-id="a4dfd-139">|classCode|String| Código de clase que usa el centro educativo.| |externalId|String| Identificador de la clase en el sistema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-139">|classCode|String| Class code used by the school.| |externalId|String| ID of the class from the syncing system.</span></span> <span data-ttu-id="a4dfd-140">| |externalName|String|Nombre de la clase en el sistema de sincronización.| |externalSource|string| Forma en que se ha creado la clase.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-140">| |externalName|String|Name of the class in the syncing system.| |externalSource|string| How this class was created.</span></span> <span data-ttu-id="a4dfd-141">Los valores posibles son: `sis`, `manual` y `enum_sentinel`.|</span><span class="sxs-lookup"><span data-stu-id="a4dfd-141">Possible values are: `sis`, `manual`, `enum_sentinel`.</span></span>

## <a name="response"></a><span data-ttu-id="a4dfd-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4dfd-142">Response</span></span>
<span data-ttu-id="a4dfd-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationClass](../resources/educationclass.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-143">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/educationclass.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a4dfd-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4dfd-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a4dfd-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4dfd-145">Request</span></span>
<span data-ttu-id="a4dfd-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-146">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_educationclass"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/education/classes/11014
Content-type: application/json
Content-length: 224

{
  "description": "History - World History 1",
  "displayName": "World History Level 1",
}
```
##### <a name="response"></a><span data-ttu-id="a4dfd-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4dfd-147">Response</span></span>
<span data-ttu-id="a4dfd-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-148">The following is an example of the response.</span></span> 

><span data-ttu-id="a4dfd-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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