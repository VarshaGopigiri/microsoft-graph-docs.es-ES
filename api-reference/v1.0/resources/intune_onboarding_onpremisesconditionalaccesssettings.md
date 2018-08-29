# <a name="onpremisesconditionalaccesssettings-resource-type"></a>Tipo de recurso onPremisesConditionalAccessSettings

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener onPremisesConditionalAccessSettings](../api/intune_onboarding_onpremisesconditionalaccesssettings_get.md)|[onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md)|Lea las propiedades y las relaciones del objeto [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md).|
|[Actualizar onPremisesConditionalAccessSettings](../api/intune_onboarding_onpremisesconditionalaccesssettings_update.md)|[onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md)|Actualice las propiedades de un objeto [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Todavía no documentado|
|enabled|Booleano|Indica si está habilitado el acceso condicional local para esta organización|
|includedGroups|Colección Guid|Grupos de usuarios a los que se dirigirá el acceso condicional local. Todos los usuarios de estos grupos deberán tener dispositivos móviles administrados y compatibles para tener acceso al correo.|
|excludedGroups|Colección Guid|Grupos de usuarios que estarán exentos del acceso condicional local. Todos los usuarios de estos grupos estarán exentos de la directiva de acceso condicional.|
|overrideDefaultRule|Booleano|Anular la regla de acceso predeterminada al permitir que un dispositivo garantice que se concede el acceso.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.onPremisesConditionalAccessSettings"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.onPremisesConditionalAccessSettings",
  "id": "String (identifier)",
  "enabled": true,
  "includedGroups": [
    "fe4d7f2b-e7b8-4276-9976-7a3fc83edbbc"
  ],
  "excludedGroups": [
    "79199ed9-e50b-4257-8de4-70b9c8685061"
  ],
  "overrideDefaultRule": true
}
```



