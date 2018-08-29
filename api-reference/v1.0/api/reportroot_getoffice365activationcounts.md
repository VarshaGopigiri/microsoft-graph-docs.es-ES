# <a name="reportroot-getoffice365activationcounts"></a><span data-ttu-id="29e2a-101">reportRoot: getOffice365ActivationCounts</span><span class="sxs-lookup"><span data-stu-id="29e2a-101">reportRoot: getOffice365ActivationCounts</span></span>

<span data-ttu-id="29e2a-102">Obtiene el número de activaciones de Office 365 en dispositivos y equipos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="29e2a-102">Get the count of Office 365 activations on desktops and devices.</span></span>

> <span data-ttu-id="29e2a-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Activaciones de Microsoft Office](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span><span class="sxs-lookup"><span data-stu-id="29e2a-103">**Note:** For details about different report views and names, see [Office 365 Reports - Microsoft Office activations](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span></span>

## <a name="permissions"></a><span data-ttu-id="29e2a-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="29e2a-104">Permissions</span></span>

<span data-ttu-id="29e2a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="29e2a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="29e2a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="29e2a-107">Permission type</span></span>                        | <span data-ttu-id="29e2a-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="29e2a-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="29e2a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="29e2a-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="29e2a-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="29e2a-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="29e2a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="29e2a-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="29e2a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="29e2a-112">Not supported.</span></span>                           |
| <span data-ttu-id="29e2a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="29e2a-113">Application</span></span>                            | <span data-ttu-id="29e2a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="29e2a-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="29e2a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="29e2a-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActivationCounts
```

## <a name="request-headers"></a><span data-ttu-id="29e2a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="29e2a-116">Request headers</span></span>

| <span data-ttu-id="29e2a-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="29e2a-117">Name</span></span>          | <span data-ttu-id="29e2a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="29e2a-118">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="29e2a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="29e2a-119">Authorization</span></span> | <span data-ttu-id="29e2a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="29e2a-p102">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="29e2a-122">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="29e2a-122">If-None-Match</span></span> | <span data-ttu-id="29e2a-123">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="29e2a-123">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="29e2a-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="29e2a-124">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="29e2a-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29e2a-125">Response</span></span>

<span data-ttu-id="29e2a-126">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="29e2a-126">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="29e2a-127">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="29e2a-127">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="29e2a-128">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="29e2a-128">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="29e2a-129">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="29e2a-129">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="29e2a-130">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="29e2a-130">Report Refresh Date</span></span>
- <span data-ttu-id="29e2a-131">Tipo de producto</span><span class="sxs-lookup"><span data-stu-id="29e2a-131">Product Type</span></span>
- <span data-ttu-id="29e2a-132">Windows</span><span class="sxs-lookup"><span data-stu-id="29e2a-132">Windows</span></span>
- <span data-ttu-id="29e2a-133">Mac</span><span class="sxs-lookup"><span data-stu-id="29e2a-133">Mac</span></span>
- <span data-ttu-id="29e2a-134">Android</span><span class="sxs-lookup"><span data-stu-id="29e2a-134">Android</span></span>
- <span data-ttu-id="29e2a-135">iOS</span><span class="sxs-lookup"><span data-stu-id="29e2a-135">iOS</span></span>
- <span data-ttu-id="29e2a-136">Windows 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="29e2a-136">Windows 10 Mobile</span></span>

## <a name="example"></a><span data-ttu-id="29e2a-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="29e2a-137">Example</span></span>

#### <a name="request"></a><span data-ttu-id="29e2a-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="29e2a-138">Request</span></span>

<span data-ttu-id="29e2a-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="29e2a-139">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activationcounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActivationCounts
```

#### <a name="response"></a><span data-ttu-id="29e2a-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29e2a-140">Response</span></span>

<span data-ttu-id="29e2a-141">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="29e2a-141">The following is an example of the response.</span></span>

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

<span data-ttu-id="29e2a-142">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="29e2a-142">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Product Type,Windows,Mac,Android,iOS,Windows 10 Mobile
```
