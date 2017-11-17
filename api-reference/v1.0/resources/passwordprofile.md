# <a name="passwordprofile-resource-type"></a><span data-ttu-id="60296-101">Tipo de recurso passwordProfile</span><span class="sxs-lookup"><span data-stu-id="60296-101">passwordProfile resource type</span></span>

<span data-ttu-id="60296-p101">Contiene el perfil de contraseña asociado al usuario. La propiedad **passwordProfile** de la entidad [user](user.md) es un objeto **passwordProfile**.</span><span class="sxs-lookup"><span data-stu-id="60296-p101">Contains the password profile associated with a user. The **passwordProfile** property of the [user](user.md) entity is a **passwordProfile** object.</span></span>


## <a name="properties"></a><span data-ttu-id="60296-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60296-104">Properties</span></span>
| <span data-ttu-id="60296-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60296-105">Property</span></span>     | <span data-ttu-id="60296-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="60296-106">Type</span></span>   |<span data-ttu-id="60296-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="60296-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="60296-108">forceChangePasswordNextSignIn</span><span class="sxs-lookup"><span data-stu-id="60296-108">forceChangePasswordNextSignIn</span></span>|<span data-ttu-id="60296-109">Boolean</span><span class="sxs-lookup"><span data-stu-id="60296-109">Boolean</span></span>| <span data-ttu-id="60296-110">**true** si el usuario debe cambiar su contraseña en el próximo inicio de sesión; en caso contrario **false**.</span><span class="sxs-lookup"><span data-stu-id="60296-110">**true** if the user must change her password on the next login; otherwise **false**.</span></span> |
|<span data-ttu-id="60296-111">password</span><span class="sxs-lookup"><span data-stu-id="60296-111">password</span></span>|<span data-ttu-id="60296-112">String</span><span class="sxs-lookup"><span data-stu-id="60296-112">String</span></span>|<span data-ttu-id="60296-p102">Contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. Se puede actualizar, pero el usuario deberá cambiar la contraseña en el próximo inicio de sesión. La contraseña debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies** del usuario. De manera predeterminada, se requiere una contraseña segura.</span><span class="sxs-lookup"><span data-stu-id="60296-p102">The password for the user. This property is required when a user is created. It can be updated, but the user will be required to change the password on the next login. The password must satisfy minimum requirements as specified by the user’s **passwordPolicies** property. By default, a strong password is required.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="60296-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="60296-118">JSON representation</span></span>

<span data-ttu-id="60296-119">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="60296-119">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.passwordprofile"
}-->

```json
{
  "forceChangePasswordNextSignIn": true,
  "password": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "passwordProfile resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->