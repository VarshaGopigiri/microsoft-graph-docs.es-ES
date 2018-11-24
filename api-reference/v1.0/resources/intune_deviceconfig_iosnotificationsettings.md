# <a name="iosnotificationsettings-resource-type"></a><span data-ttu-id="364b4-101">Tipo de recurso iosNotificationSettings</span><span class="sxs-lookup"><span data-stu-id="364b4-101">iosNotificationSettings resource type</span></span>

> <span data-ttu-id="364b4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="364b4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="364b4-103">Un elemento que describe la configuración de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="364b4-103">An item describing notification setting.</span></span>
## <a name="properties"></a><span data-ttu-id="364b4-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="364b4-104">Properties</span></span>
|<span data-ttu-id="364b4-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="364b4-105">Property</span></span>|<span data-ttu-id="364b4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="364b4-106">Type</span></span>|<span data-ttu-id="364b4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="364b4-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="364b4-108">bundleID</span><span class="sxs-lookup"><span data-stu-id="364b4-108">bundleID</span></span>|<span data-ttu-id="364b4-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="364b4-109">String</span></span>|<span data-ttu-id="364b4-110">Id. de paquete de la aplicación en el que aplicar esa configuración de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="364b4-110">Bundle id of app to which to apply these notification settings.</span></span>|
|<span data-ttu-id="364b4-111">appName</span><span class="sxs-lookup"><span data-stu-id="364b4-111">appName</span></span>|<span data-ttu-id="364b4-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="364b4-112">String</span></span>|<span data-ttu-id="364b4-113">Nombre de la aplicación que se asociará con el bundleID.</span><span class="sxs-lookup"><span data-stu-id="364b4-113">Application name to be associated with the bundleID.</span></span>|
|<span data-ttu-id="364b4-114">publicador</span><span class="sxs-lookup"><span data-stu-id="364b4-114">publisher</span></span>|<span data-ttu-id="364b4-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="364b4-115">String</span></span>|<span data-ttu-id="364b4-116">Publicador que se asociará con el bundleID.</span><span class="sxs-lookup"><span data-stu-id="364b4-116">Publisher to be associated with the bundleID.</span></span>|
|<span data-ttu-id="364b4-117">habilitado</span><span class="sxs-lookup"><span data-stu-id="364b4-117">enabled</span></span>|<span data-ttu-id="364b4-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="364b4-118">Boolean</span></span>|<span data-ttu-id="364b4-119">Indica si se permiten las notificaciones para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="364b4-119">Indicates whether notifications are allowed for this app.</span></span>|
|<span data-ttu-id="364b4-120">showInNotificationCenter</span><span class="sxs-lookup"><span data-stu-id="364b4-120">showInNotificationCenter</span></span>|<span data-ttu-id="364b4-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="364b4-121">Boolean</span></span>|<span data-ttu-id="364b4-122">Indica si se pueden mostrar notificaciones en el centro de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="364b4-122">Indicates whether notifications can be shown in notification center.</span></span>|
|<span data-ttu-id="364b4-123">showOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="364b4-123">showOnLockScreen</span></span>|<span data-ttu-id="364b4-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="364b4-124">Boolean</span></span>|<span data-ttu-id="364b4-125">Indica si se pueden mostrar notificaciones en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="364b4-125">Indicates whether notifications can be shown on the lock screen.</span></span>|
|<span data-ttu-id="364b4-126">alertType</span><span class="sxs-lookup"><span data-stu-id="364b4-126">alertType</span></span>|[<span data-ttu-id="364b4-127">iosNotificationAlertType</span><span class="sxs-lookup"><span data-stu-id="364b4-127">iosNotificationAlertType</span></span>](../resources/intune_deviceconfig_iosnotificationalerttype.md)|<span data-ttu-id="364b4-128">Indica el tipo de alerta para las notificaciones de esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="364b4-128">Indicates the type of alert for notifications for this app.</span></span> <span data-ttu-id="364b4-129">Los valores posibles son: `deviceDefault`, `banner`, `modal` y `none`.</span><span class="sxs-lookup"><span data-stu-id="364b4-129">Possible values are: `deviceDefault`, `banner`, `modal`, `none`.</span></span>|
|<span data-ttu-id="364b4-130">badgesEnabled</span><span class="sxs-lookup"><span data-stu-id="364b4-130">badgesEnabled</span></span>|<span data-ttu-id="364b4-131">Booleano</span><span class="sxs-lookup"><span data-stu-id="364b4-131">Boolean</span></span>|<span data-ttu-id="364b4-132">Indica si se permiten los distintivos para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="364b4-132">Indicates whether badges are allowed for this app.</span></span>|
|<span data-ttu-id="364b4-133">soundsEnabled</span><span class="sxs-lookup"><span data-stu-id="364b4-133">soundsEnabled</span></span>|<span data-ttu-id="364b4-134">Booleano</span><span class="sxs-lookup"><span data-stu-id="364b4-134">Boolean</span></span>|<span data-ttu-id="364b4-135">Indica si se permiten los sonidos para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="364b4-135">Indicates whether sounds are allowed for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="364b4-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="364b4-136">Relationships</span></span>
<span data-ttu-id="364b4-137">Ninguna</span><span class="sxs-lookup"><span data-stu-id="364b4-137">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="364b4-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="364b4-138">JSON Representation</span></span>
<span data-ttu-id="364b4-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="364b4-139">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosNotificationSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosNotificationSettings",
  "bundleID": "String",
  "appName": "String",
  "publisher": "String",
  "enabled": true,
  "showInNotificationCenter": true,
  "showOnLockScreen": true,
  "alertType": "String",
  "badgesEnabled": true,
  "soundsEnabled": true
}
```



