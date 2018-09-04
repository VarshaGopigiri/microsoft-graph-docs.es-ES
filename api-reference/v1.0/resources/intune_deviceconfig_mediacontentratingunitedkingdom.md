# <a name="mediacontentratingunitedkingdom-resource-type"></a>Tipo de recurso mediaContentRatingUnitedKingdom

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|movieRating|[ratingUnitedKingdomMoviesType](../resources/intune_deviceconfig_ratingunitedkingdommoviestype.md)|Clasificación de películas seleccionada para el Reino Unido. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15` y `adults`.|
|tvRating|[ratingUnitedKingdomTelevisionType](../resources/intune_deviceconfig_ratingunitedkingdomtelevisiontype.md)|Clasificación de TV seleccionada para el Reino Unido. Los valores posibles son: `allAllowed`, `allBlocked` y `caution`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingUnitedKingdom",
  "movieRating": "String",
  "tvRating": "String"
}
```



