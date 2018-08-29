# <a name="domaindnsunavailablerecord-resource-type"></a><span data-ttu-id="d1954-101">Tipo de recurso domainDnsUnavailableRecord</span><span class="sxs-lookup"><span data-stu-id="d1954-101">domainDnsUnavailableRecord resource type</span></span>

<span data-ttu-id="d1954-p101">Al consultar la propiedad de navegación **serviceConfigurationRecords** para una entidad [Domain](domain.md), es posible que reciba una o varias entidades [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) o [DomainDnsTxtRecord](domaindnstxtrecord.md). Estas entidades indican qué registros DNS debe agregar al archivo de zona del dominio antes de que Microsoft Online Services pueda usar el dominio. Si no se pueden generar dichas entidades, se devuelve una entidad DomainDnsUnavailableRecord. Heredado de la entidad [DomainDnsRecord](domaindnsrecord.md).</span><span class="sxs-lookup"><span data-stu-id="d1954-p101">When you query for the navigation property **serviceConfigurationRecords** for a [Domain](domain.md) entity, you may get back one or more [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md), and/or [DomainDnsTxtRecord](domaindnstxtrecord.md) entities. These entities indicate what DNS records you must add to the zone file of the domain, before the domain can be used by Microsoft Online Services. When it is not possible to generate such entities, a DomainDnsUnavailableRecord Entity is returned instead. Inherited from [DomainDnsRecord](domaindnsrecord.md) entity.</span></span>

## <a name="methods"></a><span data-ttu-id="d1954-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1954-106">Methods</span></span>
<span data-ttu-id="d1954-p102">No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.</span><span class="sxs-lookup"><span data-stu-id="d1954-p102">Direct queries to this resource are not supported. Please see the [domain](domain.md) topic for information on how to query for domain service records.</span></span>

## <a name="properties"></a><span data-ttu-id="d1954-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1954-109">Properties</span></span>
| <span data-ttu-id="d1954-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1954-110">Property</span></span>     | <span data-ttu-id="d1954-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1954-111">Type</span></span>   |<span data-ttu-id="d1954-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1954-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d1954-113">description</span><span class="sxs-lookup"><span data-stu-id="d1954-113">description</span></span>|<span data-ttu-id="d1954-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1954-114">String</span></span>|<span data-ttu-id="d1954-115">Proporciona el motivo por el que se devuelve la entidad **DomainDnsUnavailableRecord**.</span><span class="sxs-lookup"><span data-stu-id="d1954-115">Provides the reason why the **DomainDnsUnavailableRecord** entity is returned.</span></span> |

## <a name="relationships"></a><span data-ttu-id="d1954-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d1954-116">Relationships</span></span>
<span data-ttu-id="d1954-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d1954-117">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="d1954-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d1954-118">JSON representation</span></span>
<span data-ttu-id="d1954-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d1954-119">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.domainDnsRecord",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsUnavailableRecord"
}-->

```json
{
  "description": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsUnavailableRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->