# <a name="ebookinstallsummary-resource-type"></a><span data-ttu-id="da0df-101">Tipo de recurso eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="da0df-101">eBookInstallSummary resource type</span></span>

> <span data-ttu-id="da0df-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="da0df-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="da0df-103">Contiene las propiedades del resumen de la instalación de un libro para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da0df-103">Contains properties for the installation summary of a book for a device.</span></span>
## <a name="methods"></a><span data-ttu-id="da0df-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="da0df-104">Methods</span></span>
|<span data-ttu-id="da0df-105">Método</span><span class="sxs-lookup"><span data-stu-id="da0df-105">Method</span></span>|<span data-ttu-id="da0df-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da0df-106">Return Type</span></span>|<span data-ttu-id="da0df-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="da0df-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="da0df-108">Obtener eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="da0df-108">Get eBookInstallSummary</span></span>](../api/intune_books_ebookinstallsummary_get.md)|[<span data-ttu-id="da0df-109">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="da0df-109">eBookInstallSummary</span></span>](../resources/intune_books_ebookinstallsummary.md)|<span data-ttu-id="da0df-110">Lea las propiedades y las relaciones del objeto [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="da0df-110">Read properties and relationships of the [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md) object.</span></span>|
|[<span data-ttu-id="da0df-111">Actualizar eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="da0df-111">Update eBookInstallSummary</span></span>](../api/intune_books_ebookinstallsummary_update.md)|[<span data-ttu-id="da0df-112">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="da0df-112">eBookInstallSummary</span></span>](../resources/intune_books_ebookinstallsummary.md)|<span data-ttu-id="da0df-113">Actualice las propiedades de un objeto [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md).</span><span class="sxs-lookup"><span data-stu-id="da0df-113">Update the properties of a [eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="da0df-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da0df-114">Properties</span></span>
|<span data-ttu-id="da0df-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="da0df-115">Property</span></span>|<span data-ttu-id="da0df-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="da0df-116">Type</span></span>|<span data-ttu-id="da0df-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="da0df-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="da0df-118">id</span><span class="sxs-lookup"><span data-stu-id="da0df-118">id</span></span>|<span data-ttu-id="da0df-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="da0df-119">String</span></span>|<span data-ttu-id="da0df-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="da0df-120">Key of the entity.</span></span>|
|<span data-ttu-id="da0df-121">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="da0df-121">installedDeviceCount</span></span>|<span data-ttu-id="da0df-122">Int32</span><span class="sxs-lookup"><span data-stu-id="da0df-122">Int32</span></span>|<span data-ttu-id="da0df-123">Número de dispositivos que han instalado correctamente este libro.</span><span class="sxs-lookup"><span data-stu-id="da0df-123">Number of Devices that have successfully installed this book.</span></span>|
|<span data-ttu-id="da0df-124">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="da0df-124">failedDeviceCount</span></span>|<span data-ttu-id="da0df-125">Int32</span><span class="sxs-lookup"><span data-stu-id="da0df-125">Int32</span></span>|<span data-ttu-id="da0df-126">Número de dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="da0df-126">Number of Devices that have failed to install this book.</span></span>|
|<span data-ttu-id="da0df-127">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="da0df-127">notInstalledDeviceCount</span></span>|<span data-ttu-id="da0df-128">Int32</span><span class="sxs-lookup"><span data-stu-id="da0df-128">Int32</span></span>|<span data-ttu-id="da0df-129">Número de dispositivos que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="da0df-129">Number of Devices that does not have this book installed.</span></span>|
|<span data-ttu-id="da0df-130">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="da0df-130">installedUserCount</span></span>|<span data-ttu-id="da0df-131">Int32</span><span class="sxs-lookup"><span data-stu-id="da0df-131">Int32</span></span>|<span data-ttu-id="da0df-132">Número de usuarios cuyos dispositivos al completo han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="da0df-132">Number of Users whose devices have all succeeded to install this book.</span></span>|
|<span data-ttu-id="da0df-133">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="da0df-133">failedUserCount</span></span>|<span data-ttu-id="da0df-134">Int32</span><span class="sxs-lookup"><span data-stu-id="da0df-134">Int32</span></span>|<span data-ttu-id="da0df-135">Número de usuarios que tienen 1 o más dispositivos que no han podido instalar este libro.</span><span class="sxs-lookup"><span data-stu-id="da0df-135">Number of Users that have 1 or more device that failed to install this book.</span></span>|
|<span data-ttu-id="da0df-136">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="da0df-136">notInstalledUserCount</span></span>|<span data-ttu-id="da0df-137">Int32</span><span class="sxs-lookup"><span data-stu-id="da0df-137">Int32</span></span>|<span data-ttu-id="da0df-138">Número de usuarios que no han instalado este libro.</span><span class="sxs-lookup"><span data-stu-id="da0df-138">Number of Users that did not install this book.</span></span>|

## <a name="relationships"></a><span data-ttu-id="da0df-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="da0df-139">Relationships</span></span>
<span data-ttu-id="da0df-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="da0df-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="da0df-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="da0df-141">JSON Representation</span></span>
<span data-ttu-id="da0df-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="da0df-142">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.eBookInstallSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.eBookInstallSummary",
  "id": "String (identifier)",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notInstalledDeviceCount": 1024,
  "installedUserCount": 1024,
  "failedUserCount": 1024,
  "notInstalledUserCount": 1024
}
```








