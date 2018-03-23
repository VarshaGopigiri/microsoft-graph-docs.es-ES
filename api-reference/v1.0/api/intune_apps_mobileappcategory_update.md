# <a name="update-mobileappcategory"></a><span data-ttu-id="bfc7a-101">Actualizar mobileAppCategory</span><span class="sxs-lookup"><span data-stu-id="bfc7a-101">Update mobileAppCategory</span></span>

> <span data-ttu-id="bfc7a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bfc7a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bfc7a-103">Actualice las propiedades de un objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).</span><span class="sxs-lookup"><span data-stu-id="bfc7a-103">Update the properties of a [calendar](../resources/intune_apps_mobileappcategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bfc7a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bfc7a-104">Prerequisites</span></span>
<span data-ttu-id="bfc7a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bfc7a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bfc7a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bfc7a-107">Permission type</span></span>|<span data-ttu-id="bfc7a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bfc7a-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bfc7a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bfc7a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="bfc7a-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bfc7a-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="bfc7a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bfc7a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bfc7a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bfc7a-112">Not supported.</span></span>|
|<span data-ttu-id="bfc7a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bfc7a-113">Application</span></span>|<span data-ttu-id="bfc7a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bfc7a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bfc7a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bfc7a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppCategories/{mobileAppCategoryId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/categories/{mobileAppCategoryId}
```

## <a name="request-headers"></a><span data-ttu-id="bfc7a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bfc7a-116">Request headers</span></span>
|<span data-ttu-id="bfc7a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfc7a-117">Header</span></span>|<span data-ttu-id="bfc7a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bfc7a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bfc7a-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="bfc7a-119">Authorization</span></span>|<span data-ttu-id="bfc7a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bfc7a-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="bfc7a-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bfc7a-121">Accept</span></span>|<span data-ttu-id="bfc7a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="bfc7a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bfc7a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bfc7a-123">Request body</span></span>
<span data-ttu-id="bfc7a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).</span><span class="sxs-lookup"><span data-stu-id="bfc7a-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_apps_mobileappcategory.md) object.</span></span>

<span data-ttu-id="bfc7a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).</span><span class="sxs-lookup"><span data-stu-id="bfc7a-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="bfc7a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfc7a-126">Property</span></span>|<span data-ttu-id="bfc7a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfc7a-127">Type</span></span>|<span data-ttu-id="bfc7a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfc7a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bfc7a-129">id</span><span class="sxs-lookup"><span data-stu-id="bfc7a-129">id</span></span>|<span data-ttu-id="bfc7a-130">String</span><span class="sxs-lookup"><span data-stu-id="bfc7a-130">String</span></span>|<span data-ttu-id="bfc7a-131">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bfc7a-131">The key of the entity.</span></span>|
|<span data-ttu-id="bfc7a-132">displayName</span><span class="sxs-lookup"><span data-stu-id="bfc7a-132">displayName</span></span>|<span data-ttu-id="bfc7a-133">String</span><span class="sxs-lookup"><span data-stu-id="bfc7a-133">String</span></span>|<span data-ttu-id="bfc7a-134">El nombre de la categoría de aplicación.</span><span class="sxs-lookup"><span data-stu-id="bfc7a-134">The name of the category.</span></span>|
|<span data-ttu-id="bfc7a-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bfc7a-135">lastModifiedDateTime</span></span>|<span data-ttu-id="bfc7a-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bfc7a-136">DateTimeOffset</span></span>|<span data-ttu-id="bfc7a-137">Fecha y hora de la última modificación de mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="bfc7a-137">The date and time when the attachment was last modified.</span></span>|



## <a name="response"></a><span data-ttu-id="bfc7a-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfc7a-138">Response</span></span>
<span data-ttu-id="bfc7a-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bfc7a-139">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_apps_mobileappcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bfc7a-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfc7a-140">Example</span></span>
### <a name="request"></a><span data-ttu-id="bfc7a-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfc7a-141">Request</span></span>
<span data-ttu-id="bfc7a-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfc7a-142">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppCategories/{mobileAppCategoryId}
Content-type: application/json
Content-length: 107

{
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```

### <a name="response"></a><span data-ttu-id="bfc7a-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfc7a-143">Response</span></span>
<span data-ttu-id="bfc7a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bfc7a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 212

{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "id": "d85d9cee-9cee-d85d-ee9c-5dd8ee9c5dd8",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```



