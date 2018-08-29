# <a name="mediacontentratingunitedstates-resource-type"></a>Tipo de recurso mediaContentRatingUnitedStates

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|movieRating|[ratingUnitedStatesMoviesType](../resources/intune_deviceconfig_ratingunitedstatesmoviestype.md)|Calificación de películas seleccionada para Estados Unidos. Los valores posibles son `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `parentalGuidance13`, `restricted` y `adults`.|
|tvRating|[ratingUnitedStatesTelevisionType](../resources/intune_deviceconfig_ratingunitedstatestelevisiontype.md)|Clasificación de TV seleccionada para Estados Unidos. Los valores posibles son: `allAllowed`, `allBlocked`, `childrenAll`, `childrenAbove7`, `general`, `parentalGuidance`, `childrenAbove14` y `adults`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingUnitedStates",
  "movieRating": "String",
  "tvRating": "String"
}
```



