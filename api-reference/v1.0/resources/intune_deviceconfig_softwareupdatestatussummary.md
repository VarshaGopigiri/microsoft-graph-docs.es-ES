# <a name="softwareupdatestatussummary-resource-type"></a><span data-ttu-id="798bb-101">Tipo de recurso softwareUpdateStatusSummary</span><span class="sxs-lookup"><span data-stu-id="798bb-101">softwareUpdateStatusSummary resource type</span></span>

> <span data-ttu-id="798bb-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="798bb-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="798bb-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="798bb-103">Not yet documented</span></span>
## <a name="methods"></a><span data-ttu-id="798bb-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="798bb-104">Methods</span></span>
|<span data-ttu-id="798bb-105">Método</span><span class="sxs-lookup"><span data-stu-id="798bb-105">Method</span></span>|<span data-ttu-id="798bb-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="798bb-106">Return Type</span></span>|<span data-ttu-id="798bb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="798bb-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="798bb-108">Obtener softwareUpdateStatusSummary</span><span class="sxs-lookup"><span data-stu-id="798bb-108">Get softwareUpdateStatusSummary</span></span>](../api/intune_deviceconfig_softwareupdatestatussummary_get.md)|[<span data-ttu-id="798bb-109">softwareUpdateStatusSummary</span><span class="sxs-lookup"><span data-stu-id="798bb-109">softwareUpdateStatusSummary</span></span>](../resources/intune_deviceconfig_softwareupdatestatussummary.md)|<span data-ttu-id="798bb-110">Lea las propiedades y las relaciones del objeto [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="798bb-110">Read properties and relationships of [plannerProgressTaskBoardTaskFormat](../resources/intune_deviceconfig_softwareupdatestatussummary.md) object.</span></span>|
|[<span data-ttu-id="798bb-111">Actualizar softwareUpdateStatusSummary</span><span class="sxs-lookup"><span data-stu-id="798bb-111">Update softwareUpdateStatusSummary</span></span>](../api/intune_deviceconfig_softwareupdatestatussummary_update.md)|[<span data-ttu-id="798bb-112">softwareUpdateStatusSummary</span><span class="sxs-lookup"><span data-stu-id="798bb-112">softwareUpdateStatusSummary</span></span>](../resources/intune_deviceconfig_softwareupdatestatussummary.md)|<span data-ttu-id="798bb-113">Actualice las propiedades de un objeto [softwareUpdateStatusSummary](../resources/intune_deviceconfig_softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="798bb-113">Update the properties of a [calendar](../resources/intune_deviceconfig_softwareupdatestatussummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="798bb-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="798bb-114">Properties</span></span>
|<span data-ttu-id="798bb-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="798bb-115">Property</span></span>|<span data-ttu-id="798bb-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="798bb-116">Type</span></span>|<span data-ttu-id="798bb-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="798bb-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="798bb-118">id</span><span class="sxs-lookup"><span data-stu-id="798bb-118">id</span></span>|<span data-ttu-id="798bb-119">cadena</span><span class="sxs-lookup"><span data-stu-id="798bb-119">String</span></span>|<span data-ttu-id="798bb-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="798bb-120">Key of the setting.</span></span>|
|<span data-ttu-id="798bb-121">displayName</span><span class="sxs-lookup"><span data-stu-id="798bb-121">displayName</span></span>|<span data-ttu-id="798bb-122">cadena</span><span class="sxs-lookup"><span data-stu-id="798bb-122">String</span></span>|<span data-ttu-id="798bb-123">El nombre de la directiva.</span><span class="sxs-lookup"><span data-stu-id="798bb-123">The Name parameter specifies the name of the retention policy tag.</span></span>|
|<span data-ttu-id="798bb-124">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="798bb-124">compliantDeviceCount</span></span>|<span data-ttu-id="798bb-125">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-125">Int32</span></span>|<span data-ttu-id="798bb-126">Número de dispositivos compatibles.</span><span class="sxs-lookup"><span data-stu-id="798bb-126">Number of compliant devices.</span></span>|
|<span data-ttu-id="798bb-127">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="798bb-127">nonCompliantDeviceCount</span></span>|<span data-ttu-id="798bb-128">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-128">Int32</span></span>|<span data-ttu-id="798bb-129">Número de dispositivos no compatibles.</span><span class="sxs-lookup"><span data-stu-id="798bb-129">Number of non compliant devices.</span></span>|
|<span data-ttu-id="798bb-130">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="798bb-130">remediatedDeviceCount</span></span>|<span data-ttu-id="798bb-131">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-131">Int32</span></span>|<span data-ttu-id="798bb-132">Número de dispositivos corregidos.</span><span class="sxs-lookup"><span data-stu-id="798bb-132">Number of remediated devices.</span></span>|
|<span data-ttu-id="798bb-133">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="798bb-133">errorDeviceCount</span></span>|<span data-ttu-id="798bb-134">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-134">Int32</span></span>|<span data-ttu-id="798bb-135">Número de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="798bb-135">Number of devices had error.</span></span>|
|<span data-ttu-id="798bb-136">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="798bb-136">unknownDeviceCount</span></span>|<span data-ttu-id="798bb-137">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-137">Int32</span></span>|<span data-ttu-id="798bb-138">Número de dispositivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="798bb-138">Number of unknown devices.</span></span>|
|<span data-ttu-id="798bb-139">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="798bb-139">conflictDeviceCount</span></span>|<span data-ttu-id="798bb-140">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-140">Int32</span></span>|<span data-ttu-id="798bb-141">Número de dispositivos en conflicto.</span><span class="sxs-lookup"><span data-stu-id="798bb-141">Number of conflict devices.</span></span>|
|<span data-ttu-id="798bb-142">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="798bb-142">notApplicableDeviceCount</span></span>|<span data-ttu-id="798bb-143">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-143">Int32</span></span>|<span data-ttu-id="798bb-144">Número de dispositivos no aplicables.</span><span class="sxs-lookup"><span data-stu-id="798bb-144">Number of not applicable devices.</span></span>|
|<span data-ttu-id="798bb-145">compliantUserCount</span><span class="sxs-lookup"><span data-stu-id="798bb-145">compliantUserCount</span></span>|<span data-ttu-id="798bb-146">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-146">Int32</span></span>|<span data-ttu-id="798bb-147">Número de usuarios compatibles.</span><span class="sxs-lookup"><span data-stu-id="798bb-147">Number of users: 542</span></span>|
|<span data-ttu-id="798bb-148">nonCompliantUserCount</span><span class="sxs-lookup"><span data-stu-id="798bb-148">nonCompliantUserCount</span></span>|<span data-ttu-id="798bb-149">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-149">Int32</span></span>|<span data-ttu-id="798bb-150">Número de usuarios no compatibles.</span><span class="sxs-lookup"><span data-stu-id="798bb-150">Number of non compliant users.</span></span>|
|<span data-ttu-id="798bb-151">remediatedUserCount</span><span class="sxs-lookup"><span data-stu-id="798bb-151">remediatedUserCount</span></span>|<span data-ttu-id="798bb-152">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-152">Int32</span></span>|<span data-ttu-id="798bb-153">Número de usuarios corregidos.</span><span class="sxs-lookup"><span data-stu-id="798bb-153">Number of users: 542</span></span>|
|<span data-ttu-id="798bb-154">errorUserCount</span><span class="sxs-lookup"><span data-stu-id="798bb-154">errorUserCount</span></span>|<span data-ttu-id="798bb-155">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-155">Int32</span></span>|<span data-ttu-id="798bb-156">Número de usuarios con errores.</span><span class="sxs-lookup"><span data-stu-id="798bb-156">Number of users had error.</span></span>|
|<span data-ttu-id="798bb-157">unknownUserCount</span><span class="sxs-lookup"><span data-stu-id="798bb-157">unknownUserCount</span></span>|<span data-ttu-id="798bb-158">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-158">Int32</span></span>|<span data-ttu-id="798bb-159">Número de usuarios desconocidos.</span><span class="sxs-lookup"><span data-stu-id="798bb-159">Number of users: 542</span></span>|
|<span data-ttu-id="798bb-160">conflictUserCount</span><span class="sxs-lookup"><span data-stu-id="798bb-160">conflictUserCount</span></span>|<span data-ttu-id="798bb-161">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-161">Int32</span></span>|<span data-ttu-id="798bb-162">Número de usuarios en conflicto.</span><span class="sxs-lookup"><span data-stu-id="798bb-162">Number of users: 542</span></span>|
|<span data-ttu-id="798bb-163">notApplicableUserCount</span><span class="sxs-lookup"><span data-stu-id="798bb-163">notApplicableUserCount</span></span>|<span data-ttu-id="798bb-164">Int32</span><span class="sxs-lookup"><span data-stu-id="798bb-164">Int32</span></span>|<span data-ttu-id="798bb-165">Número de usuarios no aplicables.</span><span class="sxs-lookup"><span data-stu-id="798bb-165">Number of not applicable users.</span></span>|

## <a name="relationships"></a><span data-ttu-id="798bb-166">Relaciones</span><span class="sxs-lookup"><span data-stu-id="798bb-166">Relationships</span></span>
<span data-ttu-id="798bb-167">Ninguna</span><span class="sxs-lookup"><span data-stu-id="798bb-167">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="798bb-168">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="798bb-168">JSON Representation</span></span>
<span data-ttu-id="798bb-169">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="798bb-169">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.softwareUpdateStatusSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.softwareUpdateStatusSummary",
  "id": "String (identifier)",
  "displayName": "String",
  "compliantDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "unknownDeviceCount": 1024,
  "conflictDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantUserCount": 1024,
  "nonCompliantUserCount": 1024,
  "remediatedUserCount": 1024,
  "errorUserCount": 1024,
  "unknownUserCount": 1024,
  "conflictUserCount": 1024,
  "notApplicableUserCount": 1024
}
```



