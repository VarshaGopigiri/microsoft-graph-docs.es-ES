# <a name="getmanagedapppolicies-function"></a><span data-ttu-id="702df-101">Función getManagedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="702df-101">getManagedAppPolicies function</span></span>

> <span data-ttu-id="702df-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="702df-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="702df-103">Obtiene las restricciones de aplicaciones de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="702df-103">Gets app restrictions for a given user.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="702df-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="702df-104">Prerequisites</span></span>
<span data-ttu-id="702df-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="702df-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="702df-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="702df-107">Permission type</span></span>|<span data-ttu-id="702df-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="702df-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="702df-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="702df-109">Delegated (work or school account)</span></span>| <span data-ttu-id="702df-110">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="702df-110">_varies by context_</span></span>|
| <span data-ttu-id="702df-111">&nbsp; &nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="702df-111">.mam</span></span> | <span data-ttu-id="702df-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="702df-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
|<span data-ttu-id="702df-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="702df-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="702df-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="702df-114">Not supported.</span></span>|
|<span data-ttu-id="702df-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="702df-115">Application</span></span>|<span data-ttu-id="702df-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="702df-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="702df-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="702df-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/getManagedAppPolicies
```

## <a name="request-headers"></a><span data-ttu-id="702df-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="702df-118">Request headers</span></span>
|<span data-ttu-id="702df-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="702df-119">Header</span></span>|<span data-ttu-id="702df-120">Valor</span><span class="sxs-lookup"><span data-stu-id="702df-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="702df-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="702df-121">Authorization</span></span>|<span data-ttu-id="702df-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="702df-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="702df-123">Accept</span><span class="sxs-lookup"><span data-stu-id="702df-123">Accept</span></span>|<span data-ttu-id="702df-124">application/json</span><span class="sxs-lookup"><span data-stu-id="702df-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="702df-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="702df-125">Request body</span></span>
<span data-ttu-id="702df-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="702df-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="702df-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="702df-127">Response</span></span>
<span data-ttu-id="702df-128">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="702df-128">If successful, this function returns a `200 OK` response code and a [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="702df-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="702df-129">Example</span></span>

### <a name="request"></a><span data-ttu-id="702df-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="702df-130">Request</span></span>
<span data-ttu-id="702df-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="702df-131">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users/{usersId}/getManagedAppPolicies
```

### <a name="response"></a><span data-ttu-id="702df-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="702df-132">Response</span></span>
<span data-ttu-id="702df-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="702df-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 401

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedAppPolicy",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "3c7b9675-9675-3c7b-7596-7b3c75967b3c",
      "version": "Version value"
    }
  ]
}
```



