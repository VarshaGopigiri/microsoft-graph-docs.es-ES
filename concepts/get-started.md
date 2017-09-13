# <a name="getting-started-building-microsoft-graph-apps"></a>Introducción a la compilación de aplicaciones de Microsoft Graph

En los artículos de esta sección, se proporcionan instrucciones detalladas acerca de cómo compilar aplicaciones que se conecten a Microsoft Graph en una variedad de lenguajes y plataformas de desarrollo. Cada artículo empieza con un proyecto inicial de ejemplo para la plataforma apropiada y le guía por el proceso de agregar funcionalidad que autentique el usuario. Además, realiza una solicitud de ejemplo para que Microsoft Graph envíe un correo electrónico desde su cuenta. El proyecto completado es idéntico al [ejemplo Connect del repositorio de Microsoft Graph](https://github.com/microsoftgraph?utf8=%E2%9C%93&query=connect) de esa plataforma.

Elija el artículo que trate sobre el proveedor de autenticación y la plataforma de desarrollo que desee y empiece a conectarse a Microsoft Graph. Para obtener más información, consulte [¿Qué hay diferente en el punto de conexión v2.0?](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-v2-compare)

Puede seguir los pasos del artículo que trate sobre la plataforma de desarrollo que desee o, para poner en funcionamiento rápidamente una solución de trabajo, pruebe la experiencia de [inicio rápido](https://developer.microsoft.com/graph/quick-start).

Para explorar los ejemplos de conexión terminados, visite [Microsoft Graph](https://github.com/microsoftgraph) en GitHub. En la siguiente tabla, se enumeran los ejemplos por proveedor de autenticación y plataforma y se muestra una nota para indicar si se conectan a Microsoft Graph mediante REST o una biblioteca cliente de Microsoft Graph.

<table>
  <tr>
    <th>Plataforma</th>
    <th>Punto de conexión de Azure AD</th> 
    <th>Punto de conexión v2.0 de Azure AD</th>
  </tr>
  <tr>
    <td>Android</td>
    <td>
        <a href="https://github.com/microsoftgraph/android-java-connect-sample/tree/last_v1_auth">Ejemplo de SDK</a>
    </td> 
        <td>
                <a href="https://github.com/microsoftgraph/android-java-connect-sample">Ejemplo de SDK</a> o ¶<a href="https://github.com/microsoftgraph/android-java-connect-rest-sample">Ejemplo de REST</a>
    </td> 
  </tr>
  <tr>
    <td>AngularJS</td>
    <td>
        <a href="https://github.com/microsoftgraph/angular-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a>
    </td> 
        <td>
        <a href="https://github.com/microsoftgraph/angular-connect-sample">Ejemplo de SDK</a> o ¶<a href="https://github.com/microsoftgraph/angular-connect-rest-sample">Ejemplo de REST</a>
    </td> 
  </tr>
  <tr>
    <td>ASP.NET</td>
    <td>
        <a href="https://github.com/microsoftgraph/aspnet-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a>
    </td>     
    <td>
        <a href="https://github.com/microsoftgraph/aspnet-connect-sample">Ejemplo de SDK</a> o ¶<a href="https://github.com/microsoftgraph/aspnet-connect-rest-sample">Ejemplo de REST</a>
    </td> 
  </tr>
  <tr>
    <td>iOS (Obj-C)</td>
    <td>
        <a href="https://github.com/microsoftgraph/ios-objectivec-connect-rest-sample">Ejemplo de REST</a>
    </td>     
    <td>
        <a href="https://github.com/microsoftgraph/ios-objectivec-connect-sample">Ejemplo de SDK</a>
    </td> 
  </tr>
  <tr>
    <td>iOS (Swift)</td>
    <td>
        <a href="https://github.com/microsoftgraph/ios-swift-connect-rest-sample">Ejemplo de REST</a>
    </td>     
    <td>
        <a href="https://github.com/microsoftgraph/ios-swift-connect-sample">Ejemplo de SDK</a>
    </td> 
  </tr>
  <tr>
    <td>NodeJS</td>
    <td>
        <a href="https://github.com/microsoftgraph/nodejs-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a>
    </td>     
    <td>    
        <a href="https://github.com/microsoftgraph/nodejs-connect-sample">Ejemplo de SDK</a> o <a href="https://github.com/microsoftgraph/nodejs-connect-rest-sample">Ejemplo de REST</a>
    </td> 
  </tr>
  <tr>
    <td>PHP</td>
    <td>
        <a href="https://github.com/microsoftgraph/php-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a>
    </td>     
    <td>
            <a href="https://github.com/microsoftgraph/php-connect-sample">Ejemplo de SDK</a> o ¶<a href="https://github.com/microsoftgraph/php-connect-rest-sample">Ejemplo de REST</a>
    </td> 
  </tr>
  <tr>
    <td>Python</td>
    <td>
        <a href="https://github.com/microsoftgraph/python3-connect-rest-sample">Ejemplo de REST</a>
    </td>     
    <td>
    </td> 
  </tr>
  <tr>
    <td>Ruby</td>
    <td>
        <a href="https://github.com/microsoftgraph/ruby-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a>
    </td>     
    <td>
        <a href="https://github.com/microsoftgraph/ruby-connect-rest-sample">Ejemplo de REST</a>
    </td> 
  </tr>
  <tr>
    <td>UWP</td>
    <td>
        <a href="https://github.com/microsoftgraph/uwp-csharp-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a>
    </td>     
    <td>
        <a href="https://github.com/microsoftgraph/uwp-csharp-connect-sample">Ejemplo de SDK</a> o ¶<a href="https://github.com/microsoftgraph/uwp-csharp-connect-rest-sample">Ejemplo de REST</a>
    </td> 
  </tr>
  <tr>
    <td>Xamarin</td>
    <td>
    </td>     
    <td>
        <a href="https://github.com/microsoftgraph/xamarin-csharp-connect-sample">Ejemplo de SDK</a>
    </td> 
  </tr>
</table>

## <a name="see-also"></a>Recursos adicionales

- Pruebe llamadas de REST de ejemplo en nuestro [Explorador de API](https://graph.microsoft.io/graph-explorer).
- [Documentación acerca del punto de conexión de Azure AD](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-developers-guide)
- [Documentación acerca del punto de conexión v2.0 de Azure AD](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-appmodel-v2-overview)
