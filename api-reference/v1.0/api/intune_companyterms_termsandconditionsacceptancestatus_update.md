# <a name="update-termsandconditionsacceptancestatus"></a><span data-ttu-id="dd17a-101">Actualizar termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="dd17a-101">Update termsAndConditionsAcceptanceStatus</span></span>

> <span data-ttu-id="dd17a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dd17a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dd17a-103">Actualice las propiedades de un objeto [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="dd17a-103">Update the properties of a [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dd17a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dd17a-104">Prerequisites</span></span>
<span data-ttu-id="dd17a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="dd17a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="dd17a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dd17a-107">Permission type</span></span>|<span data-ttu-id="dd17a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dd17a-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dd17a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dd17a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="dd17a-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dd17a-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="dd17a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dd17a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dd17a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd17a-112">Not supported.</span></span>|
|<span data-ttu-id="dd17a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dd17a-113">Application</span></span>|<span data-ttu-id="dd17a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd17a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dd17a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dd17a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="dd17a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dd17a-116">Request headers</span></span>
|<span data-ttu-id="dd17a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd17a-117">Header</span></span>|<span data-ttu-id="dd17a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="dd17a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dd17a-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="dd17a-119">Authorization</span></span>|<span data-ttu-id="dd17a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dd17a-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dd17a-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="dd17a-121">Accept</span></span>|<span data-ttu-id="dd17a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="dd17a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dd17a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dd17a-123">Request body</span></span>
<span data-ttu-id="dd17a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="dd17a-124">In the request body, supply a JSON representation for the [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md) object.</span></span>

<span data-ttu-id="dd17a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="dd17a-125">The following table shows the properties that are required when you create the [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md).</span></span>

|<span data-ttu-id="dd17a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dd17a-126">Property</span></span>|<span data-ttu-id="dd17a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd17a-127">Type</span></span>|<span data-ttu-id="dd17a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd17a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dd17a-129">id</span><span class="sxs-lookup"><span data-stu-id="dd17a-129">id</span></span>|<span data-ttu-id="dd17a-130">String</span><span class="sxs-lookup"><span data-stu-id="dd17a-130">String</span></span>|<span data-ttu-id="dd17a-131">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="dd17a-131">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="dd17a-132">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="dd17a-132">userDisplayName</span></span>|<span data-ttu-id="dd17a-133">String</span><span class="sxs-lookup"><span data-stu-id="dd17a-133">String</span></span>|<span data-ttu-id="dd17a-134">Nombre para mostrar del usuario cuya aceptación representa la entidad.</span><span class="sxs-lookup"><span data-stu-id="dd17a-134">Display name of the user whose acceptance the entity represents.</span></span>|
|<span data-ttu-id="dd17a-135">acceptedVersion</span><span class="sxs-lookup"><span data-stu-id="dd17a-135">acceptedVersion</span></span>|<span data-ttu-id="dd17a-136">Int32</span><span class="sxs-lookup"><span data-stu-id="dd17a-136">Int32</span></span>|<span data-ttu-id="dd17a-137">Número de versión más reciente de los TyC aceptados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="dd17a-137">Most recent version number of the T&C accepted by the user.</span></span>|
|<span data-ttu-id="dd17a-138">acceptedDateTime</span><span class="sxs-lookup"><span data-stu-id="dd17a-138">acceptedDateTime</span></span>|<span data-ttu-id="dd17a-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dd17a-139">DateTimeOffset</span></span>|<span data-ttu-id="dd17a-140">Fecha y hora en la que el usuario aceptó los términos por última vez.</span><span class="sxs-lookup"><span data-stu-id="dd17a-140">DateTime when the terms were last accepted by the user.</span></span>|



## <a name="response"></a><span data-ttu-id="dd17a-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd17a-141">Response</span></span>
<span data-ttu-id="dd17a-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd17a-142">If successful, this method returns a `200 OK` response code and an updated [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dd17a-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dd17a-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="dd17a-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dd17a-144">Request</span></span>
<span data-ttu-id="dd17a-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd17a-145">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}
Content-type: application/json
Content-length: 211

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "userDisplayName": "User Display Name value",
  "acceptedVersion": 15,
  "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
}
```

### <a name="response"></a><span data-ttu-id="dd17a-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd17a-146">Response</span></span>
<span data-ttu-id="dd17a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dd17a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 260

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "id": "a045ce1a-ce1a-a045-1ace-45a01ace45a0",
  "userDisplayName": "User Display Name value",
  "acceptedVersion": 15,
  "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
}
```



