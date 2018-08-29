# <a name="domaindnscnamerecord-resource-type"></a><span data-ttu-id="c4147-101">Tipo de recurso domainDnsCnameRecord</span><span class="sxs-lookup"><span data-stu-id="c4147-101">domainDnsCnameRecord resource type</span></span>

<span data-ttu-id="c4147-p101">Representa un registro CNAME agregado al archivo de zona DNS de un dominio determinado en el inquilino. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="c4147-p101">Represents a CNAME record added to the DNS zone file of a particular domain in the tenant. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>


## <a name="methods"></a><span data-ttu-id="c4147-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="c4147-104">Methods</span></span>
<span data-ttu-id="c4147-p102">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="c4147-p102">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="c4147-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c4147-107">Properties</span></span>
| <span data-ttu-id="c4147-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c4147-108">Property</span></span>     | <span data-ttu-id="c4147-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4147-109">Type</span></span>   |<span data-ttu-id="c4147-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4147-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c4147-111">canonicalName</span><span class="sxs-lookup"><span data-stu-id="c4147-111">canonicalName</span></span>|<span data-ttu-id="c4147-112">String</span><span class="sxs-lookup"><span data-stu-id="c4147-112">String</span></span>| <span data-ttu-id="c4147-p103">Nombre canónico del registro CNAME. Se usa para configurar el registro CNAME en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="c4147-p103">The canonical name of the CNAME record. Used to configure the CNAME record at the DNS host.</span></span> |
|<span data-ttu-id="c4147-115">id</span><span class="sxs-lookup"><span data-stu-id="c4147-115">id</span></span>|<span data-ttu-id="c4147-116">String</span><span class="sxs-lookup"><span data-stu-id="c4147-116">String</span></span>| <span data-ttu-id="c4147-p104">Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c4147-p104">Unique identifier assigned to this entity. Not nullable, Read-only</span></span>|
|<span data-ttu-id="c4147-119">isOptional</span><span class="sxs-lookup"><span data-stu-id="c4147-119">isOptional</span></span>|<span data-ttu-id="c4147-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="c4147-120">Boolean</span></span>| <span data-ttu-id="c4147-p105">Si es false, el cliente debe configurar el registro CNAME en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="c4147-p105">If false, the CNAME record must be configured by the customer at the DNS host for Microsoft Online Services to operate correctly with the domain. Not nullable</span></span> |
|<span data-ttu-id="c4147-123">label</span><span class="sxs-lookup"><span data-stu-id="c4147-123">label</span></span>|<span data-ttu-id="c4147-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="c4147-124">String</span></span>| <span data-ttu-id="c4147-125">Valor que se usa al configurar el *alias/host/name* del registro CNAME en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="c4147-125">Value used when configuring the *alias/host/name* of the CNAME record at the DNS host.</span></span> |
|<span data-ttu-id="c4147-126">recordType</span><span class="sxs-lookup"><span data-stu-id="c4147-126">recordType</span></span>|<span data-ttu-id="c4147-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="c4147-127">String</span></span>| <span data-ttu-id="c4147-p106">Tipo de registro DNS. El valor es siempre *CName*. Clave</span><span class="sxs-lookup"><span data-stu-id="c4147-p106">Type of DNS record. The value is always *CName*. Key</span></span>|
|<span data-ttu-id="c4147-131">supportedService</span><span class="sxs-lookup"><span data-stu-id="c4147-131">supportedService</span></span>|<span data-ttu-id="c4147-132">String</span><span class="sxs-lookup"><span data-stu-id="c4147-132">String</span></span>| <span data-ttu-id="c4147-133">Servicio o función de Microsoft Online que tiene una dependencia en el registro CNAME.</span><span class="sxs-lookup"><span data-stu-id="c4147-133">Microsoft Online Service or feature that has a dependency on this CNAME record.</span></span></br></br><span data-ttu-id="c4147-134">Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*</span><span class="sxs-lookup"><span data-stu-id="c4147-134">Can be one of the following values: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*</span></span>|
|<span data-ttu-id="c4147-135">ttl</span><span class="sxs-lookup"><span data-stu-id="c4147-135">ttl</span></span>|<span data-ttu-id="c4147-136">Int32</span><span class="sxs-lookup"><span data-stu-id="c4147-136">Int32</span></span>| <span data-ttu-id="c4147-p107">Valor que se debe usar al configurar la propiedad de período de vida (ttl) del registro CNAME en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="c4147-p107">Value to use when configuring the time-to-live (ttl) property of the CNAME record at the DNS host. Not nullable</span></span> |

## <a name="relationships"></a><span data-ttu-id="c4147-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c4147-139">Relationships</span></span>
<span data-ttu-id="c4147-140">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c4147-140">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="c4147-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c4147-141">JSON representation</span></span>
<span data-ttu-id="c4147-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c4147-142">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsCnameRecord"
}-->

```json
{
  "canonicalName": "String",
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
  "description": "domainDnsCnameRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->