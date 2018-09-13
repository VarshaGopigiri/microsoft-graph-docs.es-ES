# <a name="firewallcertificaterevocationlistcheckmethodtype-enum-type"></a>Tipo de enumeración firewallCertificateRevocationListCheckMethodType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para firewallCertificateRevocationListCheckMethod
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|No hay ningún valor configurado por Intune, no invalidar el valor predeterminado del dispositivo configurado por el usuario|
|none|1|No comprobar la lista de revocación de certificados|
|attempt|2|Intentar la comprobación de CRL y permitir un certificado solo si el certificado se confirma mediante la comprobación|
|require|2|Requerir una comprobación de CRL correcta antes de permitir un certificado|








