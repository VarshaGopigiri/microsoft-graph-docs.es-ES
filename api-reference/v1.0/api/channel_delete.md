# <a name="delete-channel"></a><span data-ttu-id="de578-101">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="de578-101">Delete channel</span></span>



<span data-ttu-id="de578-102">Eliminar el [canal](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="de578-102">Delete the [channel](../resources/channel.md).</span></span>

> <span data-ttu-id="de578-103">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="de578-103">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="de578-104">Para obtener información detallada, vea el [conocido lista de problemas](../../../concepts/known_issues.md#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="de578-104">For details, see the [known issues list](../../../concepts/known_issues.md#application-permissions).</span></span>

> <span data-ttu-id="de578-105">**Nota**: los datos de canales eliminados seguirán almacenarse durante varias semanas permitir que el propietario del equipo de canal de recuperación eliminado.</span><span class="sxs-lookup"><span data-stu-id="de578-105">**Note**: The data in deleted channels will continue to be stored for several weeks to allow team owner to recovery deleted channel.</span></span> <span data-ttu-id="de578-106">Durante este tiempo, no se puede crear un canal nuevo con el mismo displayName.</span><span class="sxs-lookup"><span data-stu-id="de578-106">During that time, a new channel with the same displayName may not be created.</span></span>

## <a name="permissions"></a><span data-ttu-id="de578-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="de578-107">Permissions</span></span>
<span data-ttu-id="de578-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="de578-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="de578-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="de578-110">Permission type</span></span>      | <span data-ttu-id="de578-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="de578-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="de578-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="de578-112">Delegated (work or school account)</span></span> | <span data-ttu-id="de578-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="de578-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="de578-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="de578-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="de578-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de578-115">Not supported.</span></span>    |
|<span data-ttu-id="de578-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="de578-116">Application</span></span> | <span data-ttu-id="de578-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="de578-117">Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="de578-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="de578-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/channels/{id}
```
## <a name="request-headers"></a><span data-ttu-id="de578-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="de578-119">Request headers</span></span>
| <span data-ttu-id="de578-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de578-120">Header</span></span>       | <span data-ttu-id="de578-121">Valor</span><span class="sxs-lookup"><span data-stu-id="de578-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="de578-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="de578-122">Authorization</span></span>  | <span data-ttu-id="de578-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="de578-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="de578-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="de578-125">Request body</span></span>
<span data-ttu-id="de578-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="de578-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="de578-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de578-127">Response</span></span>

<span data-ttu-id="de578-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de578-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="de578-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de578-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="de578-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="de578-131">Request</span></span>
<span data-ttu-id="de578-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="de578-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_channel"
}-->

```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```

#### <a name="response"></a><span data-ttu-id="de578-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de578-133">Response</span></span>

<span data-ttu-id="de578-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de578-134">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
