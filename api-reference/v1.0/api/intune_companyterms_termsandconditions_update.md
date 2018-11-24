# <a name="update-termsandconditions"></a><span data-ttu-id="644f3-101">Actualizar termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="644f3-101">Update termsAndConditions</span></span>

> <span data-ttu-id="644f3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="644f3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="644f3-103">Actualice las propiedades de un objeto [termsAndConditions](../resources/intune_companyterms_termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="644f3-103">Update the properties of a [termsAndConditions](../resources/intune_companyterms_termsandconditions.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="644f3-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="644f3-104">Prerequisites</span></span>
<span data-ttu-id="644f3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="644f3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="644f3-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="644f3-107">Permission type</span></span>|<span data-ttu-id="644f3-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="644f3-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="644f3-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="644f3-109">Delegated (work or school account)</span></span>|<span data-ttu-id="644f3-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="644f3-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="644f3-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="644f3-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="644f3-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="644f3-112">Not supported.</span></span>|
|<span data-ttu-id="644f3-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="644f3-113">Application</span></span>|<span data-ttu-id="644f3-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="644f3-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="644f3-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="644f3-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}/termsAndConditions
```

## <a name="request-headers"></a><span data-ttu-id="644f3-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="644f3-116">Request headers</span></span>
|<span data-ttu-id="644f3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="644f3-117">Header</span></span>|<span data-ttu-id="644f3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="644f3-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="644f3-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="644f3-119">Authorization</span></span>|<span data-ttu-id="644f3-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="644f3-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="644f3-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="644f3-121">Accept</span></span>|<span data-ttu-id="644f3-122">application/json</span><span class="sxs-lookup"><span data-stu-id="644f3-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="644f3-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="644f3-123">Request body</span></span>
<span data-ttu-id="644f3-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [termsAndConditions](../resources/intune_companyterms_termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="644f3-124">In the request body, supply a JSON representation for the [termsAndConditions](../resources/intune_companyterms_termsandconditions.md) object.</span></span>

<span data-ttu-id="644f3-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [termsAndConditions](../resources/intune_companyterms_termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="644f3-125">The following table shows the properties that are required when you create the [termsAndConditions](../resources/intune_companyterms_termsandconditions.md).</span></span>

|<span data-ttu-id="644f3-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="644f3-126">Property</span></span>|<span data-ttu-id="644f3-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="644f3-127">Type</span></span>|<span data-ttu-id="644f3-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="644f3-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="644f3-129">id</span><span class="sxs-lookup"><span data-stu-id="644f3-129">id</span></span>|<span data-ttu-id="644f3-130">String</span><span class="sxs-lookup"><span data-stu-id="644f3-130">String</span></span>|<span data-ttu-id="644f3-131">Identificador único de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="644f3-131">Unique identifier of the T&C policy.</span></span>|
|<span data-ttu-id="644f3-132">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="644f3-132">createdDateTime</span></span>|<span data-ttu-id="644f3-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="644f3-133">DateTimeOffset</span></span>|<span data-ttu-id="644f3-134">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="644f3-134">DateTime the object was created.</span></span>|
|<span data-ttu-id="644f3-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="644f3-135">lastModifiedDateTime</span></span>|<span data-ttu-id="644f3-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="644f3-136">DateTimeOffset</span></span>|<span data-ttu-id="644f3-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="644f3-137">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="644f3-138">displayName</span><span class="sxs-lookup"><span data-stu-id="644f3-138">displayName</span></span>|<span data-ttu-id="644f3-139">String</span><span class="sxs-lookup"><span data-stu-id="644f3-139">String</span></span>|<span data-ttu-id="644f3-140">Nombre proporcionado por el administrador de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="644f3-140">Administrator-supplied name for the T&C policy.</span></span> |
|<span data-ttu-id="644f3-141">description</span><span class="sxs-lookup"><span data-stu-id="644f3-141">description</span></span>|<span data-ttu-id="644f3-142">String</span><span class="sxs-lookup"><span data-stu-id="644f3-142">String</span></span>|<span data-ttu-id="644f3-143">Descripción de la directiva de TyC proporcionada por el administrador.</span><span class="sxs-lookup"><span data-stu-id="644f3-143">Administrator-supplied description of the T&C policy.</span></span>|
|<span data-ttu-id="644f3-144">title</span><span class="sxs-lookup"><span data-stu-id="644f3-144">title</span></span>|<span data-ttu-id="644f3-145">String</span><span class="sxs-lookup"><span data-stu-id="644f3-145">String</span></span>|<span data-ttu-id="644f3-146">Título de los términos y condiciones proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="644f3-146">Administrator-supplied title of the terms and conditions.</span></span> <span data-ttu-id="644f3-147">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="644f3-147">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="644f3-148">bodyText</span><span class="sxs-lookup"><span data-stu-id="644f3-148">bodyText</span></span>|<span data-ttu-id="644f3-149">String</span><span class="sxs-lookup"><span data-stu-id="644f3-149">String</span></span>|<span data-ttu-id="644f3-150">Texto de cuerpo de los términos y condiciones proporcionado por el administrador, normalmente los propios términos.</span><span class="sxs-lookup"><span data-stu-id="644f3-150">Administrator-supplied body text of the terms and conditions, typically the terms themselves.</span></span> <span data-ttu-id="644f3-151">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="644f3-151">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="644f3-152">acceptanceStatement</span><span class="sxs-lookup"><span data-stu-id="644f3-152">acceptanceStatement</span></span>|<span data-ttu-id="644f3-153">String</span><span class="sxs-lookup"><span data-stu-id="644f3-153">String</span></span>|<span data-ttu-id="644f3-154">Explicación de los términos y condiciones proporcionada por el administrador, normalmente describe lo que implica aceptar los términos y condiciones de la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="644f3-154">Administrator-supplied explanation of the terms and conditions, typically describing what it means to accept the terms and conditions set out in the T&C policy.</span></span> <span data-ttu-id="644f3-155">Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.</span><span class="sxs-lookup"><span data-stu-id="644f3-155">This is shown to the user on prompts to accept the T&C policy.</span></span>|
|<span data-ttu-id="644f3-156">version</span><span class="sxs-lookup"><span data-stu-id="644f3-156">version</span></span>|<span data-ttu-id="644f3-157">Int32</span><span class="sxs-lookup"><span data-stu-id="644f3-157">Int32</span></span>|<span data-ttu-id="644f3-158">Entero que indica la versión actual de los términos.</span><span class="sxs-lookup"><span data-stu-id="644f3-158">Integer indicating the current version of the terms.</span></span> <span data-ttu-id="644f3-159">Aumenta cuando un administrador realiza un cambio en los términos y quiere que los usuarios tengan que volver a aceptar la directiva de TyC modificada.</span><span class="sxs-lookup"><span data-stu-id="644f3-159">Incremented when an administrator makes a change to the terms and wishes to require users to re-accept the modified T&C policy.</span></span>|



## <a name="response"></a><span data-ttu-id="644f3-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="644f3-160">Response</span></span>
<span data-ttu-id="644f3-161">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [termsAndConditions](../resources/intune_companyterms_termsandconditions.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="644f3-161">If successful, this method returns a `200 OK` response code and an updated [termsAndConditions](../resources/intune_companyterms_termsandconditions.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="644f3-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="644f3-162">Example</span></span>
### <a name="request"></a><span data-ttu-id="644f3-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="644f3-163">Request</span></span>
<span data-ttu-id="644f3-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="644f3-164">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}
Content-type: application/json
Content-length: 273

{
  "@odata.type": "#microsoft.graph.termsAndConditions",
  "displayName": "Display Name value",
  "description": "Description value",
  "title": "Title value",
  "bodyText": "Body Text value",
  "acceptanceStatement": "Acceptance Statement value",
  "version": 7
}
```

### <a name="response"></a><span data-ttu-id="644f3-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="644f3-165">Response</span></span>
<span data-ttu-id="644f3-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="644f3-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 445

{
  "@odata.type": "#microsoft.graph.termsAndConditions",
  "id": "eefc80cf-80cf-eefc-cf80-fceecf80fcee",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "description": "Description value",
  "title": "Title value",
  "bodyText": "Body Text value",
  "acceptanceStatement": "Acceptance Statement value",
  "version": 7
}
```



