# <a name="privacyprofile-resource-type"></a>Tipo de recurso privacyProfile

Representa el perfil de privacidad de una compañía; incluye la dirección URL de una declaración de privacidad y una persona de contacto para las preguntas sobre la declaración de privacidad.

## <a name="properties"></a>Propiedades
| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|contactEmail|String| Dirección de correo electrónico smtp válida para el contacto de la declaración de privacidad. No se requiere.|
|statementUrl|String| Formato de URL válido que empiece por http:// o https://. La longitud máxima es de 255 caracteres. Dirección URL que se dirige a la declaración de privacidad de la compañía. No se requiere.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privacyProfile"
}-->

```json
{
  "contactEmail": "string",
  "statementUrl": "string"
}
```