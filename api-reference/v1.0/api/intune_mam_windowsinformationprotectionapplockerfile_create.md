# <a name="create-windowsinformationprotectionapplockerfile"></a><span data-ttu-id="894ac-101">Crear windowsInformationProtectionAppLockerFile</span><span class="sxs-lookup"><span data-stu-id="894ac-101">Create windowsInformationProtectionAppLockerFile</span></span>

> <span data-ttu-id="894ac-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="894ac-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="894ac-103">Cree un objeto [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="894ac-103">Create a new [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="894ac-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="894ac-104">Prerequisites</span></span>
<span data-ttu-id="894ac-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="894ac-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="894ac-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="894ac-107">Permission type</span></span>|<span data-ttu-id="894ac-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="894ac-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="894ac-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="894ac-109">Delegated (work or school account)</span></span>|<span data-ttu-id="894ac-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="894ac-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="894ac-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="894ac-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="894ac-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="894ac-112">Not supported.</span></span>|
|<span data-ttu-id="894ac-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="894ac-113">Application</span></span>|<span data-ttu-id="894ac-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="894ac-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="894ac-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="894ac-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles
POST /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/protectedAppLockerFiles
POST /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/exemptAppLockerFiles
POST /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/protectedAppLockerFiles
```

## <a name="request-headers"></a><span data-ttu-id="894ac-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="894ac-116">Request headers</span></span>
|<span data-ttu-id="894ac-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="894ac-117">Header</span></span>|<span data-ttu-id="894ac-118">Valor</span><span class="sxs-lookup"><span data-stu-id="894ac-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="894ac-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="894ac-119">Authorization</span></span>|<span data-ttu-id="894ac-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="894ac-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="894ac-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="894ac-121">Accept</span></span>|<span data-ttu-id="894ac-122">application/json</span><span class="sxs-lookup"><span data-stu-id="894ac-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="894ac-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="894ac-123">Request body</span></span>
<span data-ttu-id="894ac-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsInformationProtectionAppLockerFile.</span><span class="sxs-lookup"><span data-stu-id="894ac-124">In the request body, supply a JSON representation for the windowsInformationProtectionAppLockerFile object.</span></span>

<span data-ttu-id="894ac-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsInformationProtectionAppLockerFile.</span><span class="sxs-lookup"><span data-stu-id="894ac-125">The following table shows the properties that are required when you create the windowsInformationProtectionAppLockerFile.</span></span>

|<span data-ttu-id="894ac-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="894ac-126">Property</span></span>|<span data-ttu-id="894ac-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="894ac-127">Type</span></span>|<span data-ttu-id="894ac-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="894ac-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="894ac-129">displayName</span><span class="sxs-lookup"><span data-stu-id="894ac-129">displayName</span></span>|<span data-ttu-id="894ac-130">String</span><span class="sxs-lookup"><span data-stu-id="894ac-130">String</span></span>|<span data-ttu-id="894ac-131">El nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="894ac-131">The friendly name</span></span>|
|<span data-ttu-id="894ac-132">fileHash</span><span class="sxs-lookup"><span data-stu-id="894ac-132">fileHash</span></span>|<span data-ttu-id="894ac-133">String</span><span class="sxs-lookup"><span data-stu-id="894ac-133">String</span></span>|<span data-ttu-id="894ac-134">Hash del archivo SHA256</span><span class="sxs-lookup"><span data-stu-id="894ac-134">SHA256 hash of the file</span></span>|
|<span data-ttu-id="894ac-135">file</span><span class="sxs-lookup"><span data-stu-id="894ac-135">file</span></span>|<span data-ttu-id="894ac-136">Binario</span><span class="sxs-lookup"><span data-stu-id="894ac-136">Binary</span></span>|<span data-ttu-id="894ac-137">Archivo como una matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="894ac-137">File as a byte array</span></span>|
|<span data-ttu-id="894ac-138">id</span><span class="sxs-lookup"><span data-stu-id="894ac-138">id</span></span>|<span data-ttu-id="894ac-139">String</span><span class="sxs-lookup"><span data-stu-id="894ac-139">String</span></span>|<span data-ttu-id="894ac-140">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="894ac-140">Key of the entity.</span></span>|
|<span data-ttu-id="894ac-141">version</span><span class="sxs-lookup"><span data-stu-id="894ac-141">version</span></span>|<span data-ttu-id="894ac-142">String</span><span class="sxs-lookup"><span data-stu-id="894ac-142">String</span></span>|<span data-ttu-id="894ac-143">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="894ac-143">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="894ac-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="894ac-144">Response</span></span>
<span data-ttu-id="894ac-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="894ac-145">If successful, this method returns a `201 Created` response code and a [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="894ac-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="894ac-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="894ac-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="894ac-147">Request</span></span>
<span data-ttu-id="894ac-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="894ac-148">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles
Content-type: application/json
Content-length: 211

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLockerFile",
  "displayName": "Display Name value",
  "fileHash": "File Hash value",
  "file": "ZmlsZQ==",
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="894ac-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="894ac-149">Response</span></span>
<span data-ttu-id="894ac-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="894ac-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 260

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLockerFile",
  "displayName": "Display Name value",
  "fileHash": "File Hash value",
  "file": "ZmlsZQ==",
  "id": "d81f0e40-0e40-d81f-400e-1fd8400e1fd8",
  "version": "Version value"
}
```



