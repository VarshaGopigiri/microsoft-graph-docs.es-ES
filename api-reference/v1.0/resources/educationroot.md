# <a name="educationroot-resource-type"></a>Tipo de recurso educationRoot

El espacio de nombres `/education` expone funcionalidad específica del sector educativo. Algunos objetos del espacio de nombres `/education` pueden encontrarse en otras partes de Microsoft Graph (por ejemplo, [users](user.md)). El espacio de nombres de educación ofrece características y propiedades específicas del ámbito educativo en esos objetos.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear educationClass](../api/educationroot_post_classes.md) |[educationClass](educationclass.md)| Cree un objeto **educationClass** publicando en la colección de clases.|
|[Enumerar clases](../api/educationroot_list_classes.md) |Colección [educationClass](educationclass.md)| Obtenga una colección de objetos **educationClass**.|
|[Crear educationSchool](../api/educationroot_post_schools.md) |[educationSchool](educationschool.md)| Cree un objeto **educationSchool** publicando en la colección de centros educativos.|
|[Enumerar centros educativos](../api/educationroot_list_schools.md) |Colección [educationSchool](educationschool.md)| Obtenga una colección de objetos **educationSchool**.|
|[Crear educationUser](../api/educationroot_post_users.md) |[educationUser](educationuser.md)| Cree un objeto **educationUser** publicando en la colección de usuarios.|
|[Enumerar usuarios](../api/educationroot_list_users.md) |Colección [educationUser](educationuser.md)| Obtenga una colección de objetos **educationUser**.|

## <a name="properties"></a>Propiedades
Ninguna.

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|classes|Colección [educationClass](educationclass.md)| Solo lectura. Admite valores NULL.|
|me|[educationUser](educationuser.md)| Solo lectura. Admite valores NULL.|
|schools|Colección [educationSchool](educationschool.md)| Solo lectura. Admite valores NULL.|
|users|Colección [educationUser](educationuser.md)| Solo lectura. Admite valores NULL.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationRoot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->