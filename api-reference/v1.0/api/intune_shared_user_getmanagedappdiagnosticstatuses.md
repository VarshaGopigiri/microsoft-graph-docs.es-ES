# <a name="getmanagedappdiagnosticstatuses-function"></a><span data-ttu-id="b2535-101">Función getManagedAppDiagnosticStatuses</span><span class="sxs-lookup"><span data-stu-id="b2535-101">getManagedAppDiagnosticStatuses function</span></span>

> <span data-ttu-id="b2535-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b2535-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b2535-103">Obtiene estados de validación de diagnósticos de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="b2535-103">Gets diagnostics validation status for a given user.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b2535-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b2535-104">Prerequisites</span></span>
<span data-ttu-id="b2535-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b2535-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b2535-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b2535-107">Permission type</span></span>|<span data-ttu-id="b2535-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b2535-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b2535-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b2535-109">Delegated (work or school account)</span></span>| <span data-ttu-id="b2535-110">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="b2535-110">_varies by context_</span></span>|
| <span data-ttu-id="b2535-111">&nbsp; &nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="b2535-111">.mam</span></span> | <span data-ttu-id="b2535-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="b2535-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
|<span data-ttu-id="b2535-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b2535-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b2535-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2535-114">Not supported.</span></span>|
|<span data-ttu-id="b2535-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b2535-115">Application</span></span>|<span data-ttu-id="b2535-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2535-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b2535-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b2535-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/getManagedAppDiagnosticStatuses
```

## <a name="request-headers"></a><span data-ttu-id="b2535-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2535-118">Request headers</span></span>
|<span data-ttu-id="b2535-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2535-119">Header</span></span>|<span data-ttu-id="b2535-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b2535-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b2535-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b2535-121">Authorization</span></span>|<span data-ttu-id="b2535-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b2535-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b2535-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b2535-123">Accept</span></span>|<span data-ttu-id="b2535-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b2535-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b2535-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b2535-125">Request body</span></span>
<span data-ttu-id="b2535-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b2535-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b2535-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2535-127">Response</span></span>
<span data-ttu-id="b2535-128">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección [managedAppDiagnosticStatus](../resources/intune_mam_managedappdiagnosticstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2535-128">If successful, this function returns a `200 OK` response code and a [managedAppDiagnosticStatus](../resources/intune_mam_managedappdiagnosticstatus.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b2535-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2535-129">Example</span></span>

### <a name="request"></a><span data-ttu-id="b2535-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b2535-130">Request</span></span>
<span data-ttu-id="b2535-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2535-131">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users/{usersId}/getManagedAppDiagnosticStatuses
```

### <a name="response"></a><span data-ttu-id="b2535-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2535-132">Response</span></span>
<span data-ttu-id="b2535-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b2535-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 249

{
  "value": [
    {
      "@odata.type": "microsoft.graph.managedAppDiagnosticStatus",
      "validationName": "Validation Name value",
      "state": "State value",
      "mitigationInstruction": "Mitigation Instruction value"
    }
  ]
}
```



