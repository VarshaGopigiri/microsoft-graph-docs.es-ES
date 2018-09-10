# <a name="update-softwareupdatestatussummary"></a><span data-ttu-id="d42b8-101">Actualizar softwareUpdateStatusSummary</span><span class="sxs-lookup"><span data-stu-id="d42b8-101">Update softwareUpdateStatusSummary</span></span>

> <span data-ttu-id="d42b8-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d42b8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d42b8-103">Actualice las propiedades de un objeto [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="d42b8-103">Update the properties of a [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d42b8-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d42b8-104">Prerequisites</span></span>
<span data-ttu-id="d42b8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d42b8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d42b8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d42b8-107">Permission type</span></span>|<span data-ttu-id="d42b8-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d42b8-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d42b8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d42b8-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d42b8-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d42b8-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d42b8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d42b8-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d42b8-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d42b8-112">Not supported.</span></span>|
|<span data-ttu-id="d42b8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d42b8-113">Application</span></span>|<span data-ttu-id="d42b8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d42b8-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d42b8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d42b8-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/softwareUpdateStatusSummary
```

## <a name="request-headers"></a><span data-ttu-id="d42b8-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d42b8-116">Request headers</span></span>
|<span data-ttu-id="d42b8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d42b8-117">Header</span></span>|<span data-ttu-id="d42b8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d42b8-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d42b8-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d42b8-119">Authorization</span></span>|<span data-ttu-id="d42b8-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d42b8-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d42b8-121">Accept</span><span class="sxs-lookup"><span data-stu-id="d42b8-121">Accept</span></span>|<span data-ttu-id="d42b8-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d42b8-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d42b8-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d42b8-123">Request body</span></span>
<span data-ttu-id="d42b8-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="d42b8-124">In the request body, supply a JSON representation for the [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md) object.</span></span>

<span data-ttu-id="d42b8-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="d42b8-125">The following table shows the properties that are required when you create the [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md).</span></span>

|<span data-ttu-id="d42b8-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d42b8-126">Property</span></span>|<span data-ttu-id="d42b8-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d42b8-127">Type</span></span>|<span data-ttu-id="d42b8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d42b8-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d42b8-129">id</span><span class="sxs-lookup"><span data-stu-id="d42b8-129">id</span></span>|<span data-ttu-id="d42b8-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="d42b8-130">String</span></span>|<span data-ttu-id="d42b8-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d42b8-131">Key of the entity.</span></span>|
|<span data-ttu-id="d42b8-132">displayName</span><span class="sxs-lookup"><span data-stu-id="d42b8-132">displayName</span></span>|<span data-ttu-id="d42b8-133">String</span><span class="sxs-lookup"><span data-stu-id="d42b8-133">String</span></span>|<span data-ttu-id="d42b8-134">El nombre de la directiva.</span><span class="sxs-lookup"><span data-stu-id="d42b8-134">The name of the policy.</span></span>|
|<span data-ttu-id="d42b8-135">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-135">compliantDeviceCount</span></span>|<span data-ttu-id="d42b8-136">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-136">Int32</span></span>|<span data-ttu-id="d42b8-137">Número de dispositivos compatibles.</span><span class="sxs-lookup"><span data-stu-id="d42b8-137">Number of compliant devices.</span></span>|
|<span data-ttu-id="d42b8-138">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-138">nonCompliantDeviceCount</span></span>|<span data-ttu-id="d42b8-139">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-139">Int32</span></span>|<span data-ttu-id="d42b8-140">Número de dispositivos no compatibles.</span><span class="sxs-lookup"><span data-stu-id="d42b8-140">Number of non compliant devices.</span></span>|
|<span data-ttu-id="d42b8-141">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-141">remediatedDeviceCount</span></span>|<span data-ttu-id="d42b8-142">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-142">Int32</span></span>|<span data-ttu-id="d42b8-143">Número de dispositivos corregidos.</span><span class="sxs-lookup"><span data-stu-id="d42b8-143">Number of remediated devices.</span></span>|
|<span data-ttu-id="d42b8-144">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-144">errorDeviceCount</span></span>|<span data-ttu-id="d42b8-145">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-145">Int32</span></span>|<span data-ttu-id="d42b8-146">Número de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="d42b8-146">Number of devices had error.</span></span>|
|<span data-ttu-id="d42b8-147">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-147">unknownDeviceCount</span></span>|<span data-ttu-id="d42b8-148">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-148">Int32</span></span>|<span data-ttu-id="d42b8-149">Número de dispositivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="d42b8-149">Number of unknown devices.</span></span>|
|<span data-ttu-id="d42b8-150">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-150">conflictDeviceCount</span></span>|<span data-ttu-id="d42b8-151">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-151">Int32</span></span>|<span data-ttu-id="d42b8-152">Número de dispositivos en conflicto.</span><span class="sxs-lookup"><span data-stu-id="d42b8-152">Number of conflict devices.</span></span>|
|<span data-ttu-id="d42b8-153">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-153">notApplicableDeviceCount</span></span>|<span data-ttu-id="d42b8-154">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-154">Int32</span></span>|<span data-ttu-id="d42b8-155">Número de dispositivos no aplicables.</span><span class="sxs-lookup"><span data-stu-id="d42b8-155">Number of not applicable devices.</span></span>|
|<span data-ttu-id="d42b8-156">compliantUserCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-156">compliantUserCount</span></span>|<span data-ttu-id="d42b8-157">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-157">Int32</span></span>|<span data-ttu-id="d42b8-158">Número de usuarios compatibles.</span><span class="sxs-lookup"><span data-stu-id="d42b8-158">Number of compliant users.</span></span>|
|<span data-ttu-id="d42b8-159">nonCompliantUserCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-159">nonCompliantUserCount</span></span>|<span data-ttu-id="d42b8-160">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-160">Int32</span></span>|<span data-ttu-id="d42b8-161">Número de usuarios no compatibles.</span><span class="sxs-lookup"><span data-stu-id="d42b8-161">Number of non compliant users.</span></span>|
|<span data-ttu-id="d42b8-162">remediatedUserCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-162">remediatedUserCount</span></span>|<span data-ttu-id="d42b8-163">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-163">Int32</span></span>|<span data-ttu-id="d42b8-164">Número de usuarios corregidos.</span><span class="sxs-lookup"><span data-stu-id="d42b8-164">Number of remediated users.</span></span>|
|<span data-ttu-id="d42b8-165">errorUserCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-165">errorUserCount</span></span>|<span data-ttu-id="d42b8-166">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-166">Int32</span></span>|<span data-ttu-id="d42b8-167">Número de usuarios con errores.</span><span class="sxs-lookup"><span data-stu-id="d42b8-167">Number of users had error.</span></span>|
|<span data-ttu-id="d42b8-168">unknownUserCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-168">unknownUserCount</span></span>|<span data-ttu-id="d42b8-169">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-169">Int32</span></span>|<span data-ttu-id="d42b8-170">Número de usuarios desconocidos.</span><span class="sxs-lookup"><span data-stu-id="d42b8-170">Number of unknown users.</span></span>|
|<span data-ttu-id="d42b8-171">conflictUserCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-171">conflictUserCount</span></span>|<span data-ttu-id="d42b8-172">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-172">Int32</span></span>|<span data-ttu-id="d42b8-173">Número de usuarios en conflicto.</span><span class="sxs-lookup"><span data-stu-id="d42b8-173">Number of conflict users.</span></span>|
|<span data-ttu-id="d42b8-174">notApplicableUserCount</span><span class="sxs-lookup"><span data-stu-id="d42b8-174">notApplicableUserCount</span></span>|<span data-ttu-id="d42b8-175">Int32</span><span class="sxs-lookup"><span data-stu-id="d42b8-175">Int32</span></span>|<span data-ttu-id="d42b8-176">Número de usuarios no aplicables.</span><span class="sxs-lookup"><span data-stu-id="d42b8-176">Number of not applicable users.</span></span>|



## <a name="response"></a><span data-ttu-id="d42b8-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d42b8-177">Response</span></span>
<span data-ttu-id="d42b8-178">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d42b8-178">If successful, this method returns a `200 OK` response code and an updated [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d42b8-179">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d42b8-179">Example</span></span>
### <a name="request"></a><span data-ttu-id="d42b8-180">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d42b8-180">Request</span></span>
<span data-ttu-id="d42b8-181">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d42b8-181">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/softwareUpdateStatusSummary
Content-type: application/json
Content-length: 452

{
  "displayName": "Display Name value",
  "compliantDeviceCount": 4,
  "nonCompliantDeviceCount": 7,
  "remediatedDeviceCount": 5,
  "errorDeviceCount": 0,
  "unknownDeviceCount": 2,
  "conflictDeviceCount": 3,
  "notApplicableDeviceCount": 8,
  "compliantUserCount": 2,
  "nonCompliantUserCount": 5,
  "remediatedUserCount": 3,
  "errorUserCount": 14,
  "unknownUserCount": 0,
  "conflictUserCount": 1,
  "notApplicableUserCount": 6
}
```

### <a name="response"></a><span data-ttu-id="d42b8-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d42b8-182">Response</span></span>
<span data-ttu-id="d42b8-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d42b8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 567

{
  "@odata.type": "#microsoft.graph.softwareUpdateStatusSummary",
  "id": "4f71421f-421f-4f71-1f42-714f1f42714f",
  "displayName": "Display Name value",
  "compliantDeviceCount": 4,
  "nonCompliantDeviceCount": 7,
  "remediatedDeviceCount": 5,
  "errorDeviceCount": 0,
  "unknownDeviceCount": 2,
  "conflictDeviceCount": 3,
  "notApplicableDeviceCount": 8,
  "compliantUserCount": 2,
  "nonCompliantUserCount": 5,
  "remediatedUserCount": 3,
  "errorUserCount": 14,
  "unknownUserCount": 0,
  "conflictUserCount": 1,
  "notApplicableUserCount": 6
}
```








