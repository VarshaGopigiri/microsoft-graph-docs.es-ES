---
title: tipo de recurso synchronizationSchema
description: Define los objetos que se va a ser sincronizado y cómo se sincronizarán. El esquema de sincronización contiene la mayoría de la información de configuración para un trabajo de sincronización determinado. Normalmente, va a personalizar algunas de las asignaciones de atributo, o agregar un filtro de ámbito para sincronizar solo los objetos que cumplen una condición determinada.
localization_priority: Normal
ms.openlocfilehash: 696bdbbc6fa2d96965d11a12fb09fdfc0ce16106
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27847323"
---
# <a name="synchronizationschema-resource-type"></a>tipo de recurso synchronizationSchema

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Define los objetos que se va a ser sincronizado y cómo se sincronizarán. El esquema de sincronización contiene la mayoría de la información de configuración para un trabajo de sincronización determinado. Normalmente, va a personalizar algunas de las [asignaciones de atributos](synchronization-attributemapping.md), o agregar un [filtro de ámbito](synchronization-filter.md) para sincronizar solo los objetos que cumplen una condición determinada.

En las secciones siguientes se describen los componentes de alto nivel del esquema de sincronización.

## <a name="directory-definitions"></a>Definiciones de Active Directory

[Definiciones de Active Directory](synchronization-directorydefinition.md) proporcionan la información del motor de sincronización acerca de los directorios y sus objetos. Por ejemplo, la definición de Active directory indica que el motor de sincronización que un directorio de Azure AD tiene objetos con nombre de **usuario** y **grupo**, los atributos que se admiten para los objetos y los tipos de dichos atributos. En orden para un objeto determinado y un atributo que se utilizará en las asignaciones de reglas y objetos de sincronización, que deben definirse como parte de la definición de Active directory.

## <a name="synchronization-rules"></a>Reglas de sincronización

[Reglas de sincronización](synchronization-synchronizationrule.md) son el núcleo de la configuración de sincronización. Definen cómo debe realizarse la sincronización para el motor de sincronización, incluidos los objetos que se deben sincronizar, cómo objetos desde el directorio de origen deben coincidir con los objetos en el directorio de destino, y cómo se deben atributos transforma cuando se está sincronizando desde el origen al directorio de destino. 

## <a name="object-mappings"></a>Asignaciones de objetos

[Las asignaciones de objeto](synchronization-objectmapping.md) son la parte principal de la regla de sincronización. Cada asignación de objeto define cómo se debe sincronizar un objeto determinado desde el origen al directorio de destino. En particular, la asignación define cómo un objeto en el directorio de origen debe coincidir con un objeto en el directorio de destino, ¿qué (si hay alguno) filtros de ámbito se debe utilizar para decidir si va a aprovisionar un objeto, y cómo se deben transformar los atributos de objeto Cuando está sincronizados desde el origen al directorio de destino.

## <a name="methods"></a>Métodos

| Método        | Tipo de valor devuelto               | Descripción                  |
|:--------------|:--------------------------|:-----------------------------|
|[Obtener un esquema](../api/synchronization-synchronizationschema-get.md)    |[synchronizationSchema](synchronization-synchronizationschema.md)   |Leer las propiedades y las relaciones del objeto **synchronizationSchema** .|
|[Actualizar esquema](../api/synchronization-synchronizationschema-update.md)    |Ninguno   |Actualizar el esquema de sincronización. |
|[Eliminar esquema](../api/synchronization-synchronizationschema-delete.md)    |Ninguno   |Eliminar el esquema personalizado, restablecer el esquema a la configuración predeterminada. |
|[Operadores de filtro de lista](../api/synchronization-synchronizationschema-filteroperators.md)    |colección de [filterOperatorSchema](../resources/synchronization-filteroperatorschema.md)   |Lista de todos los operadores compatibles con los filtros de ámbito. |
|[Atributo de la lista de funciones de asignación](../api/synchronization-synchronizationschema-functions.md)    |colección de [attributeMappingFunctionSchema](../resources/synchronization-attributemappingfunctionschema.md)   |Lista de todas las funciones compatibles con las expresiones de asignación de atributo. |
|[Analizar la expresión de asignación de atributo](../api/synchronization-synchronizationschema-parseexpression.md)|[parseExpressionResponse](synchronization-parseexpressionresponse.md)|Analizar una expresión de cadena en un [attributeMappingSource|(.. / resources/synchronization_attributemappingsource.md) objeto.|


## <a name="properties"></a>Propiedades

| Propiedad      | Tipo      | Description    |
|:--------------|:----------|:---------------|
|directories            |colección de [directoryDefinition](synchronization-directorydefinition.md)   |Describe los objetos que forman parte de la [synchronizationJob](synchronization-synchronizationjob.md) o [synchronizationTemplate](synchronization-synchronizationtemplate.md)y directorios. |
|synchronizationRules   |colección de [synchronizationRule](synchronization-synchronizationrule.md)   |Una colección de reglas de sincronización configurado para el [synchronizationJob](synchronization-synchronizationjob.md) o [synchronizationTemplate](synchronization-synchronizationtemplate.md), |
|version                |Cadena                             |La versión del esquema, que se actualizan automáticamente con todos los cambios de esquema.|


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationSchema"
}-->

```json
{
  "directories": [{"@odata.type": "microsoft.graph.directoryDefinition"}],
  "provisioningTaskIdentifier": "String (identifier)",
  "synchronizationRules": [{"@odata.type": "microsoft.graph.synchronizationRule"}],
  "version": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationSchema resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
