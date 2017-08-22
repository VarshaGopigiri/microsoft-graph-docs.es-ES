# <a name="assignlicense"></a><span data-ttu-id="90069-101">assignLicense</span><span class="sxs-lookup"><span data-stu-id="90069-101">assignLicense</span></span>
<span data-ttu-id="90069-p101">Agrega o quita suscripciones del usuario. También puede habilitar y deshabilitar los planes específicos asociados a una suscripción.</span><span class="sxs-lookup"><span data-stu-id="90069-p101">Add or remove subscriptions for the user. You can also enable and disable specific plans associated with a subscription.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="90069-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="90069-104">Prerequisites</span></span>
<span data-ttu-id="90069-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *User.ReadWrite.All; Directory.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="90069-105">One of the following **scopes** is required to execute this API: *User.ReadWrite.All; Directory.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="90069-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90069-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/assignLicense
```
## <a name="request-headers"></a><span data-ttu-id="90069-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90069-107">Request headers</span></span>
| <span data-ttu-id="90069-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90069-108">Header</span></span>       | <span data-ttu-id="90069-109">Valor</span><span class="sxs-lookup"><span data-stu-id="90069-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="90069-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="90069-110">Authorization</span></span>  | <span data-ttu-id="90069-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90069-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="90069-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="90069-113">Content-Type</span></span>  | <span data-ttu-id="90069-114">application/json</span><span class="sxs-lookup"><span data-stu-id="90069-114">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="90069-115">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="90069-115">Request body</span></span>
<span data-ttu-id="90069-116">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="90069-116">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="90069-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="90069-117">Parameter</span></span>    | <span data-ttu-id="90069-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="90069-118">Type</span></span>   |<span data-ttu-id="90069-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="90069-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="90069-120">addLicenses</span><span class="sxs-lookup"><span data-stu-id="90069-120">addLicenses</span></span>|<span data-ttu-id="90069-121">AssignedLicense</span><span class="sxs-lookup"><span data-stu-id="90069-121">AssignedLicense</span></span>|<span data-ttu-id="90069-p103">Colección de objetos [assignedLicense](../resources/assignedlicense.md) que especifican las licencias que se van a agregar. Puede deshabilitar planes asociados a una licencia estableciendo la propiedad **disabledPlans** en un objeto [assignedLicense](../resources/assignedlicense.md).</span><span class="sxs-lookup"><span data-stu-id="90069-p103">A collection of [assignedLicense](../resources/assignedlicense.md) objects that specify the licenses to add. You can disable plans associated with a license by setting the **disabledPlans** property on an [assignedLicense](../resources/assignedlicense.md) object.</span></span>|
|<span data-ttu-id="90069-124">removeLicenses</span><span class="sxs-lookup"><span data-stu-id="90069-124">removeLicenses</span></span>|<span data-ttu-id="90069-125">Guid</span><span class="sxs-lookup"><span data-stu-id="90069-125">Guid</span></span>|<span data-ttu-id="90069-126">Colección de GUID que identifican las licencias que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="90069-126">A collection of GUIDs that identify the licenses to remove.</span></span>|

## <a name="response"></a><span data-ttu-id="90069-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90069-127">Response</span></span>

<span data-ttu-id="90069-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200, OK` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90069-128">If successful, this method returns `200, OK` response code and [user](../resources/user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90069-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90069-129">Example</span></span>
<span data-ttu-id="90069-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="90069-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="90069-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90069-131">Request</span></span>
<span data-ttu-id="90069-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90069-132">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="90069-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90069-133">Response</span></span>
<span data-ttu-id="90069-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90069-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
