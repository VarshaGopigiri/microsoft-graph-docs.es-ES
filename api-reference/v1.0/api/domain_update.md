# <a name="update-domain"></a><span data-ttu-id="a4af4-101">Actualizar dominio</span><span class="sxs-lookup"><span data-stu-id="a4af4-101">Update domain</span></span>

<span data-ttu-id="a4af4-102">Actualiza las propiedades del objeto del dominio.</span><span class="sxs-lookup"><span data-stu-id="a4af4-102">Update the properties of domain object.</span></span>

> <span data-ttu-id="a4af4-103">**Importante:** Solo se pueden actualizar los dominios verificados.</span><span class="sxs-lookup"><span data-stu-id="a4af4-103">**Important:** Only verified domains can be updated.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a4af4-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a4af4-104">Prerequisites</span></span>

<span data-ttu-id="a4af4-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Domain.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="a4af4-105">One of the following **scopes** is required to execute this API: *Domain.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="a4af4-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4af4-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /domains/{id}
```

> <span data-ttu-id="a4af4-107">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="a4af4-107">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a4af4-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4af4-108">Request headers</span></span>

| <span data-ttu-id="a4af4-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="a4af4-109">Name</span></span>       | <span data-ttu-id="a4af4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4af4-110">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="a4af4-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="a4af4-111">Authorization</span></span>  | <span data-ttu-id="a4af4-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a4af4-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a4af4-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a4af4-114">Content-Type</span></span>  | <span data-ttu-id="a4af4-115">application/json</span><span class="sxs-lookup"><span data-stu-id="a4af4-115">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="a4af4-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a4af4-116">Request body</span></span>

<span data-ttu-id="a4af4-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que quiera actualizar. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud conservarán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para un rendimiento óptimo, incluya solo los valores modificados.</span><span class="sxs-lookup"><span data-stu-id="a4af4-p102">In the request body, supply the values for relevant fields to be updated. Existing properties not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance, only include changed values.</span></span>

## <a name="response"></a><span data-ttu-id="a4af4-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4af4-120">Response</span></span>

<span data-ttu-id="a4af4-121">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`, pero no el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4af4-121">If successful, this method returns a `204 No Content` response code and no response body.</span></span>

## <a name="example"></a><span data-ttu-id="a4af4-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4af4-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a4af4-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4af4-123">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_domain"
}-->
```http
PATCH https://graph.microsoft.com/V1.0/domains/contoso.com
Content-type: application/json

{
  "isDefault": true,
  "supportedServices": [
    "Email",
    "OfficeCommunicationsOnline"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="a4af4-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4af4-124">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.domain"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update domain",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->