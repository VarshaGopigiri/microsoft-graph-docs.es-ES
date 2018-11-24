# <a name="update-deviceenrollmentlimitconfiguration"></a><span data-ttu-id="16a2f-101">Actualizar deviceEnrollmentLimitConfiguration</span><span class="sxs-lookup"><span data-stu-id="16a2f-101">Update deviceEnrollmentLimitConfiguration</span></span>

> <span data-ttu-id="16a2f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16a2f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16a2f-103">Actualice las propiedades de un objeto [deviceEnrollmentLimitConfiguration](../resources/intune_onboarding_deviceenrollmentlimitconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="16a2f-103">Update the properties of a [deviceEnrollmentLimitConfiguration](../resources/intune_onboarding_deviceenrollmentlimitconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="16a2f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="16a2f-104">Prerequisites</span></span>
<span data-ttu-id="16a2f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="16a2f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="16a2f-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="16a2f-107">Permission type</span></span>|<span data-ttu-id="16a2f-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="16a2f-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="16a2f-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="16a2f-109">Delegated (work or school account)</span></span>|<span data-ttu-id="16a2f-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="16a2f-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="16a2f-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="16a2f-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="16a2f-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16a2f-112">Not supported.</span></span>|
|<span data-ttu-id="16a2f-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="16a2f-113">Application</span></span>|<span data-ttu-id="16a2f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16a2f-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="16a2f-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="16a2f-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="16a2f-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="16a2f-116">Request headers</span></span>
|<span data-ttu-id="16a2f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16a2f-117">Header</span></span>|<span data-ttu-id="16a2f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="16a2f-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="16a2f-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="16a2f-119">Authorization</span></span>|<span data-ttu-id="16a2f-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="16a2f-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="16a2f-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="16a2f-121">Accept</span></span>|<span data-ttu-id="16a2f-122">application/json</span><span class="sxs-lookup"><span data-stu-id="16a2f-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="16a2f-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="16a2f-123">Request body</span></span>
<span data-ttu-id="16a2f-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentLimitConfiguration](../resources/intune_onboarding_deviceenrollmentlimitconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="16a2f-124">In the request body, supply a JSON representation for the [deviceEnrollmentLimitConfiguration](../resources/intune_onboarding_deviceenrollmentlimitconfiguration.md) object.</span></span>

<span data-ttu-id="16a2f-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentLimitConfiguration](../resources/intune_onboarding_deviceenrollmentlimitconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="16a2f-125">The following table shows the properties that are required when you create the [deviceEnrollmentLimitConfiguration](../resources/intune_onboarding_deviceenrollmentlimitconfiguration.md).</span></span>

|<span data-ttu-id="16a2f-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16a2f-126">Property</span></span>|<span data-ttu-id="16a2f-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="16a2f-127">Type</span></span>|<span data-ttu-id="16a2f-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="16a2f-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16a2f-129">id</span><span class="sxs-lookup"><span data-stu-id="16a2f-129">id</span></span>|<span data-ttu-id="16a2f-130">String</span><span class="sxs-lookup"><span data-stu-id="16a2f-130">String</span></span>|<span data-ttu-id="16a2f-131">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16a2f-131">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="16a2f-132">displayName</span><span class="sxs-lookup"><span data-stu-id="16a2f-132">displayName</span></span>|<span data-ttu-id="16a2f-133">String</span><span class="sxs-lookup"><span data-stu-id="16a2f-133">String</span></span>|<span data-ttu-id="16a2f-134">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16a2f-134">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="16a2f-135">description</span><span class="sxs-lookup"><span data-stu-id="16a2f-135">description</span></span>|<span data-ttu-id="16a2f-136">String</span><span class="sxs-lookup"><span data-stu-id="16a2f-136">String</span></span>|<span data-ttu-id="16a2f-137">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16a2f-137">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="16a2f-138">prioridad</span><span class="sxs-lookup"><span data-stu-id="16a2f-138">priority</span></span>|<span data-ttu-id="16a2f-139">Int32</span><span class="sxs-lookup"><span data-stu-id="16a2f-139">Int32</span></span>|<span data-ttu-id="16a2f-140">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16a2f-140">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="16a2f-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="16a2f-141">createdDateTime</span></span>|<span data-ttu-id="16a2f-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16a2f-142">DateTimeOffset</span></span>|<span data-ttu-id="16a2f-143">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16a2f-143">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="16a2f-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="16a2f-144">lastModifiedDateTime</span></span>|<span data-ttu-id="16a2f-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16a2f-145">DateTimeOffset</span></span>|<span data-ttu-id="16a2f-146">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16a2f-146">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="16a2f-147">version</span><span class="sxs-lookup"><span data-stu-id="16a2f-147">version</span></span>|<span data-ttu-id="16a2f-148">Int32</span><span class="sxs-lookup"><span data-stu-id="16a2f-148">Int32</span></span>|<span data-ttu-id="16a2f-149">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="16a2f-149">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="16a2f-150">límite</span><span class="sxs-lookup"><span data-stu-id="16a2f-150">limit</span></span>|<span data-ttu-id="16a2f-151">Int32</span><span class="sxs-lookup"><span data-stu-id="16a2f-151">Int32</span></span>|<span data-ttu-id="16a2f-152">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="16a2f-152">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="16a2f-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16a2f-153">Response</span></span>
<span data-ttu-id="16a2f-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentLimitConfiguration](../resources/intune_onboarding_deviceenrollmentlimitconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16a2f-154">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentLimitConfiguration](../resources/intune_onboarding_deviceenrollmentlimitconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="16a2f-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="16a2f-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="16a2f-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16a2f-156">Request</span></span>
<span data-ttu-id="16a2f-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16a2f-157">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
Content-type: application/json
Content-length: 205

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentLimitConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "version": 7,
  "limit": 5
}
```

### <a name="response"></a><span data-ttu-id="16a2f-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16a2f-158">Response</span></span>
<span data-ttu-id="16a2f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="16a2f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 377

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentLimitConfiguration",
  "id": "4f8c4e4c-4e4c-4f8c-4c4e-8c4f4c4e8c4f",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "limit": 5
}
```



