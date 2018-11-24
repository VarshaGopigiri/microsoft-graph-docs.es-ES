# <a name="create-androidworkprofilecustomconfiguration"></a><span data-ttu-id="06824-101">Crear androidWorkProfileCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="06824-101">Create androidWorkProfileCustomConfiguration</span></span>

> <span data-ttu-id="06824-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="06824-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="06824-103">Crear un nuevo objeto [androidWorkProfileCustomConfiguration](../resources/intune_deviceconfig_androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="06824-103">Create a new [androidWorkProfileCustomConfiguration](../resources/intune_deviceconfig_androidworkprofilecustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="06824-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="06824-104">Prerequisites</span></span>
<span data-ttu-id="06824-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="06824-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="06824-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="06824-107">Permission type</span></span>|<span data-ttu-id="06824-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="06824-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="06824-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="06824-109">Delegated (work or school account)</span></span>|<span data-ttu-id="06824-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="06824-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="06824-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="06824-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="06824-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06824-112">Not supported.</span></span>|
|<span data-ttu-id="06824-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="06824-113">Application</span></span>|<span data-ttu-id="06824-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06824-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="06824-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="06824-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="06824-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="06824-116">Request headers</span></span>
|<span data-ttu-id="06824-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06824-117">Header</span></span>|<span data-ttu-id="06824-118">Valor</span><span class="sxs-lookup"><span data-stu-id="06824-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="06824-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="06824-119">Authorization</span></span>|<span data-ttu-id="06824-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="06824-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="06824-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="06824-121">Accept</span></span>|<span data-ttu-id="06824-122">application/json</span><span class="sxs-lookup"><span data-stu-id="06824-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="06824-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="06824-123">Request body</span></span>
<span data-ttu-id="06824-124">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidWorkProfileCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="06824-124">In the request body, supply a JSON representation for the androidWorkProfileCustomConfiguration object.</span></span>

<span data-ttu-id="06824-125">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidWorkProfileCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="06824-125">The following table shows the properties that are required when you create the androidWorkProfileCustomConfiguration.</span></span>

|<span data-ttu-id="06824-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06824-126">Property</span></span>|<span data-ttu-id="06824-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="06824-127">Type</span></span>|<span data-ttu-id="06824-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="06824-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="06824-129">id</span><span class="sxs-lookup"><span data-stu-id="06824-129">id</span></span>|<span data-ttu-id="06824-130">String</span><span class="sxs-lookup"><span data-stu-id="06824-130">String</span></span>|<span data-ttu-id="06824-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="06824-131">Key of the entity.</span></span> <span data-ttu-id="06824-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06824-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06824-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="06824-133">lastModifiedDateTime</span></span>|<span data-ttu-id="06824-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="06824-134">DateTimeOffset</span></span>|<span data-ttu-id="06824-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="06824-135">DateTime the object was last modified.</span></span> <span data-ttu-id="06824-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06824-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06824-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="06824-137">createdDateTime</span></span>|<span data-ttu-id="06824-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="06824-138">DateTimeOffset</span></span>|<span data-ttu-id="06824-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="06824-139">DateTime the object was created.</span></span> <span data-ttu-id="06824-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06824-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06824-141">descripción</span><span class="sxs-lookup"><span data-stu-id="06824-141">description</span></span>|<span data-ttu-id="06824-142">String</span><span class="sxs-lookup"><span data-stu-id="06824-142">String</span></span>|<span data-ttu-id="06824-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06824-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="06824-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06824-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06824-145">displayName</span><span class="sxs-lookup"><span data-stu-id="06824-145">displayName</span></span>|<span data-ttu-id="06824-146">String</span><span class="sxs-lookup"><span data-stu-id="06824-146">String</span></span>|<span data-ttu-id="06824-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06824-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="06824-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06824-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06824-149">version</span><span class="sxs-lookup"><span data-stu-id="06824-149">version</span></span>|<span data-ttu-id="06824-150">Int32</span><span class="sxs-lookup"><span data-stu-id="06824-150">Int32</span></span>|<span data-ttu-id="06824-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06824-151">Version of the device configuration.</span></span> <span data-ttu-id="06824-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06824-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06824-153">omaSettings</span><span class="sxs-lookup"><span data-stu-id="06824-153">omaSettings</span></span>|<span data-ttu-id="06824-154">Colección [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="06824-154">[omaSetting](../resources/intune_deviceconfig_omasetting.md) collection</span></span>|<span data-ttu-id="06824-155">Configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="06824-155">OMA settings.</span></span> <span data-ttu-id="06824-156">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="06824-156">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="06824-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06824-157">Response</span></span>
<span data-ttu-id="06824-158">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidWorkProfileCustomConfiguration](../resources/intune_deviceconfig_androidworkprofilecustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06824-158">If successful, this method returns a `201 Created` response code and a [androidWorkProfileCustomConfiguration](../resources/intune_deviceconfig_androidworkprofilecustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="06824-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06824-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="06824-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="06824-160">Request</span></span>
<span data-ttu-id="06824-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06824-161">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 413

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSettingInteger",
      "displayName": "Display Name value",
      "description": "Description value",
      "omaUri": "Oma Uri value",
      "value": 5
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="06824-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06824-162">Response</span></span>
<span data-ttu-id="06824-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="06824-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 585

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
  "id": "76c5d59b-d59b-76c5-9bd5-c5769bd5c576",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSettingInteger",
      "displayName": "Display Name value",
      "description": "Description value",
      "omaUri": "Oma Uri value",
      "value": 5
    }
  ]
}
```



