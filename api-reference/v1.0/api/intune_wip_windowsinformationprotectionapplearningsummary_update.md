# <a name="update-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="8af76-101">Actualizar windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="8af76-101">Update windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="8af76-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8af76-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8af76-103">Actualice las propiedades de un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="8af76-103">Update the properties of a [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8af76-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8af76-104">Prerequisites</span></span>
<span data-ttu-id="8af76-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8af76-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8af76-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8af76-107">Permission type</span></span>|<span data-ttu-id="8af76-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8af76-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8af76-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8af76-109">Delegated (work or school account)</span></span>|<span data-ttu-id="8af76-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8af76-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8af76-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8af76-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8af76-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8af76-112">Not supported.</span></span>|
|<span data-ttu-id="8af76-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8af76-113">Application</span></span>|<span data-ttu-id="8af76-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8af76-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8af76-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8af76-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="8af76-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8af76-116">Request headers</span></span>
|<span data-ttu-id="8af76-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8af76-117">Header</span></span>|<span data-ttu-id="8af76-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8af76-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8af76-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="8af76-119">Authorization</span></span>|<span data-ttu-id="8af76-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8af76-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8af76-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8af76-121">Accept</span></span>|<span data-ttu-id="8af76-122">aplicación/json</span><span class="sxs-lookup"><span data-stu-id="8af76-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8af76-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8af76-123">Request body</span></span>
<span data-ttu-id="8af76-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="8af76-124">In the request body, supply a JSON representation for the [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object.</span></span>

<span data-ttu-id="8af76-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="8af76-125">The following table shows the properties that are required when you create the [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).</span></span>

|<span data-ttu-id="8af76-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8af76-126">Property</span></span>|<span data-ttu-id="8af76-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="8af76-127">Type</span></span>|<span data-ttu-id="8af76-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="8af76-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8af76-129">id</span><span class="sxs-lookup"><span data-stu-id="8af76-129">id</span></span>|<span data-ttu-id="8af76-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="8af76-130">String</span></span>|<span data-ttu-id="8af76-131">Identificador único para WindowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="8af76-131">Unique Identifier for the WindowsInformationProtectionAppLearningSummary.</span></span>|
|<span data-ttu-id="8af76-132">applicationName</span><span class="sxs-lookup"><span data-stu-id="8af76-132">applicationName</span></span>|<span data-ttu-id="8af76-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="8af76-133">String</span></span>|<span data-ttu-id="8af76-134">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8af76-134">Application Name</span></span>|
|<span data-ttu-id="8af76-135">applicationType</span><span class="sxs-lookup"><span data-stu-id="8af76-135">applicationType</span></span>|[<span data-ttu-id="8af76-136">applicationType</span><span class="sxs-lookup"><span data-stu-id="8af76-136">applicationType</span></span>](../resources/intune_wip_applicationtype.md)|<span data-ttu-id="8af76-p102">Tipo de aplicación. Los valores posibles son: `universal` y `desktop`.</span><span class="sxs-lookup"><span data-stu-id="8af76-p102">Application Type Possible values are: `universal`, `desktop`.</span></span>|
|<span data-ttu-id="8af76-139">deviceCount</span><span class="sxs-lookup"><span data-stu-id="8af76-139">deviceCount</span></span>|<span data-ttu-id="8af76-140">Int32</span><span class="sxs-lookup"><span data-stu-id="8af76-140">Int32</span></span>|<span data-ttu-id="8af76-141">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="8af76-141">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="8af76-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8af76-142">Response</span></span>
<span data-ttu-id="8af76-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8af76-143">If successful, this method returns a `200 OK` response code and an updated [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8af76-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8af76-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="8af76-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8af76-145">Request</span></span>
<span data-ttu-id="8af76-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8af76-146">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
Content-type: application/json
Content-length: 106

{
  "applicationName": "Application Name value",
  "applicationType": "desktop",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="8af76-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8af76-147">Response</span></span>
<span data-ttu-id="8af76-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8af76-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 240

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
  "id": "063baf50-af50-063b-50af-3b0650af3b06",
  "applicationName": "Application Name value",
  "applicationType": "desktop",
  "deviceCount": 11
}
```








