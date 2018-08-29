# <a name="windowsinformationprotectiondatarecoverycertificate-resource-type"></a><span data-ttu-id="3777d-101">Tipo de recurso windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="3777d-101">windowsInformationProtectionDataRecoveryCertificate resource type</span></span>

> <span data-ttu-id="3777d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3777d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3777d-103">Certificado de recuperación de datos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="3777d-103">Windows Information Protection DataRecoveryCertificate</span></span>
## <a name="properties"></a><span data-ttu-id="3777d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3777d-104">Properties</span></span>
|<span data-ttu-id="3777d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3777d-105">Property</span></span>|<span data-ttu-id="3777d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="3777d-106">Type</span></span>|<span data-ttu-id="3777d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3777d-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3777d-108">subjectName</span><span class="sxs-lookup"><span data-stu-id="3777d-108">subjectName</span></span>|<span data-ttu-id="3777d-109">cadena</span><span class="sxs-lookup"><span data-stu-id="3777d-109">String</span></span>|<span data-ttu-id="3777d-110">Nombre de asunto del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="3777d-110">Data recovery Certificate subject name</span></span>|
|<span data-ttu-id="3777d-111">descripción</span><span class="sxs-lookup"><span data-stu-id="3777d-111">description</span></span>|<span data-ttu-id="3777d-112">cadena</span><span class="sxs-lookup"><span data-stu-id="3777d-112">String</span></span>|<span data-ttu-id="3777d-113">Descripción del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="3777d-113">Data recovery Certificate description</span></span>|
|<span data-ttu-id="3777d-114">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="3777d-114">expirationDateTime</span></span>|<span data-ttu-id="3777d-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3777d-115">DateTimeOffset</span></span>|<span data-ttu-id="3777d-116">Fecha y hora de expiración del certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="3777d-116">Data recovery Certificate expiration datetime</span></span>|
|<span data-ttu-id="3777d-117">certificado</span><span class="sxs-lookup"><span data-stu-id="3777d-117">certificate</span></span>|<span data-ttu-id="3777d-118">Binario</span><span class="sxs-lookup"><span data-stu-id="3777d-118">Binary</span></span>|<span data-ttu-id="3777d-119">Certificado para la recuperación de datos</span><span class="sxs-lookup"><span data-stu-id="3777d-119">Data recovery Certificate</span></span>|

## <a name="relationships"></a><span data-ttu-id="3777d-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3777d-120">Relationships</span></span>
<span data-ttu-id="3777d-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3777d-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3777d-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3777d-122">JSON Representation</span></span>
<span data-ttu-id="3777d-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3777d-123">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
  "subjectName": "String",
  "description": "String",
  "expirationDateTime": "String (timestamp)",
  "certificate": "binary"
}
```



