# <a name="list-users"></a><span data-ttu-id="1fa07-101">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="1fa07-101">List users</span></span>

> <span data-ttu-id="1fa07-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1fa07-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1fa07-103">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1fa07-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1fa07-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1fa07-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1fa07-105">Enumere las propiedades y las relaciones de los objetos [user](../resources/intune_troubleshooting_user.md).</span><span class="sxs-lookup"><span data-stu-id="1fa07-105">List properties and relationships of the [user](../resources/intune_troubleshooting_user.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1fa07-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1fa07-106">Prerequisites</span></span>
<span data-ttu-id="1fa07-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1fa07-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1fa07-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1fa07-109">Permission type</span></span>|<span data-ttu-id="1fa07-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1fa07-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1fa07-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1fa07-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1fa07-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="1fa07-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="1fa07-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1fa07-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1fa07-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1fa07-114">Not supported.</span></span>|
|<span data-ttu-id="1fa07-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1fa07-115">Application</span></span>|<span data-ttu-id="1fa07-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1fa07-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1fa07-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1fa07-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users
```

## <a name="request-headers"></a><span data-ttu-id="1fa07-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1fa07-118">Request headers</span></span>
|<span data-ttu-id="1fa07-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fa07-119">Header</span></span>|<span data-ttu-id="1fa07-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1fa07-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1fa07-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="1fa07-121">Authorization</span></span>|<span data-ttu-id="1fa07-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1fa07-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1fa07-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1fa07-123">Accept</span></span>|<span data-ttu-id="1fa07-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1fa07-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1fa07-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1fa07-125">Request body</span></span>
<span data-ttu-id="1fa07-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1fa07-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1fa07-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fa07-127">Response</span></span>
<span data-ttu-id="1fa07-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/intune_troubleshooting_user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1fa07-128">If successful, this method returns a `200 OK` response code and a collection of [user](../resources/intune_troubleshooting_user.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1fa07-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fa07-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="1fa07-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1fa07-130">Request</span></span>
<span data-ttu-id="1fa07-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1fa07-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/users
```

### <a name="response"></a><span data-ttu-id="1fa07-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fa07-132">Response</span></span>
<span data-ttu-id="1fa07-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1fa07-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 136

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.user",
      "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
    }
  ]
}
```



