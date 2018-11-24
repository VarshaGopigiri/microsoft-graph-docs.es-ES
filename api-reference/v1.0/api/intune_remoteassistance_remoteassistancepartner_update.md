# <a name="update-remoteassistancepartner"></a><span data-ttu-id="5869e-101">Actualizar remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="5869e-101">Update remoteAssistancePartner</span></span>

> <span data-ttu-id="5869e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5869e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5869e-103">Actualice las propiedades de un objeto [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="5869e-103">Update the properties of a [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5869e-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5869e-104">Prerequisites</span></span>
<span data-ttu-id="5869e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5869e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5869e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5869e-107">Permission type</span></span>|<span data-ttu-id="5869e-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5869e-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5869e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5869e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5869e-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5869e-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="5869e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5869e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5869e-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5869e-112">Not supported.</span></span>|
|<span data-ttu-id="5869e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5869e-113">Application</span></span>|<span data-ttu-id="5869e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5869e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5869e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5869e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="5869e-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5869e-116">Request headers</span></span>
|<span data-ttu-id="5869e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5869e-117">Header</span></span>|<span data-ttu-id="5869e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5869e-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5869e-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="5869e-119">Authorization</span></span>|<span data-ttu-id="5869e-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5869e-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5869e-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5869e-121">Accept</span></span>|<span data-ttu-id="5869e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5869e-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5869e-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5869e-123">Request body</span></span>
<span data-ttu-id="5869e-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="5869e-124">In the request body, supply a JSON representation for the [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md) object.</span></span>

<span data-ttu-id="5869e-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="5869e-125">The following table shows the properties that are required when you create the [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md).</span></span>

|<span data-ttu-id="5869e-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5869e-126">Property</span></span>|<span data-ttu-id="5869e-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5869e-127">Type</span></span>|<span data-ttu-id="5869e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5869e-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5869e-129">id</span><span class="sxs-lookup"><span data-stu-id="5869e-129">id</span></span>|<span data-ttu-id="5869e-130">String</span><span class="sxs-lookup"><span data-stu-id="5869e-130">String</span></span>|<span data-ttu-id="5869e-131">Identificador único del partner.</span><span class="sxs-lookup"><span data-stu-id="5869e-131">Unique identifier of the partner.</span></span>|
|<span data-ttu-id="5869e-132">displayName</span><span class="sxs-lookup"><span data-stu-id="5869e-132">displayName</span></span>|<span data-ttu-id="5869e-133">String</span><span class="sxs-lookup"><span data-stu-id="5869e-133">String</span></span>|<span data-ttu-id="5869e-134">Nombre para mostrar del partner.</span><span class="sxs-lookup"><span data-stu-id="5869e-134">Display name of the partner.</span></span>|
|<span data-ttu-id="5869e-135">onboardingUrl</span><span class="sxs-lookup"><span data-stu-id="5869e-135">onboardingUrl</span></span>|<span data-ttu-id="5869e-136">String</span><span class="sxs-lookup"><span data-stu-id="5869e-136">String</span></span>|<span data-ttu-id="5869e-137">Dirección URL del portal de integración del partner, donde un administrador puede configurar el servicio de Asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="5869e-137">URL of the partner's onboarding portal, where an administrator can configure their Remote Assistance service.</span></span>|
|<span data-ttu-id="5869e-138">onboardingStatus</span><span class="sxs-lookup"><span data-stu-id="5869e-138">onboardingStatus</span></span>|[<span data-ttu-id="5869e-139">remoteAssistanceOnboardingStatus</span><span class="sxs-lookup"><span data-stu-id="5869e-139">remoteAssistanceOnboardingStatus</span></span>](../resources/intune_remoteassistance_remoteassistanceonboardingstatus.md)|<span data-ttu-id="5869e-140">TBD.</span><span class="sxs-lookup"><span data-stu-id="5869e-140">TBD.</span></span> <span data-ttu-id="5869e-141">Los valores posibles son: `notOnboarded`, `onboarding` y `onboarded`.</span><span class="sxs-lookup"><span data-stu-id="5869e-141">Possible values are: `notOnboarded`, `onboarding`, `onboarded`.</span></span>|
|<span data-ttu-id="5869e-142">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="5869e-142">lastConnectionDateTime</span></span>|<span data-ttu-id="5869e-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5869e-143">DateTimeOffset</span></span>|<span data-ttu-id="5869e-144">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="5869e-144">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="5869e-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5869e-145">Response</span></span>
<span data-ttu-id="5869e-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5869e-146">If successful, this method returns a `200 OK` response code and an updated [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5869e-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5869e-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="5869e-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5869e-148">Request</span></span>
<span data-ttu-id="5869e-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5869e-149">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
Content-type: application/json
Content-length: 266

{
  "@odata.type": "#microsoft.graph.remoteAssistancePartner",
  "displayName": "Display Name value",
  "onboardingUrl": "https://example.com/onboardingUrl/",
  "onboardingStatus": "onboarding",
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```

### <a name="response"></a><span data-ttu-id="5869e-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5869e-150">Response</span></span>
<span data-ttu-id="5869e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5869e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 315

{
  "@odata.type": "#microsoft.graph.remoteAssistancePartner",
  "id": "7443c8b9-c8b9-7443-b9c8-4374b9c84374",
  "displayName": "Display Name value",
  "onboardingUrl": "https://example.com/onboardingUrl/",
  "onboardingStatus": "onboarding",
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```



