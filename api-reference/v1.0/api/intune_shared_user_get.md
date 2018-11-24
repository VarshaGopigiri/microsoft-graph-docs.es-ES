# <a name="get-user"></a><span data-ttu-id="35bd0-101">Obtener usuario</span><span class="sxs-lookup"><span data-stu-id="35bd0-101">Get user</span></span>

> <span data-ttu-id="35bd0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="35bd0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="35bd0-103">Lea las propiedades y las relaciones del objeto [user](../resources/intune_shared_user.md).</span><span class="sxs-lookup"><span data-stu-id="35bd0-103">Read properties and relationships of the [user](../resources/intune_shared_user.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="35bd0-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="35bd0-104">Prerequisites</span></span>
<span data-ttu-id="35bd0-105">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="35bd0-105">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="35bd0-106">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="35bd0-106">To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>  <span data-ttu-id="35bd0-107">El permiso específico depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="35bd0-107">The specific permission depends on the context.</span></span>

|<span data-ttu-id="35bd0-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="35bd0-108">Permission type</span></span>|<span data-ttu-id="35bd0-109">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="35bd0-109">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="35bd0-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="35bd0-110">Delegated (work or school account)</span></span>| <span data-ttu-id="35bd0-111">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="35bd0-111">_varies by context_</span></span>|
| <span data-ttu-id="35bd0-112">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="35bd0-112">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="35bd0-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="35bd0-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="35bd0-114">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="35bd0-114">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="35bd0-115">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="35bd0-115">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="35bd0-116">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="35bd0-116">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="35bd0-117">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="35bd0-117">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="35bd0-118">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="35bd0-118">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="35bd0-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="35bd0-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
|<span data-ttu-id="35bd0-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="35bd0-120">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="35bd0-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35bd0-121">Not supported.</span></span>|
|<span data-ttu-id="35bd0-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="35bd0-122">Application</span></span>|<span data-ttu-id="35bd0-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35bd0-123">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="35bd0-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35bd0-124">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="35bd0-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="35bd0-125">Optional query parameters</span></span>
<span data-ttu-id="35bd0-126">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35bd0-126">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="35bd0-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35bd0-127">Request headers</span></span>
|<span data-ttu-id="35bd0-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35bd0-128">Header</span></span>|<span data-ttu-id="35bd0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="35bd0-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="35bd0-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="35bd0-130">Authorization</span></span>|<span data-ttu-id="35bd0-131">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="35bd0-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="35bd0-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="35bd0-132">Accept</span></span>|<span data-ttu-id="35bd0-133">application/json</span><span class="sxs-lookup"><span data-stu-id="35bd0-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="35bd0-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="35bd0-134">Request body</span></span>
<span data-ttu-id="35bd0-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="35bd0-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="35bd0-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35bd0-136">Response</span></span>
<span data-ttu-id="35bd0-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/intune_shared_user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35bd0-137">If successful, this method returns a `200 OK` response code and [user](../resources/intune_shared_user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="35bd0-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35bd0-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="35bd0-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="35bd0-139">Request</span></span>
<span data-ttu-id="35bd0-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="35bd0-140">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users/{usersId}
```

### <a name="response"></a><span data-ttu-id="35bd0-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35bd0-141">Response</span></span>
<span data-ttu-id="35bd0-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="35bd0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 118

{
  "value": {
    "@odata.type": "#microsoft.graph.user",
    "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
  }
}
```



