# <a name="domaindnssrvrecord-resource-type"></a><span data-ttu-id="f25f5-101">Tipo de recurso domainDnsSrvRecord</span><span class="sxs-lookup"><span data-stu-id="f25f5-101">domainDnsSrvRecord resource type</span></span>

<span data-ttu-id="f25f5-p101">Representa un registro SRV agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="f25f5-p101">Represents a SRV record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="f25f5-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="f25f5-104">Methods</span></span>
<span data-ttu-id="f25f5-p102">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="f25f5-p102">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="f25f5-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f25f5-107">Properties</span></span>
| <span data-ttu-id="f25f5-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f25f5-108">Property</span></span>     | <span data-ttu-id="f25f5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f25f5-109">Type</span></span>   |<span data-ttu-id="f25f5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f25f5-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f25f5-111">id</span><span class="sxs-lookup"><span data-stu-id="f25f5-111">id</span></span>|<span data-ttu-id="f25f5-112">String</span><span class="sxs-lookup"><span data-stu-id="f25f5-112">String</span></span>| <span data-ttu-id="f25f5-p103">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f25f5-p103">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="f25f5-115">isOptional</span><span class="sxs-lookup"><span data-stu-id="f25f5-115">isOptional</span></span>|<span data-ttu-id="f25f5-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="f25f5-116">Boolean</span></span>| <span data-ttu-id="f25f5-117">Si es false, el cliente debe configurar el registro SRV en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="f25f5-117">If false, the SRV record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="f25f5-118">label</span><span class="sxs-lookup"><span data-stu-id="f25f5-118">label</span></span>|<span data-ttu-id="f25f5-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="f25f5-119">String</span></span>| <span data-ttu-id="f25f5-120">Valor que se usa al configurar la propiedad *name* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="f25f5-120">Value used when configuring the *name* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="f25f5-121">nameTarget</span><span class="sxs-lookup"><span data-stu-id="f25f5-121">nameTarget</span></span>|<span data-ttu-id="f25f5-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="f25f5-122">String</span></span>| <span data-ttu-id="f25f5-123">Valor que se debe usar al configurar la propiedad *Target* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="f25f5-123">Value to use when configuring the *Target* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="f25f5-124">port</span><span class="sxs-lookup"><span data-stu-id="f25f5-124">port</span></span>|<span data-ttu-id="f25f5-125">Int32</span><span class="sxs-lookup"><span data-stu-id="f25f5-125">Int32</span></span>| <span data-ttu-id="f25f5-126">Valor que se debe usar al configurar la propiedad *port* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="f25f5-126">Value to use when configuring the *port* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="f25f5-127">priority</span><span class="sxs-lookup"><span data-stu-id="f25f5-127">priority</span></span>|<span data-ttu-id="f25f5-128">Int32</span><span class="sxs-lookup"><span data-stu-id="f25f5-128">Int32</span></span>| <span data-ttu-id="f25f5-129">Valor que se debe usar al configurar la propiedad *priority* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="f25f5-129">Value to use when configuring the *priority* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="f25f5-130">protocol</span><span class="sxs-lookup"><span data-stu-id="f25f5-130">protocol</span></span>|<span data-ttu-id="f25f5-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="f25f5-131">String</span></span>| <span data-ttu-id="f25f5-132">Valor que se debe usar al configurar la propiedad *protocol* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="f25f5-132">Value to use when configuring the *protocol* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="f25f5-133">recordType</span><span class="sxs-lookup"><span data-stu-id="f25f5-133">recordType</span></span>|<span data-ttu-id="f25f5-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="f25f5-134">String</span></span>|  <span data-ttu-id="f25f5-p104">Tipo de registro DNS. El valor es siempre *Srv*. Clave</span><span class="sxs-lookup"><span data-stu-id="f25f5-p104">Type of DNS record. The value is always *Srv*. Key</span></span> |
|<span data-ttu-id="f25f5-138">service</span><span class="sxs-lookup"><span data-stu-id="f25f5-138">service</span></span>|<span data-ttu-id="f25f5-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="f25f5-139">String</span></span>| <span data-ttu-id="f25f5-140">Valor que se debe usar al configurar la propiedad *service* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="f25f5-140">Value to use when configuring the *service* property of the SRV record at the DNS host.</span></span> |
|<span data-ttu-id="f25f5-141">supportedService</span><span class="sxs-lookup"><span data-stu-id="f25f5-141">supportedService</span></span>|<span data-ttu-id="f25f5-142">String</span><span class="sxs-lookup"><span data-stu-id="f25f5-142">String</span></span>| <span data-ttu-id="f25f5-143">Servicio o función de Microsoft Online que tiene una dependencia en el registro SRV.</span><span class="sxs-lookup"><span data-stu-id="f25f5-143">Microsoft Online Service or feature that has a dependency on this SRV record.</span></span></br></br><span data-ttu-id="f25f5-144">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="f25f5-144">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span> |
|<span data-ttu-id="f25f5-145">ttl</span><span class="sxs-lookup"><span data-stu-id="f25f5-145">ttl</span></span>|<span data-ttu-id="f25f5-146">Int32</span><span class="sxs-lookup"><span data-stu-id="f25f5-146">Int32</span></span>| <span data-ttu-id="f25f5-p105">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro SRV en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="f25f5-p105">Value to use when configuring the *time-to-live (ttl)* property of the SRV record at the DNS host. Not nullable</span></span> |
|<span data-ttu-id="f25f5-149">weight</span><span class="sxs-lookup"><span data-stu-id="f25f5-149">weight</span></span>|<span data-ttu-id="f25f5-150">Int32</span><span class="sxs-lookup"><span data-stu-id="f25f5-150">Int32</span></span>| <span data-ttu-id="f25f5-151">Valor que se debe usar al configurar la propiedad *weight* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="f25f5-151">Value to use when configuring the *weight* property of the SRV record at the DNS host.</span></span> |

## <a name="relationships"></a><span data-ttu-id="f25f5-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f25f5-152">Relationships</span></span>
<span data-ttu-id="f25f5-153">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f25f5-153">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="f25f5-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f25f5-154">JSON representation</span></span>
<span data-ttu-id="f25f5-155">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f25f5-155">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsSrvRecord"
}-->

```json
{
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "nameTarget": "String",
  "port": 1024,
  "priority": 1024,
  "protocol": "String",
  "recordType": "String",
  "service": "String",
  "supportedService": "String",
  "ttl": 1024,
  "weight": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsSrvRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->