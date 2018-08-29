# <a name="reportroot-resource-type"></a><span data-ttu-id="5fca8-101">Tipo de recurso reportRoot</span><span class="sxs-lookup"><span data-stu-id="5fca8-101">reportRoot resource type</span></span>

> <span data-ttu-id="5fca8-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5fca8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5fca8-103">El recurso que representa una instancia del historial de informes.</span><span class="sxs-lookup"><span data-stu-id="5fca8-103">The resource that represents an instance of History Reports.</span></span>
## <a name="methods"></a><span data-ttu-id="5fca8-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="5fca8-104">Methods</span></span>
|<span data-ttu-id="5fca8-105">Método</span><span class="sxs-lookup"><span data-stu-id="5fca8-105">Method</span></span>|<span data-ttu-id="5fca8-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fca8-106">Return Type</span></span>|<span data-ttu-id="5fca8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fca8-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="5fca8-108">Obtener reportRoot</span><span class="sxs-lookup"><span data-stu-id="5fca8-108">Get reportRoot</span></span>](../api/intune_deviceconfig_reportroot_get.md)|[<span data-ttu-id="5fca8-109">reportRoot</span><span class="sxs-lookup"><span data-stu-id="5fca8-109">reportRoot</span></span>](../resources/intune_deviceconfig_reportroot.md)|<span data-ttu-id="5fca8-110">Lea las propiedades y las relaciones del objeto [reportRoot](../resources/intune_deviceconfig_reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="5fca8-110">Read properties and relationships of the [reportRoot](../resources/intune_deviceconfig_reportroot.md) object.</span></span>|
|[<span data-ttu-id="5fca8-111">Actualizar reportRoot</span><span class="sxs-lookup"><span data-stu-id="5fca8-111">Update reportRoot</span></span>](../api/intune_deviceconfig_reportroot_update.md)|[<span data-ttu-id="5fca8-112">reportRoot</span><span class="sxs-lookup"><span data-stu-id="5fca8-112">reportRoot</span></span>](../resources/intune_deviceconfig_reportroot.md)|<span data-ttu-id="5fca8-113">Actualice las propiedades de un objeto [reportRoot](../resources/intune_deviceconfig_reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="5fca8-113">Update the properties of a [reportRoot](../resources/intune_deviceconfig_reportroot.md) object.</span></span>|
|[<span data-ttu-id="5fca8-114">Función deviceConfigurationUserActivity</span><span class="sxs-lookup"><span data-stu-id="5fca8-114">deviceConfigurationUserActivity function</span></span>](../api/intune_deviceconfig_reportroot_deviceconfigurationuseractivity.md)|[<span data-ttu-id="5fca8-115">report</span><span class="sxs-lookup"><span data-stu-id="5fca8-115">report</span></span>](../resources/intune_deviceconfig_report.md)|<span data-ttu-id="5fca8-116">Metadatos para el informe de actividad de usuario de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5fca8-116">Metadata for the device configuration user activity report</span></span>|
|[<span data-ttu-id="5fca8-117">Función deviceConfigurationDeviceActivity</span><span class="sxs-lookup"><span data-stu-id="5fca8-117">deviceConfigurationDeviceActivity function</span></span>](../api/intune_deviceconfig_reportroot_deviceconfigurationdeviceactivity.md)|[<span data-ttu-id="5fca8-118">report</span><span class="sxs-lookup"><span data-stu-id="5fca8-118">report</span></span>](../resources/intune_deviceconfig_report.md)|<span data-ttu-id="5fca8-119">Metadatos para el informe de actividad de dispositivo de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5fca8-119">Metadata for the device configuration device activity report</span></span>|

## <a name="relationships"></a><span data-ttu-id="5fca8-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5fca8-120">Relationships</span></span>
<span data-ttu-id="5fca8-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5fca8-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5fca8-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5fca8-122">JSON Representation</span></span>
<span data-ttu-id="5fca8-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5fca8-123">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.reportRoot"
}-->
``` json
{
}
```

## <a name="example"></a><span data-ttu-id="5fca8-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5fca8-124">Example</span></span>

<!--{"blockType": "request"}-->
```http
GET https://graph.microsoft.com/v1.0/reports
```

<!--{"blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.reportRoot"}-->
```json
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```
