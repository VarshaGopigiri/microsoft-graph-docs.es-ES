# <a name="ioslobappassignmentsettings-resource-type"></a><span data-ttu-id="12b7c-101">Tipo de recurso iosLobAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="12b7c-101">iosLobAppAssignmentSettings resource type</span></span>

> <span data-ttu-id="12b7c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="12b7c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="12b7c-103">Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de línea de negocio para iOS.</span><span class="sxs-lookup"><span data-stu-id="12b7c-103">Contains properties used to assign an iOS LOB mobile app to a group.</span></span>

<span data-ttu-id="12b7c-104">Hereda de [mobileAppAssignmentSettings](../resources/intune_apps_mobileappassignmentsettings.md)</span><span class="sxs-lookup"><span data-stu-id="12b7c-104">Inherits from [mobileAppAssignmentSettings](../resources/intune_apps_mobileappassignmentsettings.md)</span></span>

## <a name="properties"></a><span data-ttu-id="12b7c-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12b7c-105">Properties</span></span>
|<span data-ttu-id="12b7c-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="12b7c-106">Property</span></span>|<span data-ttu-id="12b7c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="12b7c-107">Type</span></span>|<span data-ttu-id="12b7c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="12b7c-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="12b7c-109">vpnConfigurationId</span><span class="sxs-lookup"><span data-stu-id="12b7c-109">vpnConfigurationId</span></span>|<span data-ttu-id="12b7c-110">cadena</span><span class="sxs-lookup"><span data-stu-id="12b7c-110">String</span></span>|<span data-ttu-id="12b7c-111">El identificador de configuración de VPN que se aplicará a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="12b7c-111">The VPN Configuration Id to apply for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="12b7c-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="12b7c-112">Relationships</span></span>
<span data-ttu-id="12b7c-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="12b7c-113">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="12b7c-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="12b7c-114">JSON Representation</span></span>
<span data-ttu-id="12b7c-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="12b7c-115">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.mobileAppAssignmentSettings",
  "@odata.type": "microsoft.graph.iosLobAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosLobAppAssignmentSettings",
  "vpnConfigurationId": "String"
}
```



