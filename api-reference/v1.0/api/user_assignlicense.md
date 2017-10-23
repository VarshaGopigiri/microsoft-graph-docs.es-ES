# <a name="assignlicense"></a><span data-ttu-id="0c68a-101">assignLicense</span><span class="sxs-lookup"><span data-stu-id="0c68a-101">assignLicense</span></span>
<span data-ttu-id="0c68a-p101">Agrega o quita suscripciones del usuario. También puede habilitar y deshabilitar los planes específicos asociados a una suscripción.</span><span class="sxs-lookup"><span data-stu-id="0c68a-p101">Add or remove subscriptions for the user. You can also enable and disable specific plans associated with a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="0c68a-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="0c68a-104">Permissions</span></span>
<span data-ttu-id="0c68a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0c68a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0c68a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0c68a-107">Permission type</span></span>      | <span data-ttu-id="0c68a-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0c68a-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0c68a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0c68a-109">Delegated (work or school account)</span></span> | <span data-ttu-id="0c68a-110">User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0c68a-110">User.ReadWrite.All, Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="0c68a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0c68a-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0c68a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0c68a-112">Not supported.</span></span>    |
|<span data-ttu-id="0c68a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0c68a-113">Application</span></span> | <span data-ttu-id="0c68a-114">User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0c68a-114">User.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0c68a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0c68a-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/assignLicense
```
## <a name="request-headers"></a><span data-ttu-id="0c68a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0c68a-116">Request headers</span></span>
| <span data-ttu-id="0c68a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c68a-117">Header</span></span>       | <span data-ttu-id="0c68a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0c68a-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0c68a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="0c68a-119">Authorization</span></span>  | <span data-ttu-id="0c68a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c68a-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="0c68a-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="0c68a-122">Content-Type</span></span>  | <span data-ttu-id="0c68a-123">application/json</span><span class="sxs-lookup"><span data-stu-id="0c68a-123">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0c68a-124">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="0c68a-124">Request body</span></span>
<span data-ttu-id="0c68a-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="0c68a-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0c68a-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0c68a-126">Parameter</span></span>    | <span data-ttu-id="0c68a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c68a-127">Type</span></span>   |<span data-ttu-id="0c68a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c68a-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0c68a-129">addLicenses</span><span class="sxs-lookup"><span data-stu-id="0c68a-129">addLicenses</span></span>|<span data-ttu-id="0c68a-130">AssignedLicense</span><span class="sxs-lookup"><span data-stu-id="0c68a-130">AssignedLicense</span></span>|<span data-ttu-id="0c68a-p104">Colección de objetos [assignedLicense](../resources/assignedlicense.md) que especifican las licencias que se van a agregar. Puede deshabilitar planes asociados a una licencia estableciendo la propiedad **disabledPlans** en un objeto [assignedLicense](../resources/assignedlicense.md).</span><span class="sxs-lookup"><span data-stu-id="0c68a-p104">A collection of [assignedLicense](../resources/assignedlicense.md) objects that specify the licenses to add. You can disable plans associated with a license by setting the **disabledPlans** property on an [assignedLicense](../resources/assignedlicense.md) object.</span></span>|
|<span data-ttu-id="0c68a-133">removeLicenses</span><span class="sxs-lookup"><span data-stu-id="0c68a-133">removeLicenses</span></span>|<span data-ttu-id="0c68a-134">Guid</span><span class="sxs-lookup"><span data-stu-id="0c68a-134">Guid</span></span>|<span data-ttu-id="0c68a-135">Colección de GUID que identifican las licencias que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="0c68a-135">A collection of GUIDs that identify the licenses to remove.</span></span>|

## <a name="response"></a><span data-ttu-id="0c68a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0c68a-136">Response</span></span>

<span data-ttu-id="0c68a-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0c68a-137">If successful, this method returns `200 OK` response code and [user](../resources/user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0c68a-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c68a-138">Example</span></span>
<span data-ttu-id="0c68a-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0c68a-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0c68a-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0c68a-140">Request</span></span>
<span data-ttu-id="0c68a-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0c68a-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_assignlicense"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/assignLicense
Content-type: application/json
Content-length: 185

{
  "addLicenses": [
    {
      "disabledPlans": [ "11b0131d-43c8-4bbb-b2c8-e80f9a50834a" ],
      "skuId": "skuId-value"
    }
  ],
  "removeLicenses": [ "bea13e0c-3828-4daa-a392-28af7ff61a0f" ]
}
```

##### <a name="response"></a><span data-ttu-id="0c68a-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0c68a-142">Response</span></span>
<span data-ttu-id="0c68a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0c68a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
  "accountEnabled": true,
  "assignedLicenses": [
    {
      "disabledPlans": [ "11b0131d-43c8-4bbb-b2c8-e80f9a50834a" ],
      "skuId": "skuId-value"
    }
  ],
  "assignedPlans": [
    {
      "assignedDateTime": "datetime-value",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "bea13e0c-3828-4daa-a392-28af7ff61a0f"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "companyName": "companyName-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: assignLicense",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
