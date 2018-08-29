# <a name="reportroot-getoffice365activationsusercounts"></a><span data-ttu-id="2ace7-101">reportRoot: getOffice365ActivationsUserCounts</span><span class="sxs-lookup"><span data-stu-id="2ace7-101">reportRoot: getOffice365ActivationsUserCounts</span></span>

<span data-ttu-id="2ace7-102">Obtiene el número de usuarios habilitados y el número de usuarios que activaron la suscripción de Office en dispositivos o equipos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="2ace7-102">Get the count of users that are enabled and those that have activated the Office subscription on desktop or devices.</span></span>

> <span data-ttu-id="2ace7-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Activaciones de Microsoft Office](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span><span class="sxs-lookup"><span data-stu-id="2ace7-103">**Note:** For details about different report views and names, see [Office 365 Reports - Microsoft Office activations](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span></span>

## <a name="permissions"></a><span data-ttu-id="2ace7-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="2ace7-104">Permissions</span></span>

<span data-ttu-id="2ace7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2ace7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="2ace7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2ace7-107">Permission type</span></span>                        | <span data-ttu-id="2ace7-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2ace7-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="2ace7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2ace7-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="2ace7-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="2ace7-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="2ace7-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2ace7-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2ace7-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ace7-112">Not supported.</span></span>                           |
| <span data-ttu-id="2ace7-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2ace7-113">Application</span></span>                            | <span data-ttu-id="2ace7-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="2ace7-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="2ace7-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ace7-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActivationsUserCounts
```

## <a name="request-headers"></a><span data-ttu-id="2ace7-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ace7-116">Request headers</span></span>

| <span data-ttu-id="2ace7-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ace7-117">Name</span></span>          | <span data-ttu-id="2ace7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ace7-118">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="2ace7-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="2ace7-119">Authorization</span></span> | <span data-ttu-id="2ace7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2ace7-p102">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="2ace7-122">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="2ace7-122">If-None-Match</span></span> | <span data-ttu-id="2ace7-123">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="2ace7-123">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="2ace7-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2ace7-124">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="2ace7-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ace7-125">Response</span></span>

<span data-ttu-id="2ace7-126">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="2ace7-126">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="2ace7-127">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ace7-127">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="2ace7-128">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="2ace7-128">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="2ace7-129">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="2ace7-129">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="2ace7-130">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="2ace7-130">Report Refresh Date</span></span>
- <span data-ttu-id="2ace7-131">Tipo de producto</span><span class="sxs-lookup"><span data-stu-id="2ace7-131">Product Type</span></span>
- <span data-ttu-id="2ace7-132">Asignado</span><span class="sxs-lookup"><span data-stu-id="2ace7-132">Assigned</span></span>
- <span data-ttu-id="2ace7-133">Activado</span><span class="sxs-lookup"><span data-stu-id="2ace7-133">Activated</span></span>

## <a name="example"></a><span data-ttu-id="2ace7-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ace7-134">Example</span></span>

#### <a name="request"></a><span data-ttu-id="2ace7-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ace7-135">Request</span></span>

<span data-ttu-id="2ace7-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2ace7-136">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activationsusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActivationsUserCounts
```

#### <a name="response"></a><span data-ttu-id="2ace7-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ace7-137">Response</span></span>

<span data-ttu-id="2ace7-138">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ace7-138">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="2ace7-139">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="2ace7-139">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Product Type,Assigned,Activated
```
