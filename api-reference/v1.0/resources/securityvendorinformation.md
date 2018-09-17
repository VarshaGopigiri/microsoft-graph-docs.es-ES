# <a name="securityvendorinformation-resource-type"></a>Tipo de recurso securityVendorInformation

Contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y el subproveedor (por ejemplo, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|proveedor *|Cadena|Proveedor específico (producto/servicio - no empresa proveedora); por ejemplo, WindowsDefenderATP.|
|providerVersion|Cadena|Versión del proveedor o subprovider, si existe, que generó la alerta.|
|subProvider|Cadena|Subproveedor específico (debajo de agregación de proveedor); Por ejemplo, WindowsDefenderATP.SmartScreen.|
|proveedor *|Cadena|Nombre del proveedor de alerta (por ejemplo, Microsoft, Dell, FireEye).|
(\* Indica un campo obligatorio.)

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.securityVendorInformation"
}-->

```json
{
  "provider": "String",
  "providerVersion": "String",
  "subProvider": "String",
  "vendor": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "securityVendorInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
