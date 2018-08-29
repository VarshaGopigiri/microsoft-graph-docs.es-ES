# <a name="educationstudent-resource-type"></a>Tipo de recurso educationStudent

Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `student`.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|birthDate|Fecha| Fecha de nacimiento del alumno.|
|externalId|Cadena| Identificador del alumno en el sistema de origen.|
|gender|educationGender| Los valores posibles son: `female`, `male`, `other` y `unknownFutureValue`.|
|grade|Cadena|Curso actual del alumno.|
|graduationYear|Cadena| Año de graduación del alumno en el centro educativo.|
|studentNumber|Cadena| Número de alumno.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationStudent"
}-->

```json
{
  "birthDate": "String (timestamp)",
  "externalId": "String",
  "gender": "educationGender",
  "grade": "String",
  "graduationYear": "String",
  "studentNumber": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationStudent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
