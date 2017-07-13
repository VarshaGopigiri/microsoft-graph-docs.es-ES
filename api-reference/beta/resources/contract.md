# Tipo de recurso Contract
<a id="contract-resource-type" class="xliff"></a>
Representa una asociación existente que tiene el espacio empresarial asociado con un espacio empresarial del cliente.

> **Importante:** Solo existe en los inquilinos asociados. Los inquilinos asociados son los inquilinos de Azure AD que pertenecen a los socios de Microsoft que forman parte de los programas [Proveedor de soluciones en la nube de Microsoft](https://partnercenter.microsoft.com/en-us/partner/programs), Office 365 Syndication o Microsoft Advisor.

## Métodos
<a id="methods" class="xliff"></a>

| Método   | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
|[Obtener contrato](../api/contract_get.md) | Contrato |Lea las propiedades de un objeto de un contrato específico. |
|[Enumerar contratos](../api/contract_list.md) | Colección de contratos | Lista de contratos de los inquilinos asociados. |

## Propiedades
<a id="properties" class="xliff"></a>
| Propiedad   | Tipo | Descripción |
|:---------------|:--------|:----------|
|contractType|Cadena|Tipo de contrato.<br><br>Los valores posibles son:<br> *SyndicationPartner* - socio que tan solo revende y administra O365 e Intune para este cliente. Revenden y dan soporte a sus clientes.<br> *BreadthPartner*: socio que tiene la capacidad de proporcionar soporte administrativo a este cliente. En cambio, no se le permite revender a los clientes.<br>*ResellerPartner*: socio que es similar a un socio de distribución ("syndication partner"), salvo que el socio no tenga acceso exclusivo a un inquilino. En el caso de la distribución, el cliente no puede comprar suscripciones adicionales directas de Microsoft u otros socios.|
|customerId|Guid|El identificador único para el inquilino del cliente al que hace referencia esta asociación. Corresponde a la propiedad del id. del recurso de organización del inquilino del cliente. |
|defaultDomainName|String|Una copia del nombre de dominio predeterminado del inquilino del cliente. La copia se realiza cuando se establece la asociación con el cliente. No se actualiza automáticamente si el nombre de dominio predeterminado del inquino del cliente cambia.|
|displayName|String|Una copia del nombre que se muestra del inquilino del cliente. La copia se realiza cuando se establece la asociación con el cliente. No se actualiza automáticamente si el nombre que se muestra del inquino del cliente cambia.|
|id|String| El identificador único del socio. Clave, solo lectura. |

## Relaciones
<a id="relationships" class="xliff"></a>
Ninguno


## Representación JSON
<a id="json-representation" class="xliff"></a>
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.Contract"
}-->

```json
{
  "contractType": "String",
  "customerId": "Guid",
  "defaultDomainName": "String",
  "displayName": "String",
  "id": "String (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Contract resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->