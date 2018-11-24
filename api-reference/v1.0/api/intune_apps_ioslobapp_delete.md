# <a name="delete-ioslobapp"></a><span data-ttu-id="f0681-101">Eliminar iosLobApp</span><span class="sxs-lookup"><span data-stu-id="f0681-101">Delete iosLobApp</span></span>

> <span data-ttu-id="f0681-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f0681-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f0681-103">Elimina un [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f0681-103">Deletes a [iosLobApp](../resources/intune_apps_ioslobapp.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f0681-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f0681-104">Prerequisites</span></span>
<span data-ttu-id="f0681-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f0681-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f0681-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f0681-107">Permission type</span></span>|<span data-ttu-id="f0681-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f0681-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f0681-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f0681-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f0681-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f0681-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f0681-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f0681-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f0681-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0681-112">Not supported.</span></span>|
|<span data-ttu-id="f0681-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f0681-113">Application</span></span>|<span data-ttu-id="f0681-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0681-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f0681-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f0681-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="f0681-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f0681-116">Request headers</span></span>
|<span data-ttu-id="f0681-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0681-117">Header</span></span>|<span data-ttu-id="f0681-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f0681-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f0681-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="f0681-119">Authorization</span></span>|<span data-ttu-id="f0681-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f0681-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f0681-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f0681-121">Accept</span></span>|<span data-ttu-id="f0681-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f0681-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f0681-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f0681-123">Request body</span></span>
<span data-ttu-id="f0681-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f0681-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f0681-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0681-125">Response</span></span>
<span data-ttu-id="f0681-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f0681-126">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f0681-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f0681-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="f0681-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f0681-128">Request</span></span>
<span data-ttu-id="f0681-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f0681-129">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="f0681-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0681-130">Response</span></span>
<span data-ttu-id="f0681-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f0681-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



