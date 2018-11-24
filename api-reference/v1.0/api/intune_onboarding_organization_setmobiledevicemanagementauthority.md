# <a name="setmobiledevicemanagementauthority-action"></a><span data-ttu-id="4c8de-101">Acción setMobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="4c8de-101">setMobileDeviceManagementAuthority action</span></span>

> <span data-ttu-id="4c8de-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4c8de-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4c8de-103">Establecer la entidad de administración de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="4c8de-103">Set mobile device management authority</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4c8de-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4c8de-104">Prerequisites</span></span>
<span data-ttu-id="4c8de-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4c8de-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4c8de-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4c8de-107">Permission type</span></span>|<span data-ttu-id="4c8de-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4c8de-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4c8de-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4c8de-109">Delegated (work or school account)</span></span>|<span data-ttu-id="4c8de-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4c8de-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="4c8de-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4c8de-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4c8de-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c8de-112">Not supported.</span></span>|
|<span data-ttu-id="4c8de-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4c8de-113">Application</span></span>|<span data-ttu-id="4c8de-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c8de-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4c8de-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4c8de-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /organization/{organizationId}/setMobileDeviceManagementAuthority
```

## <a name="request-headers"></a><span data-ttu-id="4c8de-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4c8de-116">Request headers</span></span>
|<span data-ttu-id="4c8de-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c8de-117">Header</span></span>|<span data-ttu-id="4c8de-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4c8de-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4c8de-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="4c8de-119">Authorization</span></span>|<span data-ttu-id="4c8de-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4c8de-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4c8de-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4c8de-121">Accept</span></span>|<span data-ttu-id="4c8de-122">application/json</span><span class="sxs-lookup"><span data-stu-id="4c8de-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4c8de-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4c8de-123">Request body</span></span>
<span data-ttu-id="4c8de-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4c8de-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4c8de-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c8de-125">Response</span></span>
<span data-ttu-id="4c8de-126">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y un Int32 en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c8de-126">If successful, this action returns a `200 OK` response code and a Int32 in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4c8de-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c8de-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="4c8de-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4c8de-128">Request</span></span>
<span data-ttu-id="4c8de-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c8de-129">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/organization/{organizationId}/setMobileDeviceManagementAuthority
```

### <a name="response"></a><span data-ttu-id="4c8de-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c8de-130">Response</span></span>
<span data-ttu-id="4c8de-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4c8de-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 18

{
  "value": 2
}
```



