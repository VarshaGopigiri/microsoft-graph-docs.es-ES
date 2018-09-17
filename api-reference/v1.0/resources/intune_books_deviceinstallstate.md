# <a name="deviceinstallstate-resource-type"></a><span data-ttu-id="97831-101">Tipo de recurso deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="97831-101">deviceInstallState resource type</span></span>

> <span data-ttu-id="97831-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="97831-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="97831-103">Contiene las propiedades del estado de la instalación para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97831-103">Contains properties for the installation state for a device.</span></span>
## <a name="methods"></a><span data-ttu-id="97831-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="97831-104">Methods</span></span>
|<span data-ttu-id="97831-105">Método</span><span class="sxs-lookup"><span data-stu-id="97831-105">Method</span></span>|<span data-ttu-id="97831-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97831-106">Return Type</span></span>|<span data-ttu-id="97831-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="97831-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="97831-108">Enumerar deviceInstallStates</span><span class="sxs-lookup"><span data-stu-id="97831-108">List deviceInstallStates</span></span>](../api/intune_books_deviceinstallstate_list.md)|<span data-ttu-id="97831-109">Colección [deviceInstallState](../resources/intune_books_deviceinstallstate.md)</span><span class="sxs-lookup"><span data-stu-id="97831-109">[deviceInstallState](../resources/intune_books_deviceinstallstate.md) collection</span></span>|<span data-ttu-id="97831-110">Enumere las propiedades y las relaciones de los objetos [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="97831-110">List properties and relationships of the [deviceInstallState](../resources/intune_books_deviceinstallstate.md) objects.</span></span>|
|[<span data-ttu-id="97831-111">Obtener deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="97831-111">Get deviceInstallState</span></span>](../api/intune_books_deviceinstallstate_get.md)|[<span data-ttu-id="97831-112">deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="97831-112">deviceInstallState</span></span>](../resources/intune_books_deviceinstallstate.md)|<span data-ttu-id="97831-113">Lea las propiedades y las relaciones del objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="97831-113">Read properties and relationships of the [deviceInstallState](../resources/intune_books_deviceinstallstate.md) object.</span></span>|
|[<span data-ttu-id="97831-114">Crear deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="97831-114">Create deviceInstallState</span></span>](../api/intune_books_deviceinstallstate_create.md)|[<span data-ttu-id="97831-115">deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="97831-115">deviceInstallState</span></span>](../resources/intune_books_deviceinstallstate.md)|<span data-ttu-id="97831-116">Cree un objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="97831-116">Create a new [deviceInstallState](../resources/intune_books_deviceinstallstate.md) object.</span></span>|
|[<span data-ttu-id="97831-117">Eliminar deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="97831-117">Delete deviceInstallState</span></span>](../api/intune_books_deviceinstallstate_delete.md)|<span data-ttu-id="97831-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="97831-118">None</span></span>|<span data-ttu-id="97831-119">Elimina un [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="97831-119">Deletes a [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span></span>|
|[<span data-ttu-id="97831-120">Actualizar deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="97831-120">Update deviceInstallState</span></span>](../api/intune_books_deviceinstallstate_update.md)|[<span data-ttu-id="97831-121">deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="97831-121">deviceInstallState</span></span>](../resources/intune_books_deviceinstallstate.md)|<span data-ttu-id="97831-122">Actualice las propiedades de un objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="97831-122">Update the properties of a [deviceInstallState](../resources/intune_books_deviceinstallstate.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="97831-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97831-123">Properties</span></span>
|<span data-ttu-id="97831-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="97831-124">Property</span></span>|<span data-ttu-id="97831-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="97831-125">Type</span></span>|<span data-ttu-id="97831-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="97831-126">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="97831-127">id.</span><span class="sxs-lookup"><span data-stu-id="97831-127">id</span></span>|<span data-ttu-id="97831-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="97831-128">String</span></span>|<span data-ttu-id="97831-129">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="97831-129">Key of the entity.</span></span>|
|<span data-ttu-id="97831-130">deviceName</span><span class="sxs-lookup"><span data-stu-id="97831-130">deviceName</span></span>|<span data-ttu-id="97831-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="97831-131">String</span></span>|<span data-ttu-id="97831-132">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97831-132">Device name.</span></span>|
|<span data-ttu-id="97831-133">deviceId</span><span class="sxs-lookup"><span data-stu-id="97831-133">deviceId</span></span>|<span data-ttu-id="97831-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="97831-134">String</span></span>|<span data-ttu-id="97831-135">Id. del dispositivo</span><span class="sxs-lookup"><span data-stu-id="97831-135">Device Id.</span></span>|
|<span data-ttu-id="97831-136">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="97831-136">lastSyncDateTime</span></span>|<span data-ttu-id="97831-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="97831-137">DateTimeOffset</span></span>|<span data-ttu-id="97831-138">Fecha y hora de la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="97831-138">Last sync date and time.</span></span>|
|<span data-ttu-id="97831-139">installState</span><span class="sxs-lookup"><span data-stu-id="97831-139">installState</span></span>|[<span data-ttu-id="97831-140">installState</span><span class="sxs-lookup"><span data-stu-id="97831-140">installState</span></span>](../resources/intune_books_installstate.md)|<span data-ttu-id="97831-p101">El estado de instalación del libro electrónico. Los valores posibles son: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="97831-p101">The install state of the eBook. The possible values are: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span></span>|
|<span data-ttu-id="97831-143">errorCode</span><span class="sxs-lookup"><span data-stu-id="97831-143">errorCode</span></span>|<span data-ttu-id="97831-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="97831-144">String</span></span>|<span data-ttu-id="97831-145">El código de error si hay errores de instalación.</span><span class="sxs-lookup"><span data-stu-id="97831-145">The error code for install failures.</span></span>|
|<span data-ttu-id="97831-146">osVersion</span><span class="sxs-lookup"><span data-stu-id="97831-146">osVersion</span></span>|<span data-ttu-id="97831-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="97831-147">String</span></span>|<span data-ttu-id="97831-148">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="97831-148">OS Version.</span></span>|
|<span data-ttu-id="97831-149">osDescription</span><span class="sxs-lookup"><span data-stu-id="97831-149">osDescription</span></span>|<span data-ttu-id="97831-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="97831-150">String</span></span>|<span data-ttu-id="97831-151">Descripción del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="97831-151">OS Description.</span></span>|
|<span data-ttu-id="97831-152">userName</span><span class="sxs-lookup"><span data-stu-id="97831-152">userName</span></span>|<span data-ttu-id="97831-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="97831-153">String</span></span>|<span data-ttu-id="97831-154">Nombre de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97831-154">Device User Name.</span></span>|

## <a name="relationships"></a><span data-ttu-id="97831-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="97831-155">Relationships</span></span>
<span data-ttu-id="97831-156">Ninguna</span><span class="sxs-lookup"><span data-stu-id="97831-156">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="97831-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="97831-157">JSON Representation</span></span>
<span data-ttu-id="97831-158">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="97831-158">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceInstallState"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceInstallState",
  "id": "String (identifier)",
  "deviceName": "String",
  "deviceId": "String",
  "lastSyncDateTime": "String (timestamp)",
  "installState": "String",
  "errorCode": "String",
  "osVersion": "String",
  "osDescription": "String",
  "userName": "String"
}
```








