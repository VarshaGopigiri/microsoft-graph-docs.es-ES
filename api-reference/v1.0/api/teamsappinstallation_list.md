# <a name="list-apps-in-team"></a><span data-ttu-id="325e9-101">Lista de aplicaciones en el equipo</span><span class="sxs-lookup"><span data-stu-id="325e9-101">List apps in team</span></span>



<span data-ttu-id="325e9-102">Recuperar la lista de [aplicaciones instalado](../resources/teamsappinstallation.md) en el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="325e9-102">Retrieve the list of [apps installed](../resources/teamsappinstallation.md) in the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="325e9-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="325e9-103">Permissions</span></span>

<span data-ttu-id="325e9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="325e9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="325e9-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="325e9-106">Permission type</span></span>      | <span data-ttu-id="325e9-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="325e9-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="325e9-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="325e9-108">Delegated (work or school account)</span></span> | <span data-ttu-id="325e9-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="325e9-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="325e9-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="325e9-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="325e9-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="325e9-111">Not supported.</span></span>    |
|<span data-ttu-id="325e9-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="325e9-112">Application</span></span> | <span data-ttu-id="325e9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="325e9-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="325e9-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="325e9-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /teams/{id}/installedApps
```

## <a name="optional-query-parameters"></a><span data-ttu-id="325e9-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="325e9-115">Optional query parameters</span></span>

<span data-ttu-id="325e9-116">Este método admite la $filter, $select, y $expanda [Parámetros de consulta de OData](../../../concepts/query_parameters.md) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="325e9-116">This method supports the $filter, $select, and $expand [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="325e9-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="325e9-117">Request headers</span></span>

| <span data-ttu-id="325e9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="325e9-118">Header</span></span>       | <span data-ttu-id="325e9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="325e9-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="325e9-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="325e9-120">Authorization</span></span>  | <span data-ttu-id="325e9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="325e9-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="325e9-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="325e9-123">Request body</span></span>

<span data-ttu-id="325e9-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="325e9-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="325e9-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="325e9-125">Response</span></span>

<span data-ttu-id="325e9-126">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [teamsApp](../resources/teamsapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="325e9-126">If successful, this method returns a `200 OK` response code and collection of [teamsApp](../resources/teamsapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="325e9-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="325e9-127">Example</span></span>

### <a name="request"></a><span data-ttu-id="325e9-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="325e9-128">Request</span></span>

<span data-ttu-id="325e9-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="325e9-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_owners"
}-->

```http
GET https://graph.microsoft.com/beta/teams/{id}/installedApps
```

### <a name="response"></a><span data-ttu-id="325e9-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="325e9-130">Response</span></span>

<span data-ttu-id="325e9-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="325e9-131">The following is an example of the response.</span></span>
><span data-ttu-id="325e9-132">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="325e9-132">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="325e9-133">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="325e9-133">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

## <a name="example----getting-the-names-of-the-installed-apps"></a><span data-ttu-id="325e9-134">Ejemplo: obtener los nombres de las aplicaciones instaladas</span><span class="sxs-lookup"><span data-stu-id="325e9-134">Example -- getting the names of the installed apps</span></span>

### <a name="request"></a><span data-ttu-id="325e9-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="325e9-135">Request</span></span>

<span data-ttu-id="325e9-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="325e9-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_owners"
}-->

```http
GET https://graph.microsoft.com/beta/teams/{id}/installedApps?$expand=teamsAppDefinition
```

### <a name="response"></a><span data-ttu-id="325e9-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="325e9-137">Response</span></span>

<span data-ttu-id="325e9-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="325e9-138">The following is an example of the response.</span></span>

><span data-ttu-id="325e9-139">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="325e9-139">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="325e9-140">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="325e9-140">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
    "value": [
        {
            "id": "NjRiOWM3NDYtYjE1NS00MDQyLThkNDctOTQxYmQzODE2ODFiIyMwZDgyMGVjZC1kZWYyLTQyOTctYWRhZC03ODA1NmNkZTdjNzg=",
            "teamsAppDefinition": {
                "id": "MGQ4MjBlY2QtZGVmMi00Mjk3LWFkYWQtNzgwNTZjZGU3Yzc4IyMxLjAuMA==",
                "teamsAppId": "0d820ecd-def2-4297-adad-78056cde7c78",
                "displayName": "OneNote",
                "version": "1.0.0"
            }
        },
        {
            "id": "NjRiOWM3NDYtYjE1NS00MDQyLThkNDctOTQxYmQzODE2ODFiIyMwZmQ5MjVhMC0zNTdmLTRkMjUtODQ1Ni1iMzAyMmFhYTQxYTk=",
            "teamsAppDefinition": {
                "id": "MGZkOTI1YTAtMzU3Zi00ZDI1LTg0NTYtYjMwMjJhYWE0MWE5IyMxLjc=",
                "teamsAppId": "0fd925a0-357f-4d25-8456-b3022aaa41a9",
                "displayName": "SurveyMonkey",
                "version": "1.7"
            }
        },
        {
            "id": "NjRiOWM3NDYtYjE1NS00MDQyLThkNDctOTQxYmQzODE2ODFiIyMyYTUyNzcwMy0xZjZmLTQ1NTktYTMzMi1kOGE3ZDI4OGNkODg=",
            "teamsAppDefinition": {
                "id": "MmE1Mjc3MDMtMWY2Zi00NTU5LWEzMzItZDhhN2QyODhjZDg4IyMxLjA=",
                "teamsAppId": "2a527703-1f6f-4559-a332-d8a7d288cd88",
                "displayName": "SharePoint",
                "version": "1.0"
            }
        }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List owners",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->