# <a name="grouplifecyclepolicy-resource-type"></a>tipo de recurso groupLifecyclePolicy

Representa una directiva de ciclo de vida de un grupo de Office 365. Una directiva de ciclo de vida de grupo permite a los administradores establecer un período de expiración para los grupos. Por ejemplo, después de 180 días, un grupo expira. Cuando un grupo llega a su expiración, sus propietarios deben renovar su grupo en el intervalo de tiempo definido por el administrador. Una vez renovado, la expiración del grupo se amplía por el número de días definidos en la directiva. Por ejemplo, la nueva expiración del grupo es 180 días después de la renovación. Si no se renueva el grupo, este expira y se elimina. El grupo se puede restaurar en un período de 30 días después de la eliminación.

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
|[Obtener groupLifecyclePolicy](../api/grouplifecyclepolicy_get.md) | [groupLifecyclePolicy](grouplifecyclepolicy.md) |Lee las propiedades y relaciones de un objeto groupLifecyclePolicy.|
|[Mostrar groupLifecyclePolicies](../api/grouplifecyclepolicy_list.md) | Colección de [groupLifecyclePolicy](grouplifecyclepolicy.md) | Muestra todos los objetos groupLifecyclePolicies. |
|[Actualizar groupLifecyclePolicy](../api/grouplifecyclepolicy_update.md) | [groupLifecyclePolicy](grouplifecyclepolicy.md) | Actualiza un objeto groupLifecyclePolicy. |
|[Eliminar groupLifecyclePolicy](../api/grouplifecyclepolicy_delete.md) | Ninguno | Elimina un objeto groupLifecyclePolicy. |
|[Agregar un grupo a un groupLifecyclePolicy](../api/grouplifecyclepolicy_addgroup.md)|Ninguno| Agrega un grupo a una directiva de ciclo de vida. |
|[Quitar un grupo de un groupLifecyclePolicy](../api/grouplifecyclepolicy_removegroup.md)|Ninguno| Quita un grupo a una directiva de ciclo de vida. |

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|alternateNotificationEmails|String| Lista de direcciones de correo electrónico para enviar notificaciones para grupos sin propietarios. Se pueden definir varias direcciones de correo electrónico separando una de la otra con un punto y coma. |
|groupLifetimeInDays|Int32| Número de días que faltan para que un grupo expire y necesite renovarse. Una vez renovado, la expiración del grupo se amplía por el número de días definidos. |
|id|Guid| Identificador único para una directiva. Solo lectura.|
|managedGroupTypes|String| El tipo de grupo al que se aplica la directiva de expiración. Los valores posibles son **Todos**, **Seleccionados** o **Ninguno**. |

## <a name="relationships"></a>Relaciones

Ninguna.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.groupLifecyclePolicy"
}-->

```json
{
  "alternateNotificationEmails": "String",
  "groupLifetimeInDays": 180,
  "id": "Guid (identifier)",
  "managedGroupTypes": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupLifecyclePolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->