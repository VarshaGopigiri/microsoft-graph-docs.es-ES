# <a name="reportroot-getskypeforbusinessdeviceusageusercounts"></a><span data-ttu-id="ac728-101">reportRoot: getSkypeForBusinessDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="ac728-101">reportRoot: getSkypeForBusinessDeviceUsageUserCounts</span></span>

<span data-ttu-id="ac728-102">Obtiene las tendencias de uso sobre el número de usuarios de la organización que se conectaron con la aplicación de Skype Empresarial.</span><span class="sxs-lookup"><span data-stu-id="ac728-102">Get the usage trends on how many users in your organization have connected using the Skype for Business app.</span></span> <span data-ttu-id="ac728-103">También obtendrá un desglose por el tipo de dispositivo (Windows, teléfono Windows, teléfono Android, iPhone o iPad) donde se instaló y se usó la aplicación cliente de Skype Empresarial en la organización.</span><span class="sxs-lookup"><span data-stu-id="ac728-103">You will also get a breakdown by the type of device (Windows, Windows phone, Android phone, iPhone, or iPad) on which the Skype for Business client app is installed and used across your organization.</span></span>

> <span data-ttu-id="ac728-104">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Clientes usados de Skype Empresarial](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span><span class="sxs-lookup"><span data-stu-id="ac728-104">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business clients used](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span></span>

## <a name="permissions"></a><span data-ttu-id="ac728-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ac728-105">Permissions</span></span>

<span data-ttu-id="ac728-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ac728-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="ac728-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ac728-108">Permission type</span></span>                        | <span data-ttu-id="ac728-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ac728-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="ac728-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ac728-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="ac728-111">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ac728-111">Reports.Read.All</span></span>                         |
| <span data-ttu-id="ac728-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ac728-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ac728-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac728-113">Not supported.</span></span>                           |
| <span data-ttu-id="ac728-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ac728-114">Application</span></span>                            | <span data-ttu-id="ac728-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ac728-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="ac728-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ac728-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessDeviceUsageUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="ac728-117">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ac728-117">Request parameters</span></span>

<span data-ttu-id="ac728-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="ac728-118">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="ac728-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac728-119">Parameter</span></span> | <span data-ttu-id="ac728-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac728-120">Type</span></span>   | <span data-ttu-id="ac728-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac728-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="ac728-122">period</span><span class="sxs-lookup"><span data-stu-id="ac728-122">period</span></span>    | <span data-ttu-id="ac728-123">cadena</span><span class="sxs-lookup"><span data-stu-id="ac728-123">string</span></span> | <span data-ttu-id="ac728-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ac728-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="ac728-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="ac728-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="ac728-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ac728-126">These values follow the format D   where    represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="ac728-127">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ac728-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="ac728-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ac728-128">Request headers</span></span>

| <span data-ttu-id="ac728-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac728-129">Name</span></span>          | <span data-ttu-id="ac728-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac728-130">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="ac728-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="ac728-131">Authorization</span></span> | <span data-ttu-id="ac728-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ac728-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="ac728-134">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="ac728-134">If-None-Match</span></span> | <span data-ttu-id="ac728-135">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="ac728-135">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="ac728-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ac728-136">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="ac728-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac728-137">Response</span></span>

<span data-ttu-id="ac728-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="ac728-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="ac728-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac728-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="ac728-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="ac728-140">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="ac728-141">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="ac728-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="ac728-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="ac728-142">Report Refresh Date</span></span>
- <span data-ttu-id="ac728-143">Windows</span><span class="sxs-lookup"><span data-stu-id="ac728-143">Windows</span></span>
- <span data-ttu-id="ac728-144">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="ac728-144">Windows Phone</span></span>
- <span data-ttu-id="ac728-145">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="ac728-145">Android Phone</span></span>
- <span data-ttu-id="ac728-146">iPhone</span><span class="sxs-lookup"><span data-stu-id="ac728-146">iPhone</span></span>
- <span data-ttu-id="ac728-147">iPad</span><span class="sxs-lookup"><span data-stu-id="ac728-147">iPad</span></span>
- <span data-ttu-id="ac728-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="ac728-148">Report Date</span></span>
- <span data-ttu-id="ac728-149">Período del informe</span><span class="sxs-lookup"><span data-stu-id="ac728-149">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="ac728-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac728-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="ac728-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ac728-151">Request</span></span>

<span data-ttu-id="ac728-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ac728-152">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessdeviceusageusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessDeviceUsageUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="ac728-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac728-153">Response</span></span>

<span data-ttu-id="ac728-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac728-154">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="ac728-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="ac728-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Windows,Windows Phone,Android Phone,iPhone,iPad,Report Date,Report Period
```
