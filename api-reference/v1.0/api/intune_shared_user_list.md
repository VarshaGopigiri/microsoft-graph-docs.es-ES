# <a name="list-users"></a><span data-ttu-id="d2a0c-101">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="d2a0c-101">List users</span></span>

> <span data-ttu-id="d2a0c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d2a0c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d2a0c-103">Enumere las propiedades y las relaciones de los objetos [user](../resources/intune_shared_user.md).</span><span class="sxs-lookup"><span data-stu-id="d2a0c-103">List properties and relationships of the [user](../resources/intune_shared_user.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d2a0c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d2a0c-104">Prerequisites</span></span>
<span data-ttu-id="d2a0c-105">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d2a0c-105">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="d2a0c-106">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d2a0c-106">To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>  <span data-ttu-id="d2a0c-107">El permiso específico depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="d2a0c-107">The specific permission depends on the context.</span></span>

|<span data-ttu-id="d2a0c-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2a0c-108">Permission type</span></span>|<span data-ttu-id="d2a0c-109">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2a0c-109">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d2a0c-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2a0c-110">Delegated (work or school account)</span></span>| <span data-ttu-id="d2a0c-111">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="d2a0c-111">_varies by context_</span></span>|
| <span data-ttu-id="d2a0c-112">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="d2a0c-112">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="d2a0c-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="d2a0c-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="d2a0c-114">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="d2a0c-114">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="d2a0c-115">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="d2a0c-115">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="d2a0c-116">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="d2a0c-116">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="d2a0c-117">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="d2a0c-117">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="d2a0c-118">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="d2a0c-118">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="d2a0c-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="d2a0c-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
|<span data-ttu-id="d2a0c-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2a0c-120">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d2a0c-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2a0c-121">Not supported.</span></span>|
|<span data-ttu-id="d2a0c-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2a0c-122">Application</span></span>|<span data-ttu-id="d2a0c-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2a0c-123">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d2a0c-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2a0c-124">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users
```

## <a name="request-headers"></a><span data-ttu-id="d2a0c-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2a0c-125">Request headers</span></span>
|<span data-ttu-id="d2a0c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2a0c-126">Header</span></span>|<span data-ttu-id="d2a0c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d2a0c-127">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d2a0c-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2a0c-128">Authorization</span></span>|<span data-ttu-id="d2a0c-129">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d2a0c-129">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d2a0c-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d2a0c-130">Accept</span></span>|<span data-ttu-id="d2a0c-131">application/json</span><span class="sxs-lookup"><span data-stu-id="d2a0c-131">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d2a0c-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2a0c-132">Request body</span></span>
<span data-ttu-id="d2a0c-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d2a0c-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d2a0c-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2a0c-134">Response</span></span>
<span data-ttu-id="d2a0c-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/intune_shared_user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2a0c-135">If successful, this method returns a `200 OK` response code and a collection of [user](../resources/intune_shared_user.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2a0c-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2a0c-136">Example</span></span>

### <a name="request"></a><span data-ttu-id="d2a0c-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2a0c-137">Request</span></span>
<span data-ttu-id="d2a0c-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2a0c-138">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users
```

### <a name="response"></a><span data-ttu-id="d2a0c-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2a0c-139">Response</span></span>
<span data-ttu-id="d2a0c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2a0c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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



