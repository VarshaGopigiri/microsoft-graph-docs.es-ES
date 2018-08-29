# <a name="domaindnsmxrecord-resource-type"></a><span data-ttu-id="ec7c6-101">Tipo de recurso domainDnsMxRecord</span><span class="sxs-lookup"><span data-stu-id="ec7c6-101">domainDnsMxRecord resource type</span></span>

<span data-ttu-id="ec7c6-p101">Representa un registro MX agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="ec7c6-p101">Represents a MX record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="ec7c6-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="ec7c6-104">Methods</span></span>
<span data-ttu-id="ec7c6-p102">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="ec7c6-p102">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="ec7c6-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec7c6-107">Properties</span></span>
| <span data-ttu-id="ec7c6-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ec7c6-108">Property</span></span>     | <span data-ttu-id="ec7c6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec7c6-109">Type</span></span>   |<span data-ttu-id="ec7c6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec7c6-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ec7c6-111">id</span><span class="sxs-lookup"><span data-stu-id="ec7c6-111">id</span></span>|<span data-ttu-id="ec7c6-112">String</span><span class="sxs-lookup"><span data-stu-id="ec7c6-112">String</span></span>| <span data-ttu-id="ec7c6-p103">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ec7c6-p103">Unique identifier assigned to this entity. Not nullable, Read-only.</span></span>|
|<span data-ttu-id="ec7c6-115">isOptional</span><span class="sxs-lookup"><span data-stu-id="ec7c6-115">isOptional</span></span>|<span data-ttu-id="ec7c6-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="ec7c6-116">Boolean</span></span>| <span data-ttu-id="ec7c6-117">Si es false, el cliente debe configurar el registro MX en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio.</span><span class="sxs-lookup"><span data-stu-id="ec7c6-117">If false, the MX record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain.</span></span> |
|<span data-ttu-id="ec7c6-118">label</span><span class="sxs-lookup"><span data-stu-id="ec7c6-118">label</span></span>|<span data-ttu-id="ec7c6-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="ec7c6-119">String</span></span>| <span data-ttu-id="ec7c6-120">Valor que se usa al configurar la propiedad *alias/host/name* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="ec7c6-120">Value used when configuring the *alias/host/name* property of the MX record at the DNS host.</span></span> |
|<span data-ttu-id="ec7c6-121">mailExchange</span><span class="sxs-lookup"><span data-stu-id="ec7c6-121">mailExchange</span></span>|<span data-ttu-id="ec7c6-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="ec7c6-122">String</span></span>| <span data-ttu-id="ec7c6-123">Valor que se usa al configurar la propiedad *answer/destination/value* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="ec7c6-123">Value used when configuring the *answer/destination/value* of the MX record at the DNS host.</span></span>|
|<span data-ttu-id="ec7c6-124">preference</span><span class="sxs-lookup"><span data-stu-id="ec7c6-124">preference</span></span>|<span data-ttu-id="ec7c6-125">Int32</span><span class="sxs-lookup"><span data-stu-id="ec7c6-125">Int32</span></span>| <span data-ttu-id="ec7c6-126">Valor que se usa al configurar la propiedad *Preference/Priority* del registro MX en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="ec7c6-126">Value used when configuring the *Preference/Priority* property of the MX record at the DNS host.</span></span> |
|<span data-ttu-id="ec7c6-127">recordType</span><span class="sxs-lookup"><span data-stu-id="ec7c6-127">recordType</span></span>|<span data-ttu-id="ec7c6-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="ec7c6-128">String</span></span>| <span data-ttu-id="ec7c6-p104">Tipo de registro DNS. El valor es siempre *Mx*. Clave</span><span class="sxs-lookup"><span data-stu-id="ec7c6-p104">Type of DNS record. The value is always *Mx*. Key</span></span> |
|<span data-ttu-id="ec7c6-132">supportedService</span><span class="sxs-lookup"><span data-stu-id="ec7c6-132">supportedService</span></span>|<span data-ttu-id="ec7c6-133">String</span><span class="sxs-lookup"><span data-stu-id="ec7c6-133">String</span></span>| <span data-ttu-id="ec7c6-134">Servicio o función de Microsoft Online que tiene una dependencia en el registro MX.</span><span class="sxs-lookup"><span data-stu-id="ec7c6-134">Microsoft Online Service or feature that has a dependency on this MX record.</span></span></br></br><span data-ttu-id="ec7c6-135">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="ec7c6-135">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span> |
|<span data-ttu-id="ec7c6-136">ttl</span><span class="sxs-lookup"><span data-stu-id="ec7c6-136">ttl</span></span>|<span data-ttu-id="ec7c6-137">Int32</span><span class="sxs-lookup"><span data-stu-id="ec7c6-137">Int32</span></span>| <span data-ttu-id="ec7c6-p105">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro MX en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="ec7c6-p105">Value to use when configuring the *time-to-live (ttl)* property of the MX record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="ec7c6-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ec7c6-140">Relationships</span></span>
<span data-ttu-id="ec7c6-141">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ec7c6-141">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="ec7c6-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ec7c6-142">JSON representation</span></span>
<span data-ttu-id="ec7c6-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ec7c6-143">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsMxRecord"
}-->

```json
{
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "mailExchange": "String",
  "preference": 1024,
  "recordType": "String",
  "supportedService": "String",
  "ttl": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsMxRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->