# <a name="deviceenrollmentplatformrestriction-resource-type"></a><span data-ttu-id="c74ae-101">Tipo de recurso deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="c74ae-101">deviceEnrollmentPlatformRestriction resource type</span></span>

> <span data-ttu-id="c74ae-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c74ae-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c74ae-103">Restricciones de inscripción específicas de la plataforma</span><span class="sxs-lookup"><span data-stu-id="c74ae-103">Platform specific enrollment restrictions</span></span>
## <a name="properties"></a><span data-ttu-id="c74ae-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c74ae-104">Properties</span></span>
|<span data-ttu-id="c74ae-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c74ae-105">Property</span></span>|<span data-ttu-id="c74ae-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="c74ae-106">Type</span></span>|<span data-ttu-id="c74ae-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c74ae-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c74ae-108">platformBlocked</span><span class="sxs-lookup"><span data-stu-id="c74ae-108">platformBlocked</span></span>|<span data-ttu-id="c74ae-109">Booleano</span><span class="sxs-lookup"><span data-stu-id="c74ae-109">Boolean</span></span>|<span data-ttu-id="c74ae-110">Impedir que la plataforma se inscriba</span><span class="sxs-lookup"><span data-stu-id="c74ae-110">Block the platform from enrolling</span></span>|
|<span data-ttu-id="c74ae-111">personalDeviceEnrollmentBlocked</span><span class="sxs-lookup"><span data-stu-id="c74ae-111">personalDeviceEnrollmentBlocked</span></span>|<span data-ttu-id="c74ae-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="c74ae-112">Boolean</span></span>|<span data-ttu-id="c74ae-113">Impedir que los dispositivos de propiedad personal se inscriban</span><span class="sxs-lookup"><span data-stu-id="c74ae-113">Block personally owned devices from enrolling</span></span>|
|<span data-ttu-id="c74ae-114">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="c74ae-114">osMinimumVersion</span></span>|<span data-ttu-id="c74ae-115">cadena</span><span class="sxs-lookup"><span data-stu-id="c74ae-115">String</span></span>|<span data-ttu-id="c74ae-116">Versión de sistema operativo mínima compatible</span><span class="sxs-lookup"><span data-stu-id="c74ae-116">Min OS version supported</span></span>|
|<span data-ttu-id="c74ae-117">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="c74ae-117">osMaximumVersion</span></span>|<span data-ttu-id="c74ae-118">cadena</span><span class="sxs-lookup"><span data-stu-id="c74ae-118">String</span></span>|<span data-ttu-id="c74ae-119">Versión de sistema operativo máxima compatible</span><span class="sxs-lookup"><span data-stu-id="c74ae-119">Max OS version supported</span></span>|

## <a name="relationships"></a><span data-ttu-id="c74ae-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c74ae-120">Relationships</span></span>
<span data-ttu-id="c74ae-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c74ae-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c74ae-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c74ae-122">JSON Representation</span></span>
<span data-ttu-id="c74ae-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c74ae-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestriction",
  "platformBlocked": true,
  "personalDeviceEnrollmentBlocked": true,
  "osMinimumVersion": "String",
  "osMaximumVersion": "String"
}
```



