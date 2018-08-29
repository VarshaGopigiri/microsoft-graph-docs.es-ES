# <a name="create-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="60ba8-101">Crear windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="60ba8-101">Create windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="60ba8-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="60ba8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="60ba8-103">Cree un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="60ba8-103">Create a new [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="60ba8-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="60ba8-104">Prerequisites</span></span>
<span data-ttu-id="60ba8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="60ba8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="60ba8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="60ba8-107">Permission type</span></span>|<span data-ttu-id="60ba8-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="60ba8-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="60ba8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="60ba8-109">Delegated (work or school account)</span></span>|<span data-ttu-id="60ba8-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="60ba8-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="60ba8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="60ba8-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="60ba8-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="60ba8-112">Not supported.</span></span>|
|<span data-ttu-id="60ba8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="60ba8-113">Application</span></span>|<span data-ttu-id="60ba8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="60ba8-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="60ba8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="60ba8-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsInformationProtectionAppLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="60ba8-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="60ba8-116">Request headers</span></span>
|<span data-ttu-id="60ba8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60ba8-117">Header</span></span>|<span data-ttu-id="60ba8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="60ba8-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="60ba8-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="60ba8-119">Authorization</span></span>|<span data-ttu-id="60ba8-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="60ba8-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="60ba8-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="60ba8-121">Accept</span></span>|<span data-ttu-id="60ba8-122">application/json</span><span class="sxs-lookup"><span data-stu-id="60ba8-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="60ba8-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="60ba8-123">Request body</span></span>
<span data-ttu-id="60ba8-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="60ba8-124">In the request body, supply a JSON representation for the windowsInformationProtectionAppLearningSummary object.</span></span>

<span data-ttu-id="60ba8-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="60ba8-125">The following table shows the properties that are required when you create the windowsInformationProtectionAppLearningSummary.</span></span>

|<span data-ttu-id="60ba8-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60ba8-126">Property</span></span>|<span data-ttu-id="60ba8-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="60ba8-127">Type</span></span>|<span data-ttu-id="60ba8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="60ba8-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="60ba8-129">id</span><span class="sxs-lookup"><span data-stu-id="60ba8-129">id</span></span>|<span data-ttu-id="60ba8-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="60ba8-130">String</span></span>|<span data-ttu-id="60ba8-131">Identificador único para WindowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="60ba8-131">Unique Identifier for the WindowsInformationProtectionAppLearningSummary.</span></span>|
|<span data-ttu-id="60ba8-132">applicationName</span><span class="sxs-lookup"><span data-stu-id="60ba8-132">applicationName</span></span>|<span data-ttu-id="60ba8-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="60ba8-133">String</span></span>|<span data-ttu-id="60ba8-134">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="60ba8-134">Application Name</span></span>|
|<span data-ttu-id="60ba8-135">applicationType</span><span class="sxs-lookup"><span data-stu-id="60ba8-135">applicationType</span></span>|[<span data-ttu-id="60ba8-136">applicationType</span><span class="sxs-lookup"><span data-stu-id="60ba8-136">applicationType</span></span>](../resources/intune_wip_applicationtype.md)|<span data-ttu-id="60ba8-137">Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="60ba8-137">Target Application Type</span></span> <span data-ttu-id="60ba8-138">Los valores posibles son: `universal`, `desktop`.</span><span class="sxs-lookup"><span data-stu-id="60ba8-138">The possible values are:</span></span>|
|<span data-ttu-id="60ba8-139">deviceCount</span><span class="sxs-lookup"><span data-stu-id="60ba8-139">deviceCount</span></span>|<span data-ttu-id="60ba8-140">Int32</span><span class="sxs-lookup"><span data-stu-id="60ba8-140">Int32</span></span>|<span data-ttu-id="60ba8-141">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="60ba8-141">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="60ba8-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60ba8-142">Response</span></span>
<span data-ttu-id="60ba8-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60ba8-143">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="60ba8-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60ba8-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="60ba8-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="60ba8-145">Request</span></span>
<span data-ttu-id="60ba8-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60ba8-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionAppLearningSummaries
Content-type: application/json
Content-length: 191

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
  "applicationName": "Application Name value",
  "applicationType": "desktop",
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="60ba8-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60ba8-147">Response</span></span>
<span data-ttu-id="60ba8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="60ba8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



