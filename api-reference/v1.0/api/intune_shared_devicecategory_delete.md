# <a name="delete-devicecategory"></a><span data-ttu-id="01971-101">Eliminar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="01971-101">Delete deviceCategory</span></span>

> <span data-ttu-id="01971-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01971-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01971-103">Elimina un [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="01971-103">Deletes a [deviceCategory](../resources/intune_shared_devicecategory.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="01971-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="01971-104">Prerequisites</span></span>
<span data-ttu-id="01971-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="01971-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="01971-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01971-107">Permission type</span></span>|<span data-ttu-id="01971-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01971-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="01971-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01971-109">Delegated (work or school account)</span></span>||
| <span data-ttu-id="01971-110">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="01971-110">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="01971-111">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01971-111">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="01971-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01971-112">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="01971-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01971-113">Not supported.</span></span>|
|<span data-ttu-id="01971-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01971-114">Application</span></span>|<span data-ttu-id="01971-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01971-115">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="01971-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01971-116">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceCategories/{deviceCategoryId}
```

## <a name="request-headers"></a><span data-ttu-id="01971-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01971-117">Request headers</span></span>
|<span data-ttu-id="01971-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01971-118">Header</span></span>|<span data-ttu-id="01971-119">Valor</span><span class="sxs-lookup"><span data-stu-id="01971-119">Value</span></span>|
|:---|:---|
|<span data-ttu-id="01971-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="01971-120">Authorization</span></span>|<span data-ttu-id="01971-121">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="01971-121">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="01971-122">Aceptar</span><span class="sxs-lookup"><span data-stu-id="01971-122">Accept</span></span>|<span data-ttu-id="01971-123">application/json</span><span class="sxs-lookup"><span data-stu-id="01971-123">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="01971-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01971-124">Request body</span></span>
<span data-ttu-id="01971-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="01971-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="01971-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01971-126">Response</span></span>
<span data-ttu-id="01971-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="01971-127">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="01971-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01971-128">Example</span></span>
### <a name="request"></a><span data-ttu-id="01971-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01971-129">Request</span></span>
<span data-ttu-id="01971-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01971-130">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories/{deviceCategoryId}
```

### <a name="response"></a><span data-ttu-id="01971-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01971-131">Response</span></span>
<span data-ttu-id="01971-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01971-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



