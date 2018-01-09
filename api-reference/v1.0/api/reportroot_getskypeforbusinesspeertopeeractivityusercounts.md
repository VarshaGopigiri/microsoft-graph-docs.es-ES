# <a name="reportroot-getskypeforbusinesspeertopeeractivityusercounts"></a><span data-ttu-id="9b96f-101">reportRoot: getSkypeForBusinessPeerToPeerActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="9b96f-101">reportRoot: getSkypeForBusinessPeerToPeerActivityUserCounts</span></span>

<span data-ttu-id="9b96f-102">Obtiene tendencias de uso sobre el número de usuarios únicos y el tipo de sesiones de punto a punto realizadas en la organización.</span><span class="sxs-lookup"><span data-stu-id="9b96f-102">Get usage trends on the number of unique users and type of peer-to-peer sessions held in your organization.</span></span> <span data-ttu-id="9b96f-103">Entre los diferentes tipos, se incluyen sesiones de mensajería instantánea, audio, vídeo, uso compartido de aplicaciones y transferencias de archivos en sesiones de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="9b96f-103">Types of sessions include IM, audio, video, application sharing, and file transfers in peer-to-peer sessions.</span></span>

> <span data-ttu-id="9b96f-104">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de punto a punto de Skype Empresarial]((https://support.office.com/client/Skype-for-Business-Online-peertopeer-activity-d3b2d569-4ee9-44b8-92bf-d518142f0713)).</span><span class="sxs-lookup"><span data-stu-id="9b96f-104">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business peer-to-peer activity]((https://support.office.com/client/Skype-for-Business-Online-peertopeer-activity-d3b2d569-4ee9-44b8-92bf-d518142f0713)).</span></span>

## <a name="permissions"></a><span data-ttu-id="9b96f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b96f-105">Permissions</span></span>

<span data-ttu-id="9b96f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9b96f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="9b96f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b96f-108">Permission type</span></span>                        | <span data-ttu-id="9b96f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b96f-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="9b96f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b96f-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="9b96f-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b96f-111">Not supported.</span></span>                           |
| <span data-ttu-id="9b96f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b96f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9b96f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b96f-113">Not supported.</span></span>                           |
| <span data-ttu-id="9b96f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b96f-114">Application</span></span>                            | <span data-ttu-id="9b96f-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="9b96f-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="9b96f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b96f-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessPeerToPeerActivityUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="9b96f-117">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b96f-117">Request parameters</span></span>

<span data-ttu-id="9b96f-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="9b96f-118">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="9b96f-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9b96f-119">Parameter</span></span> | <span data-ttu-id="9b96f-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b96f-120">Type</span></span>   | <span data-ttu-id="9b96f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b96f-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="9b96f-122">period</span><span class="sxs-lookup"><span data-stu-id="9b96f-122">Period</span></span>    | <span data-ttu-id="9b96f-123">cadena</span><span class="sxs-lookup"><span data-stu-id="9b96f-123">string</span></span> | <span data-ttu-id="9b96f-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="9b96f-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="9b96f-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="9b96f-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="9b96f-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="9b96f-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="9b96f-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b96f-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="9b96f-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b96f-128">Request headers</span></span>

| <span data-ttu-id="9b96f-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b96f-129">Name</span></span>          | <span data-ttu-id="9b96f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b96f-130">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="9b96f-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b96f-131">Authorization</span></span> | <span data-ttu-id="9b96f-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b96f-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9b96f-134">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="9b96f-134">if-none-match</span></span> | <span data-ttu-id="9b96f-135">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="9b96f-135">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `304 Not Modified` response is returned.</span></span> <span data-ttu-id="9b96f-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9b96f-136">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="9b96f-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b96f-137">Response</span></span>

<span data-ttu-id="9b96f-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="9b96f-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="9b96f-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b96f-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="9b96f-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="9b96f-140">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

<span data-ttu-id="9b96f-141">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="9b96f-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="9b96f-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="9b96f-142">Report Refresh Date</span></span>
- <span data-ttu-id="9b96f-143">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="9b96f-143">Report Date</span></span>
- <span data-ttu-id="9b96f-144">Período del informe</span><span class="sxs-lookup"><span data-stu-id="9b96f-144">Report Period</span></span>
- <span data-ttu-id="9b96f-145">Mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="9b96f-145">IM Address</span></span>
- <span data-ttu-id="9b96f-146">Audio</span><span class="sxs-lookup"><span data-stu-id="9b96f-146">Audio</span></span>
- <span data-ttu-id="9b96f-147">Vídeo</span><span class="sxs-lookup"><span data-stu-id="9b96f-147">Video</span></span>
- <span data-ttu-id="9b96f-148">Uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9b96f-148">App sharing</span></span>
- <span data-ttu-id="9b96f-149">Transferencia de archivos</span><span class="sxs-lookup"><span data-stu-id="9b96f-149">File Transfer</span></span>

## <a name="example"></a><span data-ttu-id="9b96f-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b96f-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="9b96f-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b96f-151">Request</span></span>

<span data-ttu-id="9b96f-152">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b96f-152">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinesspeertopeeractivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessPeerToPeerActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="9b96f-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b96f-153">Response</span></span>

<span data-ttu-id="9b96f-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b96f-154">Here is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="9b96f-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="9b96f-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,IM,Audio,Video,App Sharing,File Transfer
```
