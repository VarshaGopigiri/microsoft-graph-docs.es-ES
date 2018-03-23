# <a name="requestsignupurl-action"></a><span data-ttu-id="ed3b4-101">Acción requestSignupUrl</span><span class="sxs-lookup"><span data-stu-id="ed3b4-101">requestSignupUrl action</span></span>

> <span data-ttu-id="ed3b4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ed3b4-103">Genera una dirección URL de inicio de sesión que se utiliza para registrarse en la administración de Android for Work.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-103">Generates a sign-up URL that is used to enroll in Android for Work management.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ed3b4-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ed3b4-104">Prerequisites</span></span>
<span data-ttu-id="ed3b4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ed3b4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ed3b4-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed3b4-107">Permission type</span></span>|<span data-ttu-id="ed3b4-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed3b4-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ed3b4-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed3b4-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ed3b4-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed3b4-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ed3b4-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed3b4-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ed3b4-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-112">Not supported.</span></span>|
|<span data-ttu-id="ed3b4-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed3b4-113">Application</span></span>|<span data-ttu-id="ed3b4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ed3b4-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed3b4-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/androidForWorkSettings/requestSignupUrl
```

## <a name="request-headers"></a><span data-ttu-id="ed3b4-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ed3b4-116">Request headers</span></span>
|<span data-ttu-id="ed3b4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed3b4-117">Header</span></span>|<span data-ttu-id="ed3b4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ed3b4-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ed3b4-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="ed3b4-119">Authorization</span></span>|<span data-ttu-id="ed3b4-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="ed3b4-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ed3b4-121">Accept</span></span>|<span data-ttu-id="ed3b4-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ed3b4-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ed3b4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed3b4-123">Request body</span></span>
<span data-ttu-id="ed3b4-124">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-124">In the request body, supply a JSON representation of the Contact object.</span></span>

<span data-ttu-id="ed3b4-125">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-125">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="ed3b4-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed3b4-126">Property</span></span>|<span data-ttu-id="ed3b4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed3b4-127">Type</span></span>|<span data-ttu-id="ed3b4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed3b4-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ed3b4-129">hostName</span><span class="sxs-lookup"><span data-stu-id="ed3b4-129">hostname</span></span>|<span data-ttu-id="ed3b4-130">String</span><span class="sxs-lookup"><span data-stu-id="ed3b4-130">String</span></span>|<span data-ttu-id="ed3b4-131">El nombre de host de la dirección URL de devolución de llamada al que se redirigirá el explorador después de completar correctamente el registro.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-131">The hostname of the callback URL to which the browser will be redirected after successfully completing sign-up.</span></span>|



## <a name="response"></a><span data-ttu-id="ed3b4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed3b4-132">Response</span></span>
<span data-ttu-id="ed3b4-133">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y un objeto String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-133">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ed3b4-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed3b4-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="ed3b4-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ed3b4-135">Request</span></span>
<span data-ttu-id="ed3b4-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-136">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/androidForWorkSettings/requestSignupUrl

Content-type: application/json
Content-length: 37

{
  "hostName": "Host Name value"
}
```

### <a name="response"></a><span data-ttu-id="ed3b4-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed3b4-137">Response</span></span>
<span data-ttu-id="ed3b4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ed3b4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 56

{
  "value": "https://example.com/requestSignupUrl/"
}
```



