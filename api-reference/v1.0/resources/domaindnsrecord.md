# <a name="domaindnsrecord-resource-type"></a>Tipo de recurso domainDnsRecord

En cada dominio del inquilino es posible que deba agregar registros DNS al archivo de zona DNS del dominio antes de que Microsoft Online Services pueda usar el dominio. La entidad **DomainDnsRecord** se usa para presentar dichos registros DNS. Entidad base de las entidades [DomainDnsCnameRecord](domaindnscnamerecord.md), [DomainDnsMxRecord](domaindnsmxrecord.md), [DomainDnsSrvRecord](domaindnssrvrecord.md) y [DomainDnsSrvRecord](domaindnssrvrecord.md).

## <a name="methods"></a>Métodos
No se admiten las consultas directas a este recurso. Consulte el tema [domain](domain.md) para obtener información sobre cómo efectuar consultas para los registros de servicios de dominio.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|String| Identificador único asignado a esta entidad. No admite valores NULL, solo lectura.|
|isOptional|Booleano| Si es false, el cliente debe configurar este registro en el host DNS de Microsoft Online Services para que funcione correctamente con el dominio. |
|label|String| Valor que se usa al configurar el nombre del registro DNS en el host DNS. |
|recordType|String| Indica qué tipo de registro DNS representa esta entidad.</br></br>El valor puede ser uno de los siguientes: *CName*, *Mx*, *Srv*, *Txt*</br></br>Clave |
|supportedService|String| Servicio o función de Microsoft Online que tiene una dependencia en el registro DNS.</br></br>Puede ser uno de los siguientes valores: **null**, *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer* o *Intune*|
|ttl|Int32| Valor que se debe usar al configurar la propiedad de período de vida (ttl) del registro DNS en el host DNS. No admite valores NULL |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

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