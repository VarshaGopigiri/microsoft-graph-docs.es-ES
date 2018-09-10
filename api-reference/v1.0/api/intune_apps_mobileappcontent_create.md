# <a name="create-mobileappcontent"></a><span data-ttu-id="2e140-101">Crear mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="2e140-101">Create mobileAppContent</span></span>

> <span data-ttu-id="2e140-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2e140-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2e140-103">Cree un objeto [mobileAppContent](../resources/intune_apps_mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="2e140-103">Create a new [mobileAppContent](../resources/intune_apps_mobileappcontent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2e140-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2e140-104">Prerequisites</span></span>
<span data-ttu-id="2e140-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2e140-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2e140-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2e140-107">Permission type</span></span>|<span data-ttu-id="2e140-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2e140-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2e140-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2e140-109">Delegated (work or school account)</span></span>|<span data-ttu-id="2e140-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2e140-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="2e140-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2e140-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2e140-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e140-112">Not supported.</span></span>|
|<span data-ttu-id="2e140-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2e140-113">Application</span></span>|<span data-ttu-id="2e140-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e140-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2e140-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2e140-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.mobileLobApp/contentVersions
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.managedMobileLobApp/contentVersions
```

## <a name="request-headers"></a><span data-ttu-id="2e140-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2e140-116">Request headers</span></span>
|<span data-ttu-id="2e140-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e140-117">Header</span></span>|<span data-ttu-id="2e140-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2e140-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2e140-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="2e140-119">Authorization</span></span>|<span data-ttu-id="2e140-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2e140-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2e140-121">Accept</span><span class="sxs-lookup"><span data-stu-id="2e140-121">Accept</span></span>|<span data-ttu-id="2e140-122">application/json</span><span class="sxs-lookup"><span data-stu-id="2e140-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2e140-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2e140-123">Request body</span></span>
<span data-ttu-id="2e140-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppContent.</span><span class="sxs-lookup"><span data-stu-id="2e140-124">In the request body, supply a JSON representation for the mobileAppContent object.</span></span>

<span data-ttu-id="2e140-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppContent.</span><span class="sxs-lookup"><span data-stu-id="2e140-125">The following table shows the properties that are required when you create the mobileAppContent.</span></span>

|<span data-ttu-id="2e140-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2e140-126">Property</span></span>|<span data-ttu-id="2e140-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="2e140-127">Type</span></span>|<span data-ttu-id="2e140-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e140-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2e140-129">id</span><span class="sxs-lookup"><span data-stu-id="2e140-129">id</span></span>|<span data-ttu-id="2e140-130">String</span><span class="sxs-lookup"><span data-stu-id="2e140-130">String</span></span>|<span data-ttu-id="2e140-131">La versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2e140-131">The app content version.</span></span>|



## <a name="response"></a><span data-ttu-id="2e140-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e140-132">Response</span></span>
<span data-ttu-id="2e140-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppContent](../resources/intune_apps_mobileappcontent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e140-133">If successful, this method returns a `201 Created` response code and a [mobileAppContent](../resources/intune_apps_mobileappcontent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2e140-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e140-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="2e140-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2e140-135">Request</span></span>
<span data-ttu-id="2e140-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e140-136">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions
Content-type: application/json
Content-length: 58

{
  "@odata.type": "#microsoft.graph.mobileAppContent"
}
```

### <a name="response"></a><span data-ttu-id="2e140-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e140-137">Response</span></span>
<span data-ttu-id="2e140-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2e140-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 107

{
  "@odata.type": "#microsoft.graph.mobileAppContent",
  "id": "fe0bb9a9-b9a9-fe0b-a9b9-0bfea9b90bfe"
}
```








