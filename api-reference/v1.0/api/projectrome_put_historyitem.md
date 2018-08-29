# <a name="create-or-replace-a-historyitem"></a><span data-ttu-id="1a5fb-101">Crear o reemplazar un historyItem</span><span class="sxs-lookup"><span data-stu-id="1a5fb-101">Create or replace a history item</span></span>

<span data-ttu-id="1a5fb-102">Crear un nuevo elemento de historial o reemplazar uno existente para una actividad de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-102">Create a new or replace an existing history item for an existing user activity.</span></span>

## <a name="permissions"></a><span data-ttu-id="1a5fb-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="1a5fb-103">Permissions</span></span>

<span data-ttu-id="1a5fb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1a5fb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="1a5fb-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1a5fb-106">Permission type</span></span>      | <span data-ttu-id="1a5fb-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1a5fb-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1a5fb-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1a5fb-108">Delegated (work or school account)</span></span> | <span data-ttu-id="1a5fb-109">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="1a5fb-109">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="1a5fb-110">Delegado (cuenta Microsoft personal)</span><span class="sxs-lookup"><span data-stu-id="1a5fb-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1a5fb-111">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="1a5fb-111">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="1a5fb-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1a5fb-112">Application</span></span> | <span data-ttu-id="1a5fb-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1a5fb-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1a5fb-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /me/activities/{id}/historyItems/{id}
```

<span data-ttu-id="1a5fb-115">El id. debe ser un GUID.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-115">Id needs to be a GUID.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1a5fb-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1a5fb-116">Request headers</span></span>

|<span data-ttu-id="1a5fb-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="1a5fb-117">Name</span></span> | <span data-ttu-id="1a5fb-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="1a5fb-118">Type</span></span> | <span data-ttu-id="1a5fb-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a5fb-119">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="1a5fb-120">Autorización</span><span class="sxs-lookup"><span data-stu-id="1a5fb-120">Authorization</span></span> | <span data-ttu-id="1a5fb-121">cadena</span><span class="sxs-lookup"><span data-stu-id="1a5fb-121">string</span></span> | <span data-ttu-id="1a5fb-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-p102">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1a5fb-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1a5fb-124">Request body</span></span>

<span data-ttu-id="1a5fb-125">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [historyItem](../resources/projectrome_historyitem.md).</span><span class="sxs-lookup"><span data-stu-id="1a5fb-125">In the request body, supply a JSON representation of [directoryObject](../resources/projectrome_historyitem.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="1a5fb-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a5fb-126">Response</span></span>

<span data-ttu-id="1a5fb-127">Si tiene éxito, este método devuelve el código de respuesta `201 Created` si se ha creado el historyItem o `200 OK` si se ha reemplazado dicho historyItem.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-127">If successful, this method returns the `201 Created` response code if the historyItem was created or `200 OK` if the historyItem was replaced.</span></span>

## <a name="example"></a><span data-ttu-id="1a5fb-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1a5fb-128">Example</span></span>

#### <a name="request"></a><span data-ttu-id="1a5fb-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1a5fb-129">Request</span></span>

<span data-ttu-id="1a5fb-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-130">Here is an example of the request.</span></span>

<!-- {
    "blockType": "ignored",
    "name": "upsert_historyItem"
} -->

```http
PUT https://graph.microsoft.com/v1.0/me/activities/{activity-id}/historyItems/{item-id}
Content-type: application/json
Content-length: 364

{
    "startedDateTime": "2015-02-11T20:54:04.3457274+00:00",
    "userTimezone": "Africa/Casablanca",
    "lastActiveDateTime": "2015-02-11T20:54:04.3457274+00:00"
}
```

#### <a name="response"></a><span data-ttu-id="1a5fb-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a5fb-131">Response</span></span>

<span data-ttu-id="1a5fb-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-132">Here is an example of the response.</span></span>

<!-- {
    "blockType": "ignored",
    "truncated": true,
    "@odata.type": "microsoft.graph.activityHistoryItem"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('user%40contoso.com')/activities('13881113971988980728')/historyItems/$entity",
    "status": "updated",
    "userTimezone": "Africa/Casablanca",
    "createdDateTime": "2018-02-26T20:28:22.14Z",
    "lastModifiedDateTime": "2018-02-26T20:28:22.155Z",
    "id": "9d0b74e4-4b41-43ea-b34d-f9c1bf9f809c",
    "startedDateTime": "2018-02-26T20:54:04.345Z",
    "lastActiveDateTime": "2018-02-26T20:54:24.345Z",
    "expirationDateTime": "2018-03-28T20:28:22.14Z",
    "activeDurationSeconds": 20
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Upsert historyitem",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->