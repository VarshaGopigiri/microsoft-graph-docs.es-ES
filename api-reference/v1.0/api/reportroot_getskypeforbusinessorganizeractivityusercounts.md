# <a name="reportroot-getskypeforbusinessorganizeractivityusercounts"></a><span data-ttu-id="c0bec-101">reportRoot: getSkypeForBusinessOrganizerActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="c0bec-101">reportRoot: getSkypeForBusinessOrganizerActivityUserCounts</span></span>

<span data-ttu-id="c0bec-102">Obtiene tendencias de uso sobre el número de usuarios únicos y el tipo de sesiones de conferencia realizadas y organizadas por los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="c0bec-102">Get usage trends on the number of unique users and type of conference sessions held and organized by users in your organization.</span></span> <span data-ttu-id="c0bec-103">Entre los tipos de sesiones de conferencia, se incluyen sesiones de mensajería instantánea, audio o vídeo, uso compartido de aplicaciones, web, acceso telefónico local o aceptación de llamada de terceros, y acceso telefónico local o aceptación de llamada de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c0bec-103">Types of conference sessions include IM, audio/video, application sharing, web, dial-in/out - 3rd party, and dial-in/out Microsoft.</span></span>

> <span data-ttu-id="c0bec-104">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de organizador de conferencia de Skype Empresarial]((https://support.office.com/client/Skype-for-Business-Online-conference-organized-activity-03a255d4-0e1d-4b24-b73d-7a62fae36254)).</span><span class="sxs-lookup"><span data-stu-id="c0bec-104">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business conference organizer activity]((https://support.office.com/client/Skype-for-Business-Online-conference-organized-activity-03a255d4-0e1d-4b24-b73d-7a62fae36254)).</span></span>

## <a name="permissions"></a><span data-ttu-id="c0bec-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c0bec-105">Permissions</span></span>

<span data-ttu-id="c0bec-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c0bec-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="c0bec-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c0bec-108">Permission type</span></span>                        | <span data-ttu-id="c0bec-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c0bec-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="c0bec-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c0bec-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="c0bec-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0bec-111">Not supported.</span></span>                           |
| <span data-ttu-id="c0bec-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0bec-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0bec-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0bec-113">Not supported.</span></span>                           |
| <span data-ttu-id="c0bec-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c0bec-114">Application</span></span>                            | <span data-ttu-id="c0bec-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c0bec-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="c0bec-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0bec-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessOrganizerActivityUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="c0bec-117">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0bec-117">Request parameters</span></span>

<span data-ttu-id="c0bec-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="c0bec-118">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="c0bec-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c0bec-119">Parameter</span></span> | <span data-ttu-id="c0bec-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0bec-120">Type</span></span>   | <span data-ttu-id="c0bec-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0bec-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="c0bec-122">period</span><span class="sxs-lookup"><span data-stu-id="c0bec-122">Period</span></span>    | <span data-ttu-id="c0bec-123">cadena</span><span class="sxs-lookup"><span data-stu-id="c0bec-123">string</span></span> | <span data-ttu-id="c0bec-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c0bec-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="c0bec-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="c0bec-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="c0bec-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c0bec-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="c0bec-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0bec-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="c0bec-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0bec-128">Request headers</span></span>

| <span data-ttu-id="c0bec-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="c0bec-129">Name</span></span>          | <span data-ttu-id="c0bec-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0bec-130">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="c0bec-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="c0bec-131">Authorization</span></span> | <span data-ttu-id="c0bec-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0bec-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c0bec-134">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="c0bec-134">if-none-match</span></span> | <span data-ttu-id="c0bec-135">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="c0bec-135">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `304 Not Modified` response is returned.</span></span> <span data-ttu-id="c0bec-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c0bec-136">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="c0bec-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0bec-137">Response</span></span>

<span data-ttu-id="c0bec-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="c0bec-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="c0bec-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0bec-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="c0bec-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="c0bec-140">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

<span data-ttu-id="c0bec-141">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="c0bec-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="c0bec-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="c0bec-142">Report Refresh Date</span></span>
- <span data-ttu-id="c0bec-143">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="c0bec-143">Report Date</span></span>
- <span data-ttu-id="c0bec-144">Período del informe</span><span class="sxs-lookup"><span data-stu-id="c0bec-144">Report Period</span></span>
- <span data-ttu-id="c0bec-145">Mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="c0bec-145">IM Address</span></span>
- <span data-ttu-id="c0bec-146">Audio o vídeo</span><span class="sxs-lookup"><span data-stu-id="c0bec-146">Audio/Video</span></span>
- <span data-ttu-id="c0bec-147">Uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c0bec-147">App sharing</span></span>
- <span data-ttu-id="c0bec-148">Web</span><span class="sxs-lookup"><span data-stu-id="c0bec-148">Web</span></span>
- <span data-ttu-id="c0bec-149">Acceso telefónico local o aceptación de llamada de terceros</span><span class="sxs-lookup"><span data-stu-id="c0bec-149">Dial-in/out 3rd Party</span></span>
- <span data-ttu-id="c0bec-150">Acceso telefónico local o aceptación de llamada de Microsoft</span><span class="sxs-lookup"><span data-stu-id="c0bec-150">Dial-in/out Microsoft</span></span>

## <a name="example"></a><span data-ttu-id="c0bec-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0bec-151">Example</span></span>

#### <a name="request"></a><span data-ttu-id="c0bec-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c0bec-152">Request</span></span>

<span data-ttu-id="c0bec-153">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0bec-153">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessorganizeractivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessOrganizerActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="c0bec-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0bec-154">Response</span></span>

<span data-ttu-id="c0bec-155">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0bec-155">Here is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="c0bec-156">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="c0bec-156">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,IM,Audio/Video,App Sharing,Web,Dial-in/out 3rd Party,Dial-in/out Microsoft
```
