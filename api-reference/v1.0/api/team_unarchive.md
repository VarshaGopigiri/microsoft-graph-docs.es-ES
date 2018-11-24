# <a name="unarchive-team"></a><span data-ttu-id="89312-101">Unarchive equipo</span><span class="sxs-lookup"><span data-stu-id="89312-101">Unarchive team</span></span>



<span data-ttu-id="89312-102">Restauración de un [equipo](../resources/team.md)de archivado.</span><span class="sxs-lookup"><span data-stu-id="89312-102">Restore an archived [team](../resources/team.md).</span></span> <span data-ttu-id="89312-103">Esto restaura la capacidad de los usuarios enviar mensajes y editar el equipo, respetando por la configuración de inquilino y del equipo.</span><span class="sxs-lookup"><span data-stu-id="89312-103">This restores users' ability to send messages and edit the team, abiding by tenant and team settings.</span></span> <span data-ttu-id="89312-104">Los equipos se archivan con el [archivo](team_archive.md) API.</span><span class="sxs-lookup"><span data-stu-id="89312-104">Teams are archived using the [archive](team_archive.md) API.</span></span>

<span data-ttu-id="89312-105">Unarchiving es una operación asíncrona.</span><span class="sxs-lookup"><span data-stu-id="89312-105">Unarchiving is an async operation.</span></span> <span data-ttu-id="89312-106">Un equipo es sin archivar una vez que la operación asincrónica se completa correctamente, lo que puede producirse con posterioridad a una respuesta desde esta API.</span><span class="sxs-lookup"><span data-stu-id="89312-106">A team is unarchived once the async operation completes successfully, which may occur subsequent to a response from this API.</span></span>

## <a name="permissions"></a><span data-ttu-id="89312-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="89312-107">Permissions</span></span>
<span data-ttu-id="89312-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="89312-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="89312-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="89312-110">Permission type</span></span>      | <span data-ttu-id="89312-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="89312-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="89312-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="89312-112">Delegated (work or school account)</span></span> | <span data-ttu-id="89312-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="89312-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="89312-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89312-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="89312-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89312-115">Not supported.</span></span>    |
|<span data-ttu-id="89312-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="89312-116">Application</span></span> | <span data-ttu-id="89312-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="89312-117">Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="89312-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="89312-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/unarchive
```

## <a name="request-headers"></a><span data-ttu-id="89312-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="89312-119">Request headers</span></span>
| <span data-ttu-id="89312-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89312-120">Header</span></span>       | <span data-ttu-id="89312-121">Valor</span><span class="sxs-lookup"><span data-stu-id="89312-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="89312-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="89312-122">Authorization</span></span>  | <span data-ttu-id="89312-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="89312-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="89312-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="89312-125">Request body</span></span>
<span data-ttu-id="89312-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="89312-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="89312-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89312-127">Response</span></span>

<span data-ttu-id="89312-128">Si unarchiving se ha iniciado correctamente, este método devuelve una `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="89312-128">If unarchiving is started successfully, this method returns a `202 Accepted` response code.</span></span> <span data-ttu-id="89312-129">La respuesta contendrá también un `Location` encabezado, que contiene la ubicación de la [teamsAsyncOperation](../resources/teamsasyncoperation.md) que se creó para controlar unarchiving del equipo.</span><span class="sxs-lookup"><span data-stu-id="89312-129">The response will also contain a `Location` header, which contains the location of the [teamsAsyncOperation](../resources/teamsasyncoperation.md) that was created to handle unarchiving of the team.</span></span> <span data-ttu-id="89312-130">Comprobar el estado de la operación unarchiving mediante la realización de una solicitud GET en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="89312-130">Check the status of the unarchiving operation by making a GET request to this location.</span></span>

## <a name="example"></a><span data-ttu-id="89312-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89312-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="89312-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="89312-132">Request</span></span>
<span data-ttu-id="89312-133">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="89312-133">The following is an example of a request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "unarchive_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/unarchive
```

#### <a name="response"></a><span data-ttu-id="89312-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89312-134">Response</span></span>
<span data-ttu-id="89312-135">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="89312-135">The following is an example of a response.</span></span>
```http
HTTP/1.1 202 Accepted
Location: /teams{id}/operations({opId})
Content-Type: text/plain
Content-Length: 0
```

<!-- uuid: 9a9bb83f-6f35-4426-bb04-73ca43ad6cc8
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Unarchive team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
