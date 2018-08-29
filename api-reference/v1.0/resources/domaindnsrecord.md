# <a name="domaindnsrecord-resource-type"></a><span data-ttu-id="ea7fa-101">Tipo de recurso domainDnsRecord</span><span class="sxs-lookup"><span data-stu-id="ea7fa-101">domainDnsRecord resource type</span></span>

<span data-ttu-id="ea7fa-p101">En cada dominio del inquilino es posible que deba agregar registros DNS al archivo de zona DNS del dominio antes de que Microsoft Online Services pueda usar el dominio. La entidad **DomainDnsRecord** se usa para presentar dichos registros DNS. Entidad base de las entidades [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) y [DomainDnsSrvRecord](domaindnssrvrecord.md).</span><span class="sxs-lookup"><span data-stu-id="ea7fa-p101">For each domain in the tenant, you may be required to add DNS record(s) to the DNS zone file of the domain before the domain can be used by Microsoft Online Services. The **DomainDnsRecord** entity is used to present such DNS records. Base entity for [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) and [DomainDnsSrvRecord](domaindnssrvrecord.md) entities.</span></span>

## <a name="methods"></a><span data-ttu-id="ea7fa-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="ea7fa-105">Methods</span></span>
<span data-ttu-id="ea7fa-p102">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="ea7fa-p102">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="ea7fa-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea7fa-108">Properties</span></span>
| <span data-ttu-id="ea7fa-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea7fa-109">Property</span></span>     | <span data-ttu-id="ea7fa-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea7fa-110">Type</span></span>   |<span data-ttu-id="ea7fa-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea7fa-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ea7fa-112">id</span><span class="sxs-lookup"><span data-stu-id="ea7fa-112">id</span></span>|<span data-ttu-id="ea7fa-113">String</span><span class="sxs-lookup"><span data-stu-id="ea7fa-113">String</span></span>| <span data-ttu-id="ea7fa-p103">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ea7fa-p103">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="ea7fa-116">isOptional</span><span class="sxs-lookup"><span data-stu-id="ea7fa-116">isOptional</span></span>|<span data-ttu-id="ea7fa-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="ea7fa-117">Boolean</span></span>| <span data-ttu-id="ea7fa-118">Si es false, el cliente debe configurar este registro en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="ea7fa-118">If false, this record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="ea7fa-119">label</span><span class="sxs-lookup"><span data-stu-id="ea7fa-119">label</span></span>|<span data-ttu-id="ea7fa-120">String</span><span class="sxs-lookup"><span data-stu-id="ea7fa-120">String</span></span>| <span data-ttu-id="ea7fa-121">Valor que se usa al configurar el nombre del registro DNS en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="ea7fa-121">Value used when configuring the name of the DNS record at the DNS host.</span></span> |
|<span data-ttu-id="ea7fa-122">recordType</span><span class="sxs-lookup"><span data-stu-id="ea7fa-122">recordType</span></span>|<span data-ttu-id="ea7fa-123">String</span><span class="sxs-lookup"><span data-stu-id="ea7fa-123">String</span></span>| <span data-ttu-id="ea7fa-124">Indica qué tipo de registro DNS representa esta entidad.</span><span class="sxs-lookup"><span data-stu-id="ea7fa-124">Indicates what type of DNS record this entity represents.</span></span></br></br><span data-ttu-id="ea7fa-125">El valor puede ser uno de los siguientes: *CName*, *Mx*, *Srv*, *Txt*</span><span class="sxs-lookup"><span data-stu-id="ea7fa-125">The value can be one of the following: *CName*, *Mx*, *Srv*, *Txt*</span></span></br></br><span data-ttu-id="ea7fa-126">Clave</span><span class="sxs-lookup"><span data-stu-id="ea7fa-126">Key</span></span> |
|<span data-ttu-id="ea7fa-127">supportedService</span><span class="sxs-lookup"><span data-stu-id="ea7fa-127">supportedService</span></span>|<span data-ttu-id="ea7fa-128">String</span><span class="sxs-lookup"><span data-stu-id="ea7fa-128">String</span></span>| <span data-ttu-id="ea7fa-129">Servicio o función de Microsoft Online que tiene una dependencia en el registro DNS.</span><span class="sxs-lookup"><span data-stu-id="ea7fa-129">Microsoft Online Service or feature that has a dependency on this DNS record.</span></span></br></br><span data-ttu-id="ea7fa-130">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="ea7fa-130">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span>|
|<span data-ttu-id="ea7fa-131">ttl</span><span class="sxs-lookup"><span data-stu-id="ea7fa-131">ttl</span></span>|<span data-ttu-id="ea7fa-132">Int32</span><span class="sxs-lookup"><span data-stu-id="ea7fa-132">Int32</span></span>| <span data-ttu-id="ea7fa-p104">Valor que se debe usar al configurar la propiedad de período de vida (ttl) del registro DNS en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="ea7fa-p104">Value to use when configuring the time-to-live (ttl) property of the DNS record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="ea7fa-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ea7fa-135">Relationships</span></span>
<span data-ttu-id="ea7fa-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ea7fa-136">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="ea7fa-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ea7fa-137">JSON representation</span></span>
<span data-ttu-id="ea7fa-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ea7fa-138">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsRecord"
}-->

```json
{
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "recordType": "String",
  "supportedService": "String",
  "ttl": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->