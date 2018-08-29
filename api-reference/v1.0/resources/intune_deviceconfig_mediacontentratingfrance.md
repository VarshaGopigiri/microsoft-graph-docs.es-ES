# <a name="mediacontentratingfrance-resource-type"></a>Tipo de recurso mediaContentRatingFrance

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|movieRating|[ratingFranceMoviesType](../resources/intune_deviceconfig_ratingfrancemoviestype.md)|Clasificación de películas seleccionada para Francia. Los valores posibles son `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16` y `agesAbove18`.|
|tvRating|[ratingFranceTelevisionType](../resources/intune_deviceconfig_ratingfrancetelevisiontype.md)|Clasificación de TV seleccionada para Francia. Los valores posibles son `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16` y `agesAbove18`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingFrance"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingFrance",
  "movieRating": "String",
  "tvRating": "String"
}
```



