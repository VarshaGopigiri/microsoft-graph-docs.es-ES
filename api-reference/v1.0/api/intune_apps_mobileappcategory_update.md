# <a name="update-mobileappcategory"></a><span data-ttu-id="273d6-101">Actualizar mobileAppCategory</span><span class="sxs-lookup"><span data-stu-id="273d6-101">Update mobileAppCategory</span></span>

> <span data-ttu-id="273d6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="273d6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="273d6-103">Actualice las propiedades de un objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).</span><span class="sxs-lookup"><span data-stu-id="273d6-103">Update the properties of a [mobileAppCategory](../resources/intune_apps_mobileappcategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="273d6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="273d6-104">Prerequisites</span></span>
<span data-ttu-id="273d6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="273d6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="273d6-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="273d6-107">Permission type</span></span>|<span data-ttu-id="273d6-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="273d6-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="273d6-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="273d6-109">Delegated (work or school account)</span></span>|<span data-ttu-id="273d6-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="273d6-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="273d6-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="273d6-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="273d6-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="273d6-112">Not supported.</span></span>|
|<span data-ttu-id="273d6-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="273d6-113">Application</span></span>|<span data-ttu-id="273d6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="273d6-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="273d6-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="273d6-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppCategories/{mobileAppCategoryId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/categories/{mobileAppCategoryId}
```

## <a name="request-headers"></a><span data-ttu-id="273d6-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="273d6-116">Request headers</span></span>
|<span data-ttu-id="273d6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="273d6-117">Header</span></span>|<span data-ttu-id="273d6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="273d6-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="273d6-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="273d6-119">Authorization</span></span>|<span data-ttu-id="273d6-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="273d6-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="273d6-121">Accept</span><span class="sxs-lookup"><span data-stu-id="273d6-121">Accept</span></span>|<span data-ttu-id="273d6-122">application/json</span><span class="sxs-lookup"><span data-stu-id="273d6-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="273d6-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="273d6-123">Request body</span></span>
<span data-ttu-id="273d6-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).</span><span class="sxs-lookup"><span data-stu-id="273d6-124">In the request body, supply a JSON representation for the [mobileAppCategory](../resources/intune_apps_mobileappcategory.md) object.</span></span>

<span data-ttu-id="273d6-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).</span><span class="sxs-lookup"><span data-stu-id="273d6-125">The following table shows the properties that are required when you create the [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).</span></span>

|<span data-ttu-id="273d6-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="273d6-126">Property</span></span>|<span data-ttu-id="273d6-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="273d6-127">Type</span></span>|<span data-ttu-id="273d6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="273d6-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="273d6-129">id</span><span class="sxs-lookup"><span data-stu-id="273d6-129">id</span></span>|<span data-ttu-id="273d6-130">String</span><span class="sxs-lookup"><span data-stu-id="273d6-130">String</span></span>|<span data-ttu-id="273d6-131">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="273d6-131">The key of the entity.</span></span>|
|<span data-ttu-id="273d6-132">displayName</span><span class="sxs-lookup"><span data-stu-id="273d6-132">displayName</span></span>|<span data-ttu-id="273d6-133">String</span><span class="sxs-lookup"><span data-stu-id="273d6-133">String</span></span>|<span data-ttu-id="273d6-134">El nombre de la categoría de aplicación.</span><span class="sxs-lookup"><span data-stu-id="273d6-134">The name of the app category.</span></span>|
|<span data-ttu-id="273d6-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="273d6-135">lastModifiedDateTime</span></span>|<span data-ttu-id="273d6-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="273d6-136">DateTimeOffset</span></span>|<span data-ttu-id="273d6-137">Fecha y hora de la última modificación de mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="273d6-137">The date and time the mobileAppCategory was last modified.</span></span>|



## <a name="response"></a><span data-ttu-id="273d6-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="273d6-138">Response</span></span>
<span data-ttu-id="273d6-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="273d6-139">If successful, this method returns a `200 OK` response code and an updated [mobileAppCategory](../resources/intune_apps_mobileappcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="273d6-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="273d6-140">Example</span></span>
### <a name="request"></a><span data-ttu-id="273d6-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="273d6-141">Request</span></span>
<span data-ttu-id="273d6-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="273d6-142">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppCategories/{mobileAppCategoryId}
Content-type: application/json
Content-length: 107

{
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```

### <a name="response"></a><span data-ttu-id="273d6-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="273d6-143">Response</span></span>
<span data-ttu-id="273d6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="273d6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








