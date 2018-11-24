# <a name="create-userinstallstatesummary"></a><span data-ttu-id="03851-101">Crear userInstallStateSummary</span><span class="sxs-lookup"><span data-stu-id="03851-101">Create userInstallStateSummary</span></span>

> <span data-ttu-id="03851-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="03851-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="03851-103">Cree un objeto [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="03851-103">Create a new [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="03851-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03851-104">Prerequisites</span></span>
<span data-ttu-id="03851-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="03851-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="03851-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03851-107">Permission type</span></span>|<span data-ttu-id="03851-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03851-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="03851-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03851-109">Delegated (work or school account)</span></span>|<span data-ttu-id="03851-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="03851-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="03851-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03851-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="03851-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03851-112">Not supported.</span></span>|
|<span data-ttu-id="03851-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03851-113">Application</span></span>|<span data-ttu-id="03851-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03851-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="03851-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03851-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="03851-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03851-116">Request headers</span></span>
|<span data-ttu-id="03851-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03851-117">Header</span></span>|<span data-ttu-id="03851-118">Valor</span><span class="sxs-lookup"><span data-stu-id="03851-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="03851-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="03851-119">Authorization</span></span>|<span data-ttu-id="03851-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="03851-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="03851-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="03851-121">Accept</span></span>|<span data-ttu-id="03851-122">application/json</span><span class="sxs-lookup"><span data-stu-id="03851-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="03851-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03851-123">Request body</span></span>
<span data-ttu-id="03851-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto userInstallStateSummary.</span><span class="sxs-lookup"><span data-stu-id="03851-124">In the request body, supply a JSON representation for the userInstallStateSummary object.</span></span>

<span data-ttu-id="03851-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto userInstallStateSummary.</span><span class="sxs-lookup"><span data-stu-id="03851-125">The following table shows the properties that are required when you create the userInstallStateSummary.</span></span>

|<span data-ttu-id="03851-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="03851-126">Property</span></span>|<span data-ttu-id="03851-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="03851-127">Type</span></span>|<span data-ttu-id="03851-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="03851-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="03851-129">id</span><span class="sxs-lookup"><span data-stu-id="03851-129">id</span></span>|<span data-ttu-id="03851-130">String</span><span class="sxs-lookup"><span data-stu-id="03851-130">String</span></span>|<span data-ttu-id="03851-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="03851-131">Key of the entity.</span></span>|
|<span data-ttu-id="03851-132">userName</span><span class="sxs-lookup"><span data-stu-id="03851-132">userName</span></span>|<span data-ttu-id="03851-133">String</span><span class="sxs-lookup"><span data-stu-id="03851-133">String</span></span>|<span data-ttu-id="03851-134">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="03851-134">User name.</span></span>|
|<span data-ttu-id="03851-135">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="03851-135">installedDeviceCount</span></span>|<span data-ttu-id="03851-136">Int32</span><span class="sxs-lookup"><span data-stu-id="03851-136">Int32</span></span>|<span data-ttu-id="03851-137">Número de dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="03851-137">Installed Device Count.</span></span>|
|<span data-ttu-id="03851-138">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="03851-138">failedDeviceCount</span></span>|<span data-ttu-id="03851-139">Int32</span><span class="sxs-lookup"><span data-stu-id="03851-139">Int32</span></span>|<span data-ttu-id="03851-140">Número de dispositivos erróneos.</span><span class="sxs-lookup"><span data-stu-id="03851-140">Failed Device Count.</span></span>|
|<span data-ttu-id="03851-141">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="03851-141">notInstalledDeviceCount</span></span>|<span data-ttu-id="03851-142">Int32</span><span class="sxs-lookup"><span data-stu-id="03851-142">Int32</span></span>|<span data-ttu-id="03851-143">Número de dispositivos no instalados.</span><span class="sxs-lookup"><span data-stu-id="03851-143">Not installed device count.</span></span>|



## <a name="response"></a><span data-ttu-id="03851-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03851-144">Response</span></span>
<span data-ttu-id="03851-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03851-145">If successful, this method returns a `201 Created` response code and a [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03851-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03851-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="03851-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03851-147">Request</span></span>
<span data-ttu-id="03851-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03851-148">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary
Content-type: application/json
Content-length: 189

{
  "@odata.type": "#microsoft.graph.userInstallStateSummary",
  "userName": "User Name value",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7
}
```

### <a name="response"></a><span data-ttu-id="03851-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03851-149">Response</span></span>
<span data-ttu-id="03851-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03851-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 238

{
  "@odata.type": "#microsoft.graph.userInstallStateSummary",
  "id": "1e5b41ba-41ba-1e5b-ba41-5b1eba415b1e",
  "userName": "User Name value",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7
}
```



