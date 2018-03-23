# <a name="update-telecomexpensemanagementpartner"></a><span data-ttu-id="93bed-101">Actualizar telecomExpenseManagementPartner</span><span class="sxs-lookup"><span data-stu-id="93bed-101">Update telecomExpenseManagementPartner</span></span>

> <span data-ttu-id="93bed-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="93bed-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="93bed-103">Actualice las propiedades de un objeto [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="93bed-103">Update the properties of a [calendar](../resources/intune_tem_telecomexpensemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="93bed-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="93bed-104">Prerequisites</span></span>
<span data-ttu-id="93bed-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="93bed-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="93bed-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="93bed-107">Permission type</span></span>|<span data-ttu-id="93bed-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="93bed-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="93bed-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="93bed-109">Delegated (work or school account)</span></span>|<span data-ttu-id="93bed-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="93bed-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="93bed-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="93bed-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="93bed-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="93bed-112">Not supported.</span></span>|
|<span data-ttu-id="93bed-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="93bed-113">Application</span></span>|<span data-ttu-id="93bed-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="93bed-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="93bed-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="93bed-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/telecomExpenseManagementPartners/{telecomExpenseManagementPartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="93bed-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="93bed-116">Request headers</span></span>
|<span data-ttu-id="93bed-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93bed-117">Header</span></span>|<span data-ttu-id="93bed-118">Valor</span><span class="sxs-lookup"><span data-stu-id="93bed-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="93bed-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="93bed-119">Authorization</span></span>|<span data-ttu-id="93bed-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="93bed-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="93bed-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="93bed-121">Accept</span></span>|<span data-ttu-id="93bed-122">application/json</span><span class="sxs-lookup"><span data-stu-id="93bed-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="93bed-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="93bed-123">Request body</span></span>
<span data-ttu-id="93bed-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="93bed-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_tem_telecomexpensemanagementpartner.md) object.</span></span>

<span data-ttu-id="93bed-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="93bed-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="93bed-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="93bed-126">Property</span></span>|<span data-ttu-id="93bed-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="93bed-127">Type</span></span>|<span data-ttu-id="93bed-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="93bed-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="93bed-129">id</span><span class="sxs-lookup"><span data-stu-id="93bed-129">id</span></span>|<span data-ttu-id="93bed-130">String</span><span class="sxs-lookup"><span data-stu-id="93bed-130">String</span></span>|<span data-ttu-id="93bed-131">Identificador único del partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="93bed-131">Unique identifier of the TEM partner.</span></span>|
|<span data-ttu-id="93bed-132">displayName</span><span class="sxs-lookup"><span data-stu-id="93bed-132">displayName</span></span>|<span data-ttu-id="93bed-133">String</span><span class="sxs-lookup"><span data-stu-id="93bed-133">String</span></span>|<span data-ttu-id="93bed-134">Nombre para mostrar del partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="93bed-134">Display name of the TEM partner.</span></span>|
|<span data-ttu-id="93bed-135">url</span><span class="sxs-lookup"><span data-stu-id="93bed-135">url</span></span>|<span data-ttu-id="93bed-136">String</span><span class="sxs-lookup"><span data-stu-id="93bed-136">String</span></span>|<span data-ttu-id="93bed-137">Dirección URL del panel de control administrativo del partner de TEM, donde un administrador puede configurar el servicio de su TEM.</span><span class="sxs-lookup"><span data-stu-id="93bed-137">URL of the TEM partner's administrative control panel, where an administrator can configure their TEM service.</span></span>|
|<span data-ttu-id="93bed-138">appAuthorized</span><span class="sxs-lookup"><span data-stu-id="93bed-138">appAuthorized</span></span>|<span data-ttu-id="93bed-139">Boolean</span><span class="sxs-lookup"><span data-stu-id="93bed-139">Boolean</span></span>|<span data-ttu-id="93bed-140">Si se ha autorizado a la aplicación de AAD del partner para que obtenga acceso a Intune.</span><span class="sxs-lookup"><span data-stu-id="93bed-140">Whether the partner's AAD app has been authorized to access Intune.</span></span>|
|<span data-ttu-id="93bed-141">enabled</span><span class="sxs-lookup"><span data-stu-id="93bed-141">enabled</span></span>|<span data-ttu-id="93bed-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="93bed-142">Boolean</span></span>|<span data-ttu-id="93bed-143">Si la conexión de Intune al servicio de TEM está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="93bed-143">Whether Intune's connection to the TEM service is currently enabled or disabled.</span></span>|
|<span data-ttu-id="93bed-144">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="93bed-144">lastConnectionDateTime</span></span>|<span data-ttu-id="93bed-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="93bed-145">DateTimeOffset</span></span>|<span data-ttu-id="93bed-146">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="93bed-146">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="93bed-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93bed-147">Response</span></span>
<span data-ttu-id="93bed-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93bed-148">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_tem_telecomexpensemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="93bed-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="93bed-149">Example</span></span>
### <a name="request"></a><span data-ttu-id="93bed-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="93bed-150">Request</span></span>
<span data-ttu-id="93bed-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="93bed-151">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/telecomExpenseManagementPartners/{telecomExpenseManagementPartnerId}
Content-type: application/json
Content-length: 178

{
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```

### <a name="response"></a><span data-ttu-id="93bed-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93bed-152">Response</span></span>
<span data-ttu-id="93bed-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="93bed-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 297

{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "id": "47a3b399-b399-47a3-99b3-a34799b3a347",
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```



