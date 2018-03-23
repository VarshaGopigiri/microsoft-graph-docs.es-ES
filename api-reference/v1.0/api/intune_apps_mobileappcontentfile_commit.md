# <a name="commit-action"></a><span data-ttu-id="098e1-101">Acción commit</span><span class="sxs-lookup"><span data-stu-id="098e1-101">commit action</span></span>

> <span data-ttu-id="098e1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="098e1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="098e1-103">Confirma un archivo de una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="098e1-103">Commits a file of a given app.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="098e1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="098e1-104">Prerequisites</span></span>
<span data-ttu-id="098e1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="098e1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="098e1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="098e1-107">Permission type</span></span>|<span data-ttu-id="098e1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="098e1-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="098e1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="098e1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="098e1-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="098e1-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="098e1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="098e1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="098e1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="098e1-112">Not supported.</span></span>|
|<span data-ttu-id="098e1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="098e1-113">Application</span></span>|<span data-ttu-id="098e1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="098e1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="098e1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="098e1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}/commit
```

## <a name="request-headers"></a><span data-ttu-id="098e1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="098e1-116">Request headers</span></span>
|<span data-ttu-id="098e1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="098e1-117">Header</span></span>|<span data-ttu-id="098e1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="098e1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="098e1-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="098e1-119">Authorization</span></span>|<span data-ttu-id="098e1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="098e1-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="098e1-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="098e1-121">Accept</span></span>|<span data-ttu-id="098e1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="098e1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="098e1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="098e1-123">Request body</span></span>
<span data-ttu-id="098e1-124">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="098e1-124">In the request body, supply a JSON representation of the Contact object.</span></span>

<span data-ttu-id="098e1-125">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="098e1-125">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="098e1-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="098e1-126">Property</span></span>|<span data-ttu-id="098e1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="098e1-127">Type</span></span>|<span data-ttu-id="098e1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="098e1-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="098e1-129">fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="098e1-129">fileEncryptionInfo</span></span>|[<span data-ttu-id="098e1-130">fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="098e1-130">fileEncryptionInfo</span></span>](../resources/intune_apps_fileencryptioninfo.md)|<span data-ttu-id="098e1-131">Clave de parámetro de información de cifrado del archivo.</span><span class="sxs-lookup"><span data-stu-id="098e1-131">File encryption info parameter key.</span></span>|



## <a name="response"></a><span data-ttu-id="098e1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="098e1-132">Response</span></span>
<span data-ttu-id="098e1-133">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="098e1-133">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="098e1-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="098e1-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="098e1-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="098e1-135">Request</span></span>
<span data-ttu-id="098e1-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="098e1-136">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="098e1-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="098e1-137">Response</span></span>
<span data-ttu-id="098e1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="098e1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



