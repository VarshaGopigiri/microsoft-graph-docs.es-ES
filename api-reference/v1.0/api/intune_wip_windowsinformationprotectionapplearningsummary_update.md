# <a name="update-windowsinformationprotectionapplearningsummary"></a><span data-ttu-id="f3ce0-101">Actualizar windowsInformationProtectionAppLearningSummary</span><span class="sxs-lookup"><span data-stu-id="f3ce0-101">Update windowsInformationProtectionAppLearningSummary</span></span>

> <span data-ttu-id="f3ce0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f3ce0-103">Actualice las propiedades de un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="f3ce0-103">Update the properties of a [calendar](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f3ce0-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f3ce0-104">Prerequisites</span></span>
<span data-ttu-id="f3ce0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f3ce0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f3ce0-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f3ce0-107">Permission type</span></span>|<span data-ttu-id="f3ce0-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f3ce0-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f3ce0-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f3ce0-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f3ce0-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f3ce0-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f3ce0-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f3ce0-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f3ce0-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-112">Not supported.</span></span>|
|<span data-ttu-id="f3ce0-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f3ce0-113">Application</span></span>|<span data-ttu-id="f3ce0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f3ce0-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f3ce0-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsInformationProtectionAppLearningSummaries/{windowsInformationProtectionAppLearningSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="f3ce0-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f3ce0-116">Request headers</span></span>
|<span data-ttu-id="f3ce0-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3ce0-117">Header</span></span>|<span data-ttu-id="f3ce0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f3ce0-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f3ce0-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="f3ce0-119">Authorization</span></span>|<span data-ttu-id="f3ce0-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="f3ce0-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f3ce0-121">Accept</span></span>|<span data-ttu-id="f3ce0-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f3ce0-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f3ce0-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f3ce0-123">Request body</span></span>
<span data-ttu-id="f3ce0-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="f3ce0-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object.</span></span>

<span data-ttu-id="f3ce0-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="f3ce0-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="f3ce0-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3ce0-126">Property</span></span>|<span data-ttu-id="f3ce0-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3ce0-127">Type</span></span>|<span data-ttu-id="f3ce0-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3ce0-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f3ce0-129">id</span><span class="sxs-lookup"><span data-stu-id="f3ce0-129">id</span></span>|<span data-ttu-id="f3ce0-130">String</span><span class="sxs-lookup"><span data-stu-id="f3ce0-130">String</span></span>|<span data-ttu-id="f3ce0-131">Identificador único para WindowsInformationProtectionAppLearningSummary.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-131">Unique Identifier for the WindowsInformationProtectionAppLearningSummary.</span></span>|
|<span data-ttu-id="f3ce0-132">applicationName</span><span class="sxs-lookup"><span data-stu-id="f3ce0-132">applicationName</span></span>|<span data-ttu-id="f3ce0-133">String</span><span class="sxs-lookup"><span data-stu-id="f3ce0-133">String</span></span>|<span data-ttu-id="f3ce0-134">Nombre de la aplicación</span><span class="sxs-lookup"><span data-stu-id="f3ce0-134">Application Name</span></span>|
|<span data-ttu-id="f3ce0-135">applicationType</span><span class="sxs-lookup"><span data-stu-id="f3ce0-135">applicationType</span></span>|<span data-ttu-id="f3ce0-136">String</span><span class="sxs-lookup"><span data-stu-id="f3ce0-136">String</span></span>|<span data-ttu-id="f3ce0-137">Tipo de aplicación Los valores posibles son: `universal` y `desktop`.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-137">Application Type Possible values are: `universal`, `desktop`.</span></span>|
|<span data-ttu-id="f3ce0-138">deviceCount</span><span class="sxs-lookup"><span data-stu-id="f3ce0-138">deviceCount</span></span>|<span data-ttu-id="f3ce0-139">Int32</span><span class="sxs-lookup"><span data-stu-id="f3ce0-139">Int32</span></span>|<span data-ttu-id="f3ce0-140">Recuento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="f3ce0-140">Device Count</span></span>|



## <a name="response"></a><span data-ttu-id="f3ce0-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3ce0-141">Response</span></span>
<span data-ttu-id="f3ce0-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-142">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f3ce0-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3ce0-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="f3ce0-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3ce0-144">Request</span></span>
<span data-ttu-id="f3ce0-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-145">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="f3ce0-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3ce0-146">Response</span></span>
<span data-ttu-id="f3ce0-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f3ce0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



