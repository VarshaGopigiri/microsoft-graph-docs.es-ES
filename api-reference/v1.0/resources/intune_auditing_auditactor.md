# <a name="auditactor-resource-type"></a><span data-ttu-id="afec9-101">Tipo de recurso auditActor</span><span class="sxs-lookup"><span data-stu-id="afec9-101">auditActor resource type</span></span>

> <span data-ttu-id="afec9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="afec9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="afec9-103">Una clase que contiene las propiedades del actor de auditoría.</span><span class="sxs-lookup"><span data-stu-id="afec9-103">A class containing the properties for Audit Actor.</span></span>
## <a name="properties"></a><span data-ttu-id="afec9-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="afec9-104">Properties</span></span>
|<span data-ttu-id="afec9-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="afec9-105">Property</span></span>|<span data-ttu-id="afec9-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="afec9-106">Type</span></span>|<span data-ttu-id="afec9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="afec9-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="afec9-108">type</span><span class="sxs-lookup"><span data-stu-id="afec9-108">type</span></span>|<span data-ttu-id="afec9-109">cadena</span><span class="sxs-lookup"><span data-stu-id="afec9-109">String</span></span>|<span data-ttu-id="afec9-110">Tipo de actor.</span><span class="sxs-lookup"><span data-stu-id="afec9-110">Actor Type.</span></span>|
|<span data-ttu-id="afec9-111">permisos</span><span class="sxs-lookup"><span data-stu-id="afec9-111">permissions</span></span>|<span data-ttu-id="afec9-112">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="afec9-112">String collection</span></span>|<span data-ttu-id="afec9-113">Lista de los permisos de usuario cuando se ha realizado la auditoría.</span><span class="sxs-lookup"><span data-stu-id="afec9-113">List of user permissions when the audit was performed.</span></span>|
|<span data-ttu-id="afec9-114">userPermissions</span><span class="sxs-lookup"><span data-stu-id="afec9-114">userPermissions</span></span>|<span data-ttu-id="afec9-115">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="afec9-115">String collection</span></span>|<span data-ttu-id="afec9-116">Lista de los permisos de usuario cuando se ha realizado la auditoría.</span><span class="sxs-lookup"><span data-stu-id="afec9-116">List of user permissions when the audit was performed.</span></span>|
|<span data-ttu-id="afec9-117">applicationId</span><span class="sxs-lookup"><span data-stu-id="afec9-117">applicationId</span></span>|<span data-ttu-id="afec9-118">cadena</span><span class="sxs-lookup"><span data-stu-id="afec9-118">String</span></span>|<span data-ttu-id="afec9-119">Id. de aplicación de AAD</span><span class="sxs-lookup"><span data-stu-id="afec9-119">AAD Application Id.</span></span>|
|<span data-ttu-id="afec9-120">applicationDisplayName</span><span class="sxs-lookup"><span data-stu-id="afec9-120">applicationDisplayName</span></span>|<span data-ttu-id="afec9-121">cadena</span><span class="sxs-lookup"><span data-stu-id="afec9-121">String</span></span>|<span data-ttu-id="afec9-122">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="afec9-122">Name of the Application.</span></span>|
|<span data-ttu-id="afec9-123">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="afec9-123">userPrincipalName</span></span>|<span data-ttu-id="afec9-124">cadena</span><span class="sxs-lookup"><span data-stu-id="afec9-124">String</span></span>|<span data-ttu-id="afec9-125">Nombre principal de usuario (UPN).</span><span class="sxs-lookup"><span data-stu-id="afec9-125">User principal name (UPN)</span></span>|
|<span data-ttu-id="afec9-126">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="afec9-126">servicePrincipalName</span></span>|<span data-ttu-id="afec9-127">cadena</span><span class="sxs-lookup"><span data-stu-id="afec9-127">String</span></span>|<span data-ttu-id="afec9-128">Nombre de entidad de seguridad de servicio (SPN).</span><span class="sxs-lookup"><span data-stu-id="afec9-128">Service Principal Name (SPN).</span></span>|
|<span data-ttu-id="afec9-129">ipAddress</span><span class="sxs-lookup"><span data-stu-id="afec9-129">ipAddress</span></span>|<span data-ttu-id="afec9-130">cadena</span><span class="sxs-lookup"><span data-stu-id="afec9-130">String</span></span>|<span data-ttu-id="afec9-131">IPAddress.</span><span class="sxs-lookup"><span data-stu-id="afec9-131">IPAddress.</span></span>|
|<span data-ttu-id="afec9-132">userId</span><span class="sxs-lookup"><span data-stu-id="afec9-132">userID</span></span>|<span data-ttu-id="afec9-133">cadena</span><span class="sxs-lookup"><span data-stu-id="afec9-133">String</span></span>|<span data-ttu-id="afec9-134">Id. de usuario.</span><span class="sxs-lookup"><span data-stu-id="afec9-134">User ID</span></span>|

## <a name="relationships"></a><span data-ttu-id="afec9-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="afec9-135">Relationships</span></span>
<span data-ttu-id="afec9-136">Ninguna</span><span class="sxs-lookup"><span data-stu-id="afec9-136">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="afec9-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="afec9-137">JSON Representation</span></span>
<span data-ttu-id="afec9-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="afec9-138">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.auditActor"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditActor",
  "type": "String",
  "permissions": [
    "String"
  ],
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



