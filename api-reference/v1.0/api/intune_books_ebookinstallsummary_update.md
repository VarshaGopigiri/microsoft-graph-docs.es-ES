# <a name="update-ebookinstallsummary"></a><span data-ttu-id="bf703-101">Actualizar eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="bf703-101">Update eBookInstallSummary</span></span>

> <span data-ttu-id="bf703-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bf703-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bf703-103">Actualice las propiedades de un objeto [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="bf703-103">Update the properties of a [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bf703-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bf703-104">Prerequisites</span></span>
<span data-ttu-id="bf703-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bf703-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bf703-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf703-107">Permission type</span></span>|<span data-ttu-id="bf703-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf703-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bf703-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf703-109">Delegated (work or school account)</span></span>|<span data-ttu-id="bf703-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf703-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="bf703-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf703-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bf703-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf703-112">Not supported.</span></span>|
|<span data-ttu-id="bf703-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf703-113">Application</span></span>|<span data-ttu-id="bf703-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf703-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bf703-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf703-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/installSummary
```

## <a name="request-headers"></a><span data-ttu-id="bf703-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf703-116">Request headers</span></span>
|<span data-ttu-id="bf703-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf703-117">Header</span></span>|<span data-ttu-id="bf703-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bf703-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bf703-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="bf703-119">Authorization</span></span>|<span data-ttu-id="bf703-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bf703-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bf703-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bf703-121">Accept</span></span>|<span data-ttu-id="bf703-122">application/json</span><span class="sxs-lookup"><span data-stu-id="bf703-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bf703-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf703-123">Request body</span></span>
<span data-ttu-id="bf703-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="bf703-124">In the request body, supply a JSON representation for the [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md) object.</span></span>

<span data-ttu-id="bf703-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="bf703-125">The following table shows the properties that are required when you create the [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md).</span></span>

|<span data-ttu-id="bf703-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf703-126">Property</span></span>|<span data-ttu-id="bf703-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf703-127">Type</span></span>|<span data-ttu-id="bf703-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf703-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bf703-129">id</span><span class="sxs-lookup"><span data-stu-id="bf703-129">id</span></span>|<span data-ttu-id="bf703-130">String</span><span class="sxs-lookup"><span data-stu-id="bf703-130">String</span></span>|<span data-ttu-id="bf703-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bf703-131">Key of the entity.</span></span>|
|<span data-ttu-id="bf703-132">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bf703-132">installedDeviceCount</span></span>|<span data-ttu-id="bf703-133">Int32</span><span class="sxs-lookup"><span data-stu-id="bf703-133">Int32</span></span>|<span data-ttu-id="bf703-134">Número de dispositivos que han instalado correctamente este libro.</span><span class="sxs-lookup"><span data-stu-id="bf703-134">Number of Devices that have successfully installed this book.</span></span>|
|<span data-ttu-id="bf703-135">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bf703-135">failedDeviceCount</span></span>|<span data-ttu-id="bf703-136">Int32</span><span class="sxs-lookup"><span data-stu-id="bf703-136">Int32</span></span>|<span data-ttu-id="bf703-137">Número de dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="bf703-137">Number of Devices that have failed to install this book.</span></span>|
|<span data-ttu-id="bf703-138">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bf703-138">notInstalledDeviceCount</span></span>|<span data-ttu-id="bf703-139">Int32</span><span class="sxs-lookup"><span data-stu-id="bf703-139">Int32</span></span>|<span data-ttu-id="bf703-140">Número de dispositivos que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="bf703-140">Number of Devices that does not have this book installed.</span></span>|
|<span data-ttu-id="bf703-141">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="bf703-141">installedUserCount</span></span>|<span data-ttu-id="bf703-142">Int32</span><span class="sxs-lookup"><span data-stu-id="bf703-142">Int32</span></span>|<span data-ttu-id="bf703-143">Número de usuarios cuyos dispositivos al completo han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="bf703-143">Number of Users whose devices have all succeeded to install this book.</span></span>|
|<span data-ttu-id="bf703-144">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="bf703-144">failedUserCount</span></span>|<span data-ttu-id="bf703-145">Int32</span><span class="sxs-lookup"><span data-stu-id="bf703-145">Int32</span></span>|<span data-ttu-id="bf703-146">Número de usuarios que tienen 1 o más dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="bf703-146">Number of Users that have 1 or more device that failed to install this book.</span></span>|
|<span data-ttu-id="bf703-147">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="bf703-147">notInstalledUserCount</span></span>|<span data-ttu-id="bf703-148">Int32</span><span class="sxs-lookup"><span data-stu-id="bf703-148">Int32</span></span>|<span data-ttu-id="bf703-149">Número de usuarios que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="bf703-149">Number of Users that did not install this book.</span></span>|



## <a name="response"></a><span data-ttu-id="bf703-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf703-150">Response</span></span>
<span data-ttu-id="bf703-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf703-151">If successful, this method returns a `200 OK` response code and an updated [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bf703-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf703-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="bf703-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf703-153">Request</span></span>
<span data-ttu-id="bf703-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf703-154">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/installSummary
Content-type: application/json
Content-length: 236

{
  "@odata.type": "#microsoft.graph.eBookInstallSummary",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7,
  "installedUserCount": 2,
  "failedUserCount": 15,
  "notInstalledUserCount": 5
}
```

### <a name="response"></a><span data-ttu-id="bf703-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf703-155">Response</span></span>
<span data-ttu-id="bf703-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf703-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 285

{
  "@odata.type": "#microsoft.graph.eBookInstallSummary",
  "id": "9708ad78-ad78-9708-78ad-089778ad0897",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7,
  "installedUserCount": 2,
  "failedUserCount": 15,
  "notInstalledUserCount": 5
}
```



