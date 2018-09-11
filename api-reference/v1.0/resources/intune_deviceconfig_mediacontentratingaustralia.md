# <a name="mediacontentratingaustralia-resource-type"></a>Tipo de recurso mediaContentRatingAustralia

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|movieRating|[ratingAustraliaMoviesType](../resources/intune_deviceconfig_ratingaustraliamoviestype.md)|Calificación de películas seleccionada para Australia. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove18`.|
|tvRating|[ratingAustraliaTelevisionType](../resources/intune_deviceconfig_ratingaustraliatelevisiontype.md)|Clasificación de TV seleccionada para Australia. Los valores posibles son: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingAustralia"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingAustralia",
  "movieRating": "String",
  "tvRating": "String"
}
```








