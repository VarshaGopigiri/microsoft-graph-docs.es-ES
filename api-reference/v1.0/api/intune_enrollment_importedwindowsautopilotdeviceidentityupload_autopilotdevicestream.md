# <a name="autopilotdevicestream-function"></a><span data-ttu-id="3b0eb-101">autopilotDeviceStream (función)</span><span class="sxs-lookup"><span data-stu-id="3b0eb-101">autopilotDeviceStream function</span></span>

> <span data-ttu-id="3b0eb-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3b0eb-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3b0eb-103">Crear una solicitud de carga con la secuencia de dispositivo de piloto automático en ella.</span><span class="sxs-lookup"><span data-stu-id="3b0eb-103">Create a upload request with autopilot device stream in it.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3b0eb-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3b0eb-104">Prerequisites</span></span>
<span data-ttu-id="3b0eb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3b0eb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3b0eb-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3b0eb-107">Permission type</span></span>|<span data-ttu-id="3b0eb-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3b0eb-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3b0eb-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3b0eb-109">Delegated (work or school account)</span></span>|<span data-ttu-id="3b0eb-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b0eb-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="3b0eb-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3b0eb-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3b0eb-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b0eb-112">Not supported.</span></span>|
|<span data-ttu-id="3b0eb-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3b0eb-113">Application</span></span>|<span data-ttu-id="3b0eb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b0eb-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3b0eb-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3b0eb-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/autopilotDeviceStream
```

## <a name="request-headers"></a><span data-ttu-id="3b0eb-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3b0eb-116">Request headers</span></span>
|<span data-ttu-id="3b0eb-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b0eb-117">Header</span></span>|<span data-ttu-id="3b0eb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3b0eb-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3b0eb-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="3b0eb-119">Authorization</span></span>|<span data-ttu-id="3b0eb-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3b0eb-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3b0eb-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3b0eb-121">Accept</span></span>|<span data-ttu-id="3b0eb-122">application/json</span><span class="sxs-lookup"><span data-stu-id="3b0eb-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3b0eb-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3b0eb-123">Request body</span></span>
<span data-ttu-id="3b0eb-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3b0eb-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3b0eb-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b0eb-125">Response</span></span>
<span data-ttu-id="3b0eb-126">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un objeto String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b0eb-126">If successful, this function returns a `200 OK` response code and a String in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3b0eb-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3b0eb-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="3b0eb-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3b0eb-128">Request</span></span>
<span data-ttu-id="3b0eb-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b0eb-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/autopilotDeviceStream
```

### <a name="response"></a><span data-ttu-id="3b0eb-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b0eb-130">Response</span></span>
<span data-ttu-id="3b0eb-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3b0eb-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 48

{
  "value": "Autopilot Device Stream value"
}
```



