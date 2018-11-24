# <a name="archive-team"></a><span data-ttu-id="ea3ca-101">Equipo de archivo</span><span class="sxs-lookup"><span data-stu-id="ea3ca-101">Archive team</span></span>



<span data-ttu-id="ea3ca-102">Archivar el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-102">Archive the specified [team](../resources/team.md).</span></span> <span data-ttu-id="ea3ca-103">Cuando un equipo se archiva, los usuarios pueden enviar ya no o como mensajes en cualquier canal en el equipo, modificar otras opciones de configuración, descripción o nombre del grupo o en general realizar mayoría de los cambios en el equipo.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-103">When a team is archived, users can no longer send or like messages on any channel in the team, edit the team's name, description, or other settings, or in general make most changes to the team.</span></span>
<span data-ttu-id="ea3ca-104">Continuarán con los cambios de pertenencia en el equipo que se permitirán.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-104">Membership changes to the team continue to be allowed.</span></span>

<span data-ttu-id="ea3ca-105">El archivado es una operación asíncrona.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-105">Archiving is an async operation.</span></span> <span data-ttu-id="ea3ca-106">Un equipo se archiva una vez que la operación asincrónica se completa correctamente, lo que puede producirse con posterioridad a una respuesta desde esta API.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-106">A team is archived once the async operation completes successfully, which may occur subsequent to a response from this API.</span></span>

<span data-ttu-id="ea3ca-107">Para poder archivar el equipo, el equipo y el [grupo](../resources/group.md) deben tener un propietario.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-107">In order to archive team, the team and [group](../resources/group.md) must have an owner.</span></span>

<span data-ttu-id="ea3ca-108">Para restaurar un equipo de su estado archivado, use la API de [unarchive](team_unarchive.md).</span><span class="sxs-lookup"><span data-stu-id="ea3ca-108">To restore a team from its archived state, use the API to [unarchive](team_unarchive.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="ea3ca-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="ea3ca-109">Permissions</span></span>
<span data-ttu-id="ea3ca-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ea3ca-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ea3ca-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea3ca-112">Permission type</span></span>      | <span data-ttu-id="ea3ca-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea3ca-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ea3ca-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea3ca-114">Delegated (work or school account)</span></span> | <span data-ttu-id="ea3ca-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea3ca-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ea3ca-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea3ca-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ea3ca-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-117">Not supported.</span></span>    |
|<span data-ttu-id="ea3ca-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea3ca-118">Application</span></span> | <span data-ttu-id="ea3ca-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea3ca-119">Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="ea3ca-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea3ca-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/archive
```
## <a name="request-headers"></a><span data-ttu-id="ea3ca-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea3ca-121">Request headers</span></span>
| <span data-ttu-id="ea3ca-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea3ca-122">Header</span></span>       | <span data-ttu-id="ea3ca-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ea3ca-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ea3ca-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea3ca-124">Authorization</span></span>  | <span data-ttu-id="ea3ca-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ea3ca-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea3ca-127">Request body</span></span>
<span data-ttu-id="ea3ca-128">En la solicitud, _opcionalmente_ puede incluir la `shouldSetSpoSiteReadOnlyForMembers` parámetro en un JSON body, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-128">In the request, you may _optionally_ include the `shouldSetSpoSiteReadOnlyForMembers` parameter in a JSON body, as follows.</span></span>
```JSON
{
    "shouldSetSpoSiteReadOnlyForMembers": true
}
```
<span data-ttu-id="ea3ca-129">Este parámetro opcional define si se va a establecer permisos para los miembros del equipo de solo lectura en el sitio de Sharepoint Online asociado con el equipo.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-129">This optional parameter defines whether to set permissions for team members to read-only on the Sharepoint Online site associated with the team.</span></span> <span data-ttu-id="ea3ca-130">Si se establece en false o se omite el cuerpo por completo, se producirá este paso se omitirá.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-130">Setting it to false or omitting the body altogether will result in this step being skipped.</span></span>

## <a name="response"></a><span data-ttu-id="ea3ca-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea3ca-131">Response</span></span>

<span data-ttu-id="ea3ca-132">Si el archivado se ha iniciado correctamente, este método devuelve una `202 Accepted` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-132">If archiving is started successfully, this method returns a `202 Accepted` response code.</span></span> <span data-ttu-id="ea3ca-133">La respuesta contendrá también un `Location` encabezado, que contiene la ubicación de la [teamsAsyncOperation](../resources/teamsasyncoperation.md) que se creó para controlar el archivado del equipo.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-133">The response will also contain a `Location` header, which contains the location of the [teamsAsyncOperation](../resources/teamsasyncoperation.md) that was created to handle archiving of the team.</span></span> <span data-ttu-id="ea3ca-134">Comprobar el estado de la operación de archivado mediante la realización de una solicitud GET en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-134">Check the status of the archiving operation by making a GET request to this location.</span></span>

## <a name="example"></a><span data-ttu-id="ea3ca-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea3ca-135">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ea3ca-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea3ca-136">Request</span></span>
<span data-ttu-id="ea3ca-137">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-137">The following is an example of a request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "archive_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/archive
```
#### <a name="response"></a><span data-ttu-id="ea3ca-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea3ca-138">Response</span></span>
<span data-ttu-id="ea3ca-139">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea3ca-139">The following is an example of a response.</span></span>
```http
HTTP/1.1 202 Accepted
Location: /teams{id}/operations({opId})
Content-Type: text/plain
Content-Length: 0
```
<!-- uuid: e848414b-4669-4484-ac36-1504c58a3fb8
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Archive team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
