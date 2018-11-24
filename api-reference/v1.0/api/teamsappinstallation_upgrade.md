# <a name="upgrade-an-app-in-a-team"></a><span data-ttu-id="b6e7b-101">Actualización de una aplicación en un equipo</span><span class="sxs-lookup"><span data-stu-id="b6e7b-101">Upgrade an app in a team</span></span>



<span data-ttu-id="b6e7b-102">Actualiza una [instalación de la aplicación](../resources/teamsappinstallation.md) en un [equipo](../resources/team.md) a la versión más reciente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6e7b-102">Upgrades an [app installation](../resources/teamsappinstallation.md) in a [team](../resources/team.md) to the latest version of the app.</span></span>

## <a name="permissions"></a><span data-ttu-id="b6e7b-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b6e7b-103">Permissions</span></span>

<span data-ttu-id="b6e7b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b6e7b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b6e7b-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6e7b-106">Permission type</span></span>      | <span data-ttu-id="b6e7b-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6e7b-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b6e7b-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6e7b-108">Delegated (work or school account)</span></span> | <span data-ttu-id="b6e7b-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6e7b-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b6e7b-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6e7b-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b6e7b-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6e7b-111">Not supported.</span></span>    |
|<span data-ttu-id="b6e7b-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6e7b-112">Application</span></span> | <span data-ttu-id="b6e7b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6e7b-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b6e7b-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6e7b-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/installedApps/{id}/upgrade
```

## <a name="request-headers"></a><span data-ttu-id="b6e7b-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6e7b-115">Request headers</span></span>
| <span data-ttu-id="b6e7b-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6e7b-116">Header</span></span>       | <span data-ttu-id="b6e7b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b6e7b-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b6e7b-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6e7b-118">Authorization</span></span>  | <span data-ttu-id="b6e7b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6e7b-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b6e7b-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6e7b-121">Request body</span></span>
<span data-ttu-id="b6e7b-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b6e7b-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b6e7b-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6e7b-123">Response</span></span>

<span data-ttu-id="b6e7b-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6e7b-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b6e7b-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6e7b-126">Example</span></span>

#### <a name="request"></a><span data-ttu-id="b6e7b-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6e7b-127">Request</span></span>
<span data-ttu-id="b6e7b-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6e7b-128">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->

```http
POST /teams/{id}/installedApps/{id}/upgrade
```
#### <a name="response"></a><span data-ttu-id="b6e7b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6e7b-129">Response</span></span>
<span data-ttu-id="b6e7b-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6e7b-130">The following is an example of the response.</span></span> 

><span data-ttu-id="b6e7b-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6e7b-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
