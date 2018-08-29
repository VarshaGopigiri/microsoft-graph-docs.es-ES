# <a name="fileencryptioninfo-resource-type"></a><span data-ttu-id="ff7c2-101">Tipo de recurso fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="ff7c2-101">fileEncryptionInfo resource type</span></span>

> <span data-ttu-id="ff7c2-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ff7c2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ff7c2-103">Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.</span><span class="sxs-lookup"><span data-stu-id="ff7c2-103">Contains properties for file encryption information for the content version of a line of business app.</span></span>
## <a name="properties"></a><span data-ttu-id="ff7c2-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff7c2-104">Properties</span></span>
|<span data-ttu-id="ff7c2-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff7c2-105">Property</span></span>|<span data-ttu-id="ff7c2-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff7c2-106">Type</span></span>|<span data-ttu-id="ff7c2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff7c2-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ff7c2-108">encryptionKey</span><span class="sxs-lookup"><span data-stu-id="ff7c2-108">encryptionKey</span></span>|<span data-ttu-id="ff7c2-109">Binario</span><span class="sxs-lookup"><span data-stu-id="ff7c2-109">Binary</span></span>|<span data-ttu-id="ff7c2-110">La clave que se usa para cifrar el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="ff7c2-110">The key used to encrypt the file content.</span></span>|
|<span data-ttu-id="ff7c2-111">initializationVector</span><span class="sxs-lookup"><span data-stu-id="ff7c2-111">initializationVector</span></span>|<span data-ttu-id="ff7c2-112">Binario</span><span class="sxs-lookup"><span data-stu-id="ff7c2-112">Binary</span></span>|<span data-ttu-id="ff7c2-113">El vector de inicialización utilizado para el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="ff7c2-113">The initialization vector used for the encryption algorithm.</span></span>|
|<span data-ttu-id="ff7c2-114">mac</span><span class="sxs-lookup"><span data-stu-id="ff7c2-114">mac</span></span>|<span data-ttu-id="ff7c2-115">Binario</span><span class="sxs-lookup"><span data-stu-id="ff7c2-115">Binary</span></span>|<span data-ttu-id="ff7c2-116">El hash del contenido del archivo cifrado + IV (hash de contenido).</span><span class="sxs-lookup"><span data-stu-id="ff7c2-116">The hash of the encrypted file content + IV (content hash).</span></span>|
|<span data-ttu-id="ff7c2-117">macKey</span><span class="sxs-lookup"><span data-stu-id="ff7c2-117">macKey</span></span>|<span data-ttu-id="ff7c2-118">Binario</span><span class="sxs-lookup"><span data-stu-id="ff7c2-118">Binary</span></span>|<span data-ttu-id="ff7c2-119">La clave utilizada para obtener el MAC.</span><span class="sxs-lookup"><span data-stu-id="ff7c2-119">The key used to get mac.</span></span>|
|<span data-ttu-id="ff7c2-120">profileIdentifier</span><span class="sxs-lookup"><span data-stu-id="ff7c2-120">profileIdentifier</span></span>|<span data-ttu-id="ff7c2-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="ff7c2-121">String</span></span>|<span data-ttu-id="ff7c2-122">El identificador del perfil.</span><span class="sxs-lookup"><span data-stu-id="ff7c2-122">The the profile identifier.</span></span>|
|<span data-ttu-id="ff7c2-123">fileDigest</span><span class="sxs-lookup"><span data-stu-id="ff7c2-123">fileDigest</span></span>|<span data-ttu-id="ff7c2-124">Binario</span><span class="sxs-lookup"><span data-stu-id="ff7c2-124">Binary</span></span>|<span data-ttu-id="ff7c2-125">El resumen de los archivos antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="ff7c2-125">The file digest prior to encryption.</span></span>|
|<span data-ttu-id="ff7c2-126">fileDigestAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ff7c2-126">fileDigestAlgorithm</span></span>|<span data-ttu-id="ff7c2-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="ff7c2-127">String</span></span>|<span data-ttu-id="ff7c2-128">El algoritmo del resumen de los archivos.</span><span class="sxs-lookup"><span data-stu-id="ff7c2-128">The file digest algorithm.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ff7c2-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ff7c2-129">Relationships</span></span>
<span data-ttu-id="ff7c2-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ff7c2-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ff7c2-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ff7c2-131">JSON Representation</span></span>
<span data-ttu-id="ff7c2-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ff7c2-132">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.fileEncryptionInfo"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.fileEncryptionInfo",
  "encryptionKey": "binary",
  "initializationVector": "binary",
  "mac": "binary",
  "macKey": "binary",
  "profileIdentifier": "String",
  "fileDigest": "binary",
  "fileDigestAlgorithm": "String"
}
```



