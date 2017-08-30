# <a name="filter-apply"></a><span data-ttu-id="1b433-101">Filter: apply</span><span class="sxs-lookup"><span data-stu-id="1b433-101">Filter: apply</span></span>

<span data-ttu-id="1b433-102">Aplicar los criterios de filtro especificados en la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="1b433-102">Apply the given filter criteria on the given column.</span></span>
## <a name="permissions"></a><span data-ttu-id="1b433-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="1b433-103">Permissions</span></span>
<span data-ttu-id="1b433-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1b433-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1b433-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1b433-106">Permission type</span></span>      | <span data-ttu-id="1b433-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1b433-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1b433-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1b433-108">Delegated (work or school account)</span></span> | <span data-ttu-id="1b433-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1b433-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1b433-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1b433-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1b433-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b433-111">Not supported.</span></span>    |
|<span data-ttu-id="1b433-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1b433-112">Application</span></span> | <span data-ttu-id="1b433-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b433-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1b433-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1b433-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/filter/apply
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/filter/apply

```
## <a name="request-headers"></a><span data-ttu-id="1b433-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b433-115">Request headers</span></span>
| <span data-ttu-id="1b433-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="1b433-116">Name</span></span>       | <span data-ttu-id="1b433-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b433-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1b433-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="1b433-118">Authorization</span></span>  | <span data-ttu-id="1b433-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1b433-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1b433-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1b433-121">Request body</span></span>
<span data-ttu-id="1b433-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="1b433-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="1b433-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1b433-123">Parameter</span></span>    | <span data-ttu-id="1b433-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b433-124">Type</span></span>   |<span data-ttu-id="1b433-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b433-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1b433-126">criterios</span><span class="sxs-lookup"><span data-stu-id="1b433-126">criteria</span></span>|<span data-ttu-id="1b433-127">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="1b433-127">FilterCriteria</span></span>|<span data-ttu-id="1b433-128">Criterios que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="1b433-128">The criteria to apply.</span></span>|

## <a name="response"></a><span data-ttu-id="1b433-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b433-129">Response</span></span>

<span data-ttu-id="1b433-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b433-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1b433-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b433-132">Example</span></span>
<span data-ttu-id="1b433-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="1b433-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="1b433-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b433-134">Request</span></span>
<span data-ttu-id="1b433-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1b433-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "filter_apply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/filter/apply
Content-type: application/json
Content-length: 321

{
  "criteria": {
    "criterion1": "criterion1-value",
    "criterion2": "criterion2-value",
    "color": "color-value",
    "operator": {
    },
    "icon": {
      "set": "set-value",
      "index": 99
    },
    "dynamicCriteria": "dynamicCriteria-value",
    "values": {
    },
    "filterOn": "filterOn-value"
  }
}
```

##### <a name="response"></a><span data-ttu-id="1b433-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b433-136">Response</span></span>
<span data-ttu-id="1b433-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b433-137">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Filter: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->