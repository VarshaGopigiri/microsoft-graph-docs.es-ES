# <a name="hostsecuritystate-resource-type"></a>Tipo de recurso hostSecurityState

Contiene información de estado acerca del host (incluidos los dispositivos, equipos, etc.).

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|fqdn|Cadena|Nombre de dominio completo del host (por ejemplo, `machine.company.com`).|
|isAzureAadJoined|Booleano|True si el host es el dominio unido a los servicios de dominio de Azure Active Directory.|
|isAzureAadRegistered|Booleano|True si el host se ha registrado con el registro de dispositivos de Azure Active Directory (dispositivos BYOD, es decir, no administrados por completo por la empresa).|
|isHybridAzureDomainJoined|Booleano|True si el host se ha unido a un dominio local de Active Directory.|
|netBiosName|Cadena|El nombre de host local, sin el nombre de dominio DNS.|
|os|Cadena|Sistema operativo del host. (Por ejemplo, Windows10, Mac OS, RHEL, etcetera.).|
|privateIpAddress|Cadena|Dirección de IPv4 o IPv6 (no enrutable) privada (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) en el momento de la alerta.|
|publicIpAddress|Cadena|Dirección IPv4 o IPv6 enrutable públicamente (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) en el momento de la alerta.|
|riskScore|Cadena|Puntuación de riesgo calculado/generado por el proveedor del host.  Intervalo de valores recomendados de 0 a 1, que equivale a un porcentaje.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.hostSecurityState"
}-->

```json
{
  "fqdn": "String",
  "isAzureAadJoined": true,
  "isAzureAadRegistered": true,
  "isHybridAzureDomainJoined": true,
  "netBiosName": "String",
  "os": "String",
  "privateIpAddress": "String",
  "publicIpAddress": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "hostSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
