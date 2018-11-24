# <a name="iosstoreappassignmentsettings-resource-type"></a><span data-ttu-id="530c7-101">Tipo de recurso iosStoreAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="530c7-101">iosStoreAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="530c7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="530c7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="530c7-103">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de la tienda iOS.</span><span class="sxs-lookup"><span data-stu-id="530c7-103">Contains properties used to assign an iOS Store mobile app to a group.</span></span>

<span data-ttu-id="530c7-104">Hereda de [mobileAppAssignmentSettings](../resources/intune_apps_mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="530c7-104">Inherits from [mobileAppAssignmentSettings](../resources/intune_apps_mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="530c7-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="530c7-105">Properties</span></span>
|<span data-ttu-id="530c7-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="530c7-106">Property</span></span>|<span data-ttu-id="530c7-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="530c7-107">Type</span></span>|<span data-ttu-id="530c7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="530c7-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="530c7-109">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="530c7-109">vpnConfigurationId</span></span>|<span data-ttu-id="530c7-110">cadena</span><span class="sxs-lookup"><span data-stu-id="530c7-110">String</span></span>|<span data-ttu-id="530c7-111">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="530c7-111">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="530c7-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="530c7-112">Relationships</span></span>
<span data-ttu-id="530c7-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="530c7-113">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="530c7-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="530c7-114">JSON Representation</span></span>
<span data-ttu-id="530c7-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="530c7-115">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosStoreAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosStoreAppAssignmentSettings",
  "vpnConfigurationId": "String"
}
```



