# <a name="update-organization"></a><span data-ttu-id="f3def-101">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="f3def-101">Update organization</span></span>

<span data-ttu-id="f3def-102">Actualice las propiedades de la organización autenticada actualmente.</span><span class="sxs-lookup"><span data-stu-id="f3def-102">Update the properties of the currently authenticated organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="f3def-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="f3def-103">Permissions</span></span>

<span data-ttu-id="f3def-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f3def-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f3def-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f3def-106">Permission type</span></span> | <span data-ttu-id="f3def-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f3def-107">Permissions (from least to most privileged)</span></span> |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f3def-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f3def-108">Delegated (work or school account)</span></span> | <span data-ttu-id="f3def-109">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f3def-109">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f3def-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f3def-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f3def-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3def-111">Not supported.</span></span>    |
|<span data-ttu-id="f3def-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f3def-112">Application</span></span> | <span data-ttu-id="f3def-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3def-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f3def-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f3def-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /organization

```

## <a name="request-headers"></a><span data-ttu-id="f3def-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f3def-115">Request headers</span></span>

| <span data-ttu-id="f3def-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="f3def-116">Name</span></span>       | <span data-ttu-id="f3def-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3def-117">Type</span></span> | <span data-ttu-id="f3def-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3def-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="f3def-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f3def-119">Authorization</span></span>  | <span data-ttu-id="f3def-120">string</span><span class="sxs-lookup"><span data-stu-id="f3def-120">string</span></span>  | <span data-ttu-id="f3def-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f3def-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f3def-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="f3def-123">Request body</span></span>
<span data-ttu-id="f3def-124">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="f3def-124">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="f3def-125">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f3def-125">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="f3def-126">Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="f3def-126">For best performance, you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="f3def-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3def-127">Property</span></span>     | <span data-ttu-id="f3def-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3def-128">Type</span></span>   |<span data-ttu-id="f3def-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3def-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f3def-130">marketingNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="f3def-130">marketingNotificationEmails</span></span>|<span data-ttu-id="f3def-131">Colección String</span><span class="sxs-lookup"><span data-stu-id="f3def-131">String collection</span></span>|                                        <span data-ttu-id="f3def-132">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="f3def-132">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="f3def-133">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="f3def-133">privacyProfile</span></span>|[<span data-ttu-id="f3def-134">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="f3def-134">privacyProfile</span></span>](../resources/privacyprofile.md)|<span data-ttu-id="f3def-135">Perfil de privacidad de una organización (establecer statementUrl y contactEmail).</span><span class="sxs-lookup"><span data-stu-id="f3def-135">The privacy profile of an organization (set statementUrl and contactEmail).</span></span>            |
|<span data-ttu-id="f3def-136">securityComplianceNotificationMails</span><span class="sxs-lookup"><span data-stu-id="f3def-136">securityComplianceNotificationMails</span></span>|<span data-ttu-id="f3def-137">Colección String</span><span class="sxs-lookup"><span data-stu-id="f3def-137">String collection</span></span>||
|<span data-ttu-id="f3def-138">securityComplianceNotificationPhones</span><span class="sxs-lookup"><span data-stu-id="f3def-138">securityComplianceNotificationPhones</span></span>|<span data-ttu-id="f3def-139">Colección String</span><span class="sxs-lookup"><span data-stu-id="f3def-139">String collection</span></span>||
|<span data-ttu-id="f3def-140">technicalNotificationMails</span><span class="sxs-lookup"><span data-stu-id="f3def-140">technicalNotificationMails</span></span>|<span data-ttu-id="f3def-141">Colección String</span><span class="sxs-lookup"><span data-stu-id="f3def-141">String collection</span></span>|                                        <span data-ttu-id="f3def-142">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="f3def-142">**Notes**: not nullable.</span></span>            |

## <a name="response"></a><span data-ttu-id="f3def-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3def-143">Response</span></span>

<span data-ttu-id="f3def-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f3def-144">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f3def-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3def-145">Example</span></span>

### <a name="request"></a><span data-ttu-id="f3def-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3def-146">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_organization"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/organization
Content-type: application/json
Content-length: 411

{
  "marketingNotificationEmails" : ["marketing@contoso.com"],
  "privacyProfile" :
    {
      "contactEmail":"alice@contoso.com",
      "statementUrl":"https://contoso.com/privacyStatement"
    },
  "securityComplianceNotificationMails" : ["security@contoso.com"],
  "securityComplianceNotificationPhones" : ["(123) 456-7890"],
  "technicalNotificationMails" : ["tech@contoso.com"]
}
```

### <a name="response"></a><span data-ttu-id="f3def-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3def-147">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization"
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
