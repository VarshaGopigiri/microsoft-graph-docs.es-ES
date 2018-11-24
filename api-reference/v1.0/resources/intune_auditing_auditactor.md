# <a name="auditactor-resource-type"></a><span data-ttu-id="08381-101">Tipo de recurso auditActor</span><span class="sxs-lookup"><span data-stu-id="08381-101">auditActor resource type</span></span>

> <span data-ttu-id="08381-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="08381-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="08381-103">Una clase que contiene las propiedades del actor de auditoría.</span><span class="sxs-lookup"><span data-stu-id="08381-103">A class containing the properties for Audit Actor.</span></span>
## <a name="properties"></a><span data-ttu-id="08381-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08381-104">Properties</span></span>
|<span data-ttu-id="08381-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="08381-105">Property</span></span>|<span data-ttu-id="08381-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="08381-106">Type</span></span>|<span data-ttu-id="08381-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="08381-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="08381-108">type</span><span class="sxs-lookup"><span data-stu-id="08381-108">type</span></span>|<span data-ttu-id="08381-109">cadena</span><span class="sxs-lookup"><span data-stu-id="08381-109">String</span></span>|<span data-ttu-id="08381-110">Tipo de actor.</span><span class="sxs-lookup"><span data-stu-id="08381-110">Actor Type.</span></span>|
|<span data-ttu-id="08381-111">userPermissions</span><span class="sxs-lookup"><span data-stu-id="08381-111">userPermissions</span></span>|<span data-ttu-id="08381-112">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="08381-112">String collection</span></span>|<span data-ttu-id="08381-113">Lista de los permisos de usuario cuando se ha realizado la auditoría.</span><span class="sxs-lookup"><span data-stu-id="08381-113">List of user permissions when the audit was performed.</span></span>|
|<span data-ttu-id="08381-114">applicationId</span><span class="sxs-lookup"><span data-stu-id="08381-114">applicationId</span></span>|<span data-ttu-id="08381-115">cadena</span><span class="sxs-lookup"><span data-stu-id="08381-115">String</span></span>|<span data-ttu-id="08381-116">Id. de aplicación de AAD</span><span class="sxs-lookup"><span data-stu-id="08381-116">AAD Application Id.</span></span>|
|<span data-ttu-id="08381-117">applicationDisplayName</span><span class="sxs-lookup"><span data-stu-id="08381-117">applicationDisplayName</span></span>|<span data-ttu-id="08381-118">cadena</span><span class="sxs-lookup"><span data-stu-id="08381-118">String</span></span>|<span data-ttu-id="08381-119">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="08381-119">Name of the Application.</span></span>|
|<span data-ttu-id="08381-120">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="08381-120">userPrincipalName</span></span>|<span data-ttu-id="08381-121">cadena</span><span class="sxs-lookup"><span data-stu-id="08381-121">String</span></span>|<span data-ttu-id="08381-122">Nombre principal de usuario (UPN).</span><span class="sxs-lookup"><span data-stu-id="08381-122">User Principal Name (UPN).</span></span>|
|<span data-ttu-id="08381-123">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="08381-123">servicePrincipalName</span></span>|<span data-ttu-id="08381-124">cadena</span><span class="sxs-lookup"><span data-stu-id="08381-124">String</span></span>|<span data-ttu-id="08381-125">Nombre de entidad de seguridad de servicio (SPN).</span><span class="sxs-lookup"><span data-stu-id="08381-125">Service Principal Name (SPN).</span></span>|
|<span data-ttu-id="08381-126">ipAddress</span><span class="sxs-lookup"><span data-stu-id="08381-126">ipAddress</span></span>|<span data-ttu-id="08381-127">cadena</span><span class="sxs-lookup"><span data-stu-id="08381-127">String</span></span>|<span data-ttu-id="08381-128">IPAddress.</span><span class="sxs-lookup"><span data-stu-id="08381-128">IPAddress.</span></span>|
|<span data-ttu-id="08381-129">userId</span><span class="sxs-lookup"><span data-stu-id="08381-129">userId</span></span>|<span data-ttu-id="08381-130">cadena</span><span class="sxs-lookup"><span data-stu-id="08381-130">String</span></span>|<span data-ttu-id="08381-131">Id. de usuario.</span><span class="sxs-lookup"><span data-stu-id="08381-131">User Id.</span></span>|

## <a name="relationships"></a><span data-ttu-id="08381-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="08381-132">Relationships</span></span>
<span data-ttu-id="08381-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="08381-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="08381-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="08381-134">JSON Representation</span></span>
<span data-ttu-id="08381-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="08381-135">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.auditActor"
}
-->
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



