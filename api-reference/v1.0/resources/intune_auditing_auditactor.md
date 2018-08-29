# <a name="auditactor-resource-type"></a><span data-ttu-id="fe419-101">Tipo de recurso auditActor</span><span class="sxs-lookup"><span data-stu-id="fe419-101">auditActor resource type</span></span>

> <span data-ttu-id="fe419-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fe419-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fe419-103">Una clase que contiene las propiedades del actor de auditoría.</span><span class="sxs-lookup"><span data-stu-id="fe419-103">A class containing the properties for Audit Actor.</span></span>
## <a name="properties"></a><span data-ttu-id="fe419-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe419-104">Properties</span></span>
|<span data-ttu-id="fe419-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fe419-105">Property</span></span>|<span data-ttu-id="fe419-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe419-106">Type</span></span>|<span data-ttu-id="fe419-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe419-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fe419-108">type</span><span class="sxs-lookup"><span data-stu-id="fe419-108">type</span></span>|<span data-ttu-id="fe419-109">cadena</span><span class="sxs-lookup"><span data-stu-id="fe419-109">String</span></span>|<span data-ttu-id="fe419-110">Tipo de actor.</span><span class="sxs-lookup"><span data-stu-id="fe419-110">Actor Type.</span></span>|
|<span data-ttu-id="fe419-111">userPermissions</span><span class="sxs-lookup"><span data-stu-id="fe419-111">userPermissions</span></span>|<span data-ttu-id="fe419-112">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="fe419-112">String collection</span></span>|<span data-ttu-id="fe419-113">Lista de los permisos de usuario cuando se ha realizado la auditoría.</span><span class="sxs-lookup"><span data-stu-id="fe419-113">List of user permissions when the audit was performed.</span></span>|
|<span data-ttu-id="fe419-114">applicationId</span><span class="sxs-lookup"><span data-stu-id="fe419-114">applicationId</span></span>|<span data-ttu-id="fe419-115">cadena</span><span class="sxs-lookup"><span data-stu-id="fe419-115">String</span></span>|<span data-ttu-id="fe419-116">Id. de aplicación de AAD</span><span class="sxs-lookup"><span data-stu-id="fe419-116">AAD Application Id.</span></span>|
|<span data-ttu-id="fe419-117">applicationDisplayName</span><span class="sxs-lookup"><span data-stu-id="fe419-117">applicationDisplayName</span></span>|<span data-ttu-id="fe419-118">cadena</span><span class="sxs-lookup"><span data-stu-id="fe419-118">String</span></span>|<span data-ttu-id="fe419-119">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fe419-119">Name of the Application.</span></span>|
|<span data-ttu-id="fe419-120">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fe419-120">userPrincipalName</span></span>|<span data-ttu-id="fe419-121">cadena</span><span class="sxs-lookup"><span data-stu-id="fe419-121">String</span></span>|<span data-ttu-id="fe419-122">Nombre principal de usuario (UPN).</span><span class="sxs-lookup"><span data-stu-id="fe419-122">User Principal Name (UPN).</span></span>|
|<span data-ttu-id="fe419-123">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fe419-123">servicePrincipalName</span></span>|<span data-ttu-id="fe419-124">cadena</span><span class="sxs-lookup"><span data-stu-id="fe419-124">String</span></span>|<span data-ttu-id="fe419-125">Nombre de entidad de seguridad de servicio (SPN).</span><span class="sxs-lookup"><span data-stu-id="fe419-125">Service Principal Name (SPN).</span></span>|
|<span data-ttu-id="fe419-126">ipAddress</span><span class="sxs-lookup"><span data-stu-id="fe419-126">ipAddress</span></span>|<span data-ttu-id="fe419-127">cadena</span><span class="sxs-lookup"><span data-stu-id="fe419-127">String</span></span>|<span data-ttu-id="fe419-128">IPAddress.</span><span class="sxs-lookup"><span data-stu-id="fe419-128">IPAddress.</span></span>|
|<span data-ttu-id="fe419-129">userId</span><span class="sxs-lookup"><span data-stu-id="fe419-129">userId</span></span>|<span data-ttu-id="fe419-130">cadena</span><span class="sxs-lookup"><span data-stu-id="fe419-130">String</span></span>|<span data-ttu-id="fe419-131">Id. de usuario.</span><span class="sxs-lookup"><span data-stu-id="fe419-131">User Id.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fe419-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fe419-132">Relationships</span></span>
<span data-ttu-id="fe419-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fe419-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fe419-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fe419-134">JSON Representation</span></span>
<span data-ttu-id="fe419-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fe419-135">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.auditActor"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.auditActor",
  "type": "String",
  "userPermissions": [
    "String"
  ],
  "applicationId": "String",
  "applicationDisplayName": "String",
  "userPrincipalName": "String",
  "servicePrincipalName": "String",
  "ipAddress": "String",
  "userId": "String"
}
```



