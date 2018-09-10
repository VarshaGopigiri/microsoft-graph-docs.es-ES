# <a name="delete-androidmanagedappprotection"></a><span data-ttu-id="74a0c-101">Eliminar androidManagedAppProtection</span><span class="sxs-lookup"><span data-stu-id="74a0c-101">Delete androidManagedAppProtection</span></span>

> <span data-ttu-id="74a0c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="74a0c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="74a0c-103">Elimina un [androidManagedAppProtection](../resources/intune_mam_androidmanagedappprotection.md).</span><span class="sxs-lookup"><span data-stu-id="74a0c-103">Deletes a [androidManagedAppProtection](../resources/intune_mam_androidmanagedappprotection.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="74a0c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="74a0c-104">Prerequisites</span></span>
<span data-ttu-id="74a0c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="74a0c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="74a0c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74a0c-107">Permission type</span></span>|<span data-ttu-id="74a0c-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74a0c-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="74a0c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74a0c-109">Delegated (work or school account)</span></span>|<span data-ttu-id="74a0c-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="74a0c-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="74a0c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74a0c-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="74a0c-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74a0c-112">Not supported.</span></span>|
|<span data-ttu-id="74a0c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74a0c-113">Application</span></span>|<span data-ttu-id="74a0c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74a0c-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="74a0c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74a0c-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}
```

## <a name="request-headers"></a><span data-ttu-id="74a0c-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74a0c-116">Request headers</span></span>
|<span data-ttu-id="74a0c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74a0c-117">Header</span></span>|<span data-ttu-id="74a0c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="74a0c-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="74a0c-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="74a0c-119">Authorization</span></span>|<span data-ttu-id="74a0c-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="74a0c-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="74a0c-121">Accept</span><span class="sxs-lookup"><span data-stu-id="74a0c-121">Accept</span></span>|<span data-ttu-id="74a0c-122">application/json</span><span class="sxs-lookup"><span data-stu-id="74a0c-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="74a0c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74a0c-123">Request body</span></span>
<span data-ttu-id="74a0c-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="74a0c-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="74a0c-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74a0c-125">Response</span></span>
<span data-ttu-id="74a0c-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="74a0c-126">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="74a0c-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74a0c-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="74a0c-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74a0c-128">Request</span></span>
<span data-ttu-id="74a0c-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74a0c-129">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}
```

### <a name="response"></a><span data-ttu-id="74a0c-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74a0c-130">Response</span></span>
<span data-ttu-id="74a0c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74a0c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```








