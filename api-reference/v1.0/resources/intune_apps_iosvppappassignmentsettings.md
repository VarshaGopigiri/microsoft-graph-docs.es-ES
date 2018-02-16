# <a name="iosvppappassignmentsettings-resource-type"></a><span data-ttu-id="afe3e-101">Tipo de recurso iosVppAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="afe3e-101">iosVppAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="afe3e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="afe3e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="afe3e-103">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.</span><span class="sxs-lookup"><span data-stu-id="afe3e-103">Contains properties used to assign an iOS VPP mobile app to a group.</span></span>

<span data-ttu-id="afe3e-104">Hereda de [mobileAppAssignmentSettings](../resources/intune_apps_mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="afe3e-104">Inherits from [mobileAppAssignmentSettings](../resources/intune_apps_mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="afe3e-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="afe3e-105">Properties</span></span>
|<span data-ttu-id="afe3e-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="afe3e-106">Property</span></span>|<span data-ttu-id="afe3e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="afe3e-107">Type</span></span>|<span data-ttu-id="afe3e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="afe3e-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="afe3e-109">useDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="afe3e-109">useDeviceLicensing</span></span>|<span data-ttu-id="afe3e-110">Booleano</span><span class="sxs-lookup"><span data-stu-id="afe3e-110">Boolean</span></span>|<span data-ttu-id="afe3e-111">Si se deben usar o no las licencias de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="afe3e-111">Whether or not to use device licensing.</span></span>|
|<span data-ttu-id="afe3e-112">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="afe3e-112">vpnConfigurationId</span></span>|<span data-ttu-id="afe3e-113">cadena</span><span class="sxs-lookup"><span data-stu-id="afe3e-113">String</span></span>|<span data-ttu-id="afe3e-114">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="afe3e-114">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="afe3e-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="afe3e-115">Relationships</span></span>
<span data-ttu-id="afe3e-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="afe3e-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="afe3e-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="afe3e-117">JSON Representation</span></span>
<span data-ttu-id="afe3e-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="afe3e-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosVppAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppAppAssignmentSettings",
  "useDeviceLicensing": true,
  "vpnConfigurationId": "String"
}
```



