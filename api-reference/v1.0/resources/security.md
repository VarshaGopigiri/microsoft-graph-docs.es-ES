# <a name="security-resource-type"></a><span data-ttu-id="81b91-101">Tipo de recurso de seguridad</span><span class="sxs-lookup"><span data-stu-id="81b91-101">security resource type</span></span>

<span data-ttu-id="81b91-102">El recurso de seguridad es el punto de entrada para el modelo de objetos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="81b91-102">The security resource is the entry point for the Security object model.</span></span> <span data-ttu-id="81b91-103">Devuelve un recurso de seguridad singleton.</span><span class="sxs-lookup"><span data-stu-id="81b91-103">It returns a singleton security resource.</span></span> <span data-ttu-id="81b91-104">No contiene todas las propiedades utilizables.</span><span class="sxs-lookup"><span data-stu-id="81b91-104">It doesn't contain any usable properties.</span></span>

## <a name="methods"></a><span data-ttu-id="81b91-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="81b91-105">Methods</span></span>

| <span data-ttu-id="81b91-106">Método</span><span class="sxs-lookup"><span data-stu-id="81b91-106">Method</span></span>       | <span data-ttu-id="81b91-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81b91-107">Return Type</span></span> | <span data-ttu-id="81b91-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="81b91-108">Description</span></span> |
|:-------------|:------------|:------------|
| [<span data-ttu-id="81b91-109">Alertas de lista</span><span class="sxs-lookup"><span data-stu-id="81b91-109">List alerts</span></span>](../api/alert_list.md) | <span data-ttu-id="81b91-110">Colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="81b91-110">[alert](alert.md) collection</span></span> | <span data-ttu-id="81b91-111">Obtiene una colección de objetos de alerta.</span><span class="sxs-lookup"><span data-stu-id="81b91-111">Get a licenseDetails object collection.</span></span> |
| [<span data-ttu-id="81b91-112">obtener alertas</span><span class="sxs-lookup"><span data-stu-id="81b91-112">get alerts</span></span>](../api/alert_get.md) | <span data-ttu-id="81b91-113">Colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="81b91-113">[alert](alert.md) collection</span></span> | <span data-ttu-id="81b91-114">Obtener un objeto de alerta.</span><span class="sxs-lookup"><span data-stu-id="81b91-114">Get a alert object.</span></span> |
| [<span data-ttu-id="81b91-115">Actualización de alertas</span><span class="sxs-lookup"><span data-stu-id="81b91-115">Update alerts</span></span>](../api/alert_update.md) | <span data-ttu-id="81b91-116">Colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="81b91-116">[alert](alert.md) collection</span></span> | <span data-ttu-id="81b91-117">Obtener un objeto de alerta.</span><span class="sxs-lookup"><span data-stu-id="81b91-117">Get a alert object.</span></span> |

## <a name="properties"></a><span data-ttu-id="81b91-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81b91-118">Properties</span></span>
<span data-ttu-id="81b91-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="81b91-119">None</span></span>

## <a name="relationships"></a><span data-ttu-id="81b91-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="81b91-120">Relationships</span></span>
| <span data-ttu-id="81b91-121">Relación</span><span class="sxs-lookup"><span data-stu-id="81b91-121">Relationship</span></span> | <span data-ttu-id="81b91-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="81b91-122">Type</span></span>        | <span data-ttu-id="81b91-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="81b91-123">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="81b91-124">alertas</span><span class="sxs-lookup"><span data-stu-id="81b91-124">alerts</span></span>|<span data-ttu-id="81b91-125">Colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="81b91-125">[alert](alert.md) collection</span></span>| <span data-ttu-id="81b91-p102">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="81b91-p102">Read-only. Nullable.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="81b91-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="81b91-128">JSON representation</span></span>
<span data-ttu-id="81b91-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="81b91-129">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.security"
}-->

```json
{
}
```

## <a name="example"></a><span data-ttu-id="81b91-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="81b91-130">Example</span></span>

<span data-ttu-id="81b91-131">El recurso **security** está disponible en la raíz del gráfico.</span><span class="sxs-lookup"><span data-stu-id="81b91-131">The **planner** resource is available at the root of the graph.</span></span>

<!--{
  "blockType": "request"
}-->
```http
GET https://graph.microsoft.com/v1.0/security
```

<!--{
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security"
}-->
```json
HTTP/1.1 200 OK
Content-type: application/json

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "security resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->