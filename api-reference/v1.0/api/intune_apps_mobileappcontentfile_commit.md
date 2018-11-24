# <a name="commit-action"></a><span data-ttu-id="b9187-101">Acción commit</span><span class="sxs-lookup"><span data-stu-id="b9187-101">commit action</span></span>

> <span data-ttu-id="b9187-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b9187-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b9187-103">Confirma un archivo de una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="b9187-103">Commits a file of a given app.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b9187-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b9187-104">Prerequisites</span></span>
<span data-ttu-id="b9187-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b9187-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b9187-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b9187-107">Permission type</span></span>|<span data-ttu-id="b9187-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b9187-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b9187-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b9187-109">Delegated (work or school account)</span></span>|<span data-ttu-id="b9187-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b9187-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b9187-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b9187-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b9187-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9187-112">Not supported.</span></span>|
|<span data-ttu-id="b9187-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b9187-113">Application</span></span>|<span data-ttu-id="b9187-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9187-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b9187-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b9187-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}/commit
```

## <a name="request-headers"></a><span data-ttu-id="b9187-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b9187-116">Request headers</span></span>
|<span data-ttu-id="b9187-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9187-117">Header</span></span>|<span data-ttu-id="b9187-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b9187-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b9187-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="b9187-119">Authorization</span></span>|<span data-ttu-id="b9187-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b9187-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b9187-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b9187-121">Accept</span></span>|<span data-ttu-id="b9187-122">application/json</span><span class="sxs-lookup"><span data-stu-id="b9187-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b9187-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b9187-123">Request body</span></span>
<span data-ttu-id="b9187-124">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="b9187-124">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="b9187-125">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="b9187-125">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="b9187-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9187-126">Property</span></span>|<span data-ttu-id="b9187-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9187-127">Type</span></span>|<span data-ttu-id="b9187-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9187-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b9187-129">fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="b9187-129">fileEncryptionInfo</span></span>|[<span data-ttu-id="b9187-130">fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="b9187-130">fileEncryptionInfo</span></span>](../resources/intune_apps_fileencryptioninfo.md)|<span data-ttu-id="b9187-131">Clave de parámetro de información de cifrado del archivo.</span><span class="sxs-lookup"><span data-stu-id="b9187-131">File encryption info parameter key.</span></span>|



## <a name="response"></a><span data-ttu-id="b9187-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9187-132">Response</span></span>
<span data-ttu-id="b9187-133">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b9187-133">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="b9187-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9187-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="b9187-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b9187-135">Request</span></span>
<span data-ttu-id="b9187-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b9187-136">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}/commit

Content-type: application/json
Content-length: 399

{
  "fileEncryptionInfo": {
    "@odata.type": "microsoft.graph.fileEncryptionInfo",
    "encryptionKey": "ZW5jcnlwdGlvbktleQ==",
    "initializationVector": "aW5pdGlhbGl6YXRpb25WZWN0b3I=",
    "mac": "bWFj",
    "macKey": "bWFjS2V5",
    "profileIdentifier": "Profile Identifier value",
    "fileDigest": "ZmlsZURpZ2VzdA==",
    "fileDigestAlgorithm": "File Digest Algorithm value"
  }
}
```

### <a name="response"></a><span data-ttu-id="b9187-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9187-137">Response</span></span>
<span data-ttu-id="b9187-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b9187-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



