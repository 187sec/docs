---
title: Autenticación en GitHub
shortTitle: Authentication
intro: 'Puedes acceder de forma segura a los recursos de tu cuenta en {% data variables.product.prodname_desktop %} si te autenticas con {% data variables.product.prodname_dotcom %}.'
redirect_from:
  - /desktop/getting-started-with-github-desktop/authenticating-to-github-using-the-browser
  - /desktop/getting-started-with-github-desktop/authenticating-to-github
  - /desktop/installing-and-configuring-github-desktop/authenticating-to-github
versions:
  fpt: '*'
ms.openlocfilehash: e88d59a03d876b23d8eb72aae7324db64981096f
ms.sourcegitcommit: 47bd0e48c7dba1dde49baff60bc1eddc91ab10c5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/05/2022
ms.locfileid: '145117354'
---
## Acerca de la autenticación

Para mantener la seguridad de tu cuenta, debes autenticarte antes de que puedas utilizar {% data variables.product.prodname_desktop %} para acceder a los recursos en {% data variables.product.prodname_dotcom %}.

Antes de realizar la autenticación, {% data reusables.desktop.get-an-account %}

{% mac %}

## Autenticar una cuenta en {% data variables.product.prodname_dotcom %}

{% data reusables.desktop.mac-select-desktop-menu %} {% data reusables.desktop.mac-select-accounts %}
3. A la derecha de "{% data variables.product.prodname_dotcom_the_website %}", haga clic en **Sign In**.
  ![El botón Iniciar sesión de GitHub](/assets/images/help/desktop/mac-sign-in-github.png) {% data reusables.desktop.sign-in-browser %}


{% data reusables.desktop.authenticate-in-browser %} {% data reusables.desktop.2fa-in-browser %}
7. Después de que {% data variables.product.prodname_dotcom %} autentique tu cuenta, sigue las indicaciones para regresar a {% data variables.product.prodname_desktop %}.

## Autenticación de una cuenta en {% data variables.product.prodname_ghe_server %}


{% data reusables.desktop.mac-select-desktop-menu %} {% data reusables.desktop.mac-select-accounts %} {% data reusables.desktop.choose-product-authenticate %}
4. Para agregar una cuenta en {% data variables.product.product_location_enterprise %}, escribe la dirección URL de la instancia en "Dirección de empresa" y, luego, haz clic en **Continuar**.
  ![El botón Iniciar sesión de GitHub Enterprise](/assets/images/help/desktop/mac-sign-in-button-enterprise.png) {% data reusables.desktop.sign-in-browser %}
1. Para autenticarte en la cuenta de {% data variables.product.product_location_enterprise %}, escribe las credenciales de tu cuenta y haz clic en **Iniciar sesión**.
  ![El botón Iniciar sesión de {% data variables.product.prodname_ghe_server %} en el explorador](/assets/images/help/desktop/enterprise-sign-in-button-browser.png)

  Como alternativa, si ya hubieras iniciado sesión en la cuenta de {% data variables.product.product_location_enterprise %}, sigue los mensajes para volver a {% data variables.product.prodname_desktop %} y terminar de autenticarte. 

{% endmac %}

{% windows %}

## Autenticar una cuenta en {% data variables.product.prodname_dotcom %}

{% data reusables.desktop.windows-choose-options %} {% data reusables.desktop.windows-select-accounts %}
3. A la derecha de "GitHub.com", haga clic en **Sign in**.
  ![El botón Iniciar sesión de GitHub](/assets/images/help/desktop/windows-sign-in-github.png) {% data reusables.desktop.sign-in-browser %}

  {% data reusables.user-settings.password-authentication-deprecation-desktop %}

{% data reusables.desktop.authenticate-in-browser %} {% data reusables.desktop.2fa-in-browser %}
7. Después de que {% data variables.product.prodname_dotcom %} autentique tu cuenta, sigue las indicaciones para regresar a {% data variables.product.prodname_desktop %}.

## Autenticar una cuenta en {% data variables.product.prodname_enterprise %}


{% data reusables.desktop.windows-choose-options %} {% data reusables.desktop.windows-select-accounts %} {% data reusables.desktop.choose-product-authenticate %}
4. Para agregar una cuenta de {% data variables.product.prodname_enterprise %}, escribe tus credenciales en "Dirección de empresa" y haz clic en **Continuar**.
  ![El botón Sign in en GitHub Enterprise](/assets/images/help/desktop/windows-sign-in-button-enterprise.png) {% data reusables.desktop.retrieve-2fa %}

{% endwindows %}

## Solución de problemas de autenticación

Si {% data variables.product.prodname_desktop %} encuentra un error de autenticación, puedes utilizar los mensajes de error para solucionar los problemas.

Si te encuentras con un error de autenticación, primero intenta salir y entrar nuevamente a tu cuenta en {% data variables.product.prodname_desktop %}.

En el caso de algunos errores, {% data variables.product.prodname_desktop %} te solicitará que indiques el mensaje de error. Si no se te solicita esto, o si quieres encontrar información adicional sobre cualquier error, consulta los archivos de bitácora de {% data variables.product.prodname_desktop %} siguiendo estos pasos.

{% mac %}

1. Use el menú desplegable **Help** y haga clic en **Show Logs in Finder**.
  ![El botón Show Logs en Finder](/assets/images/help/desktop/mac-show-logs.png)
2. Selecciona el archivo de bitácora desde la fecha en donde encontraste el error de autenticación.

{% endmac %}

{% windows %}

1. Use el menú desplegable **Help** y haga clic en **Show Logs in Explorer**.
  ![El botón Show Logs en Explorer](/assets/images/help/desktop/windows-show-logs.png)
2. Selecciona el archivo de bitácora desde la fecha en donde encontraste el error de autenticación.

{% endwindows %}

Revisa la información de solución de problemas que se muestra a continuación dependiendo del error con el que te hayas encontrado.

### Credenciales incorrectas

```shell
Error: Bad credentials
```

Este error significa que hay un problema con las credenciales almacenadas de tu cuenta.

Para solucionar este problema, sal de tu cuenta en {% data variables.product.prodname_desktop %} y vuelve a firmarte.

### Token vacío

```shell
info: [ui] [AppStore.withAuthenticatingUser] account found for repository: node - <username> (empty token)
```

Este error significa que {% data variables.product.prodname_desktop %} no puede encontrar el token de acceso que creó en la cadena de llaves del sistema.

Para solucionar este problema, sal de tu cuenta en {% data variables.product.prodname_desktop %} y vuelve a firmarte.

### No se encuentra el repositorio

```shell
fatal: repository 'https://github.com/<user>/<repo>.git' not found

(The error was parsed as 8: The repository does not seem to exist anymore. You may not have access, or it may have been deleted or renamed.)
```

Este error significa que no tienes permiso para acceder al repositorio que estás intentando clonar.

Para solucionar los problemas, contacta a la persona que administre los permisos en tu organización.

### No se pudo leer del repositorio remoto

```shell
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights and the repository exists.
```

Este error significa que no tienes una llave SSH válida configurada.

Para solucionar problemas, consulte "[Generación de una nueva clave SSH y adición al agente SSH](/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)".

### No se pudo clonar

```shell
fatal: clone of 'git@github.com:<user>/<repo>' into submodule path '<path>' failed
Failed to clone 'src/github.com/<user>/<repo>'. Retry scheduled
Cloning into '<path>'...
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.
Please make sure you have the correct access rights
and the repository exists.
```

Este error significa ya sea que el repositorio que intentas clonar tiene submódulos a los cuales no tienes acceso o que no tienes una llave SSH válida configurada.

Si no tienes acceso a los submódulos, soluciona este problema contactando a la persona que administre los permisos para este repositorio.

Si no tiene una clave SSH válida configurada, consulte "[Generación de una nueva clave SSH y adición al agente SSH](/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)".

{% windows %}

### No se pudo leer la respuesta de AskPass

```shell
error: unable to read askpass response from '/Users/<path>/GitHub Desktop.app/Contents/Resources/app/static/ask-pass-trampoline.sh'
fatal: could not read Username for 'https://github.com': terminal prompts disabled
```

Este error se puede presentar a causa de varios eventos.

Si se modifican las entradas del registro de `Command Processor`, {% data variables.product.prodname_desktop %} responderá con un error de `Authentication failed`. Para verificar si estas entradas de registro se modifcaron, sigue estos pasos.

1. Abra el Editor del Registro (`regedit.exe`) y desplácese hasta las siguientes ubicaciones.
  `HKEY_CURRENT_USER\Software\Microsoft\Command Processor\`
  `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Command Processor\`
2. Compruebe si hay un valor `Autorun` en cualquiera de las ubicaciones.
3. Si hay un valor `Autorun`, elimínelo.

Si tu nombre de usuario de Windows tiene caracteres extendidos de Unicode, esto podría causar un error de respuesta de AskPass. Para solucionar los problemas, crea una cuenta nueva de usuario de Windows y migra tus archivos a dicha cuenta. Para obtener más información, consulte "[Crear una cuenta de usuario en Windows](https://support.microsoft.com/en-us/help/13951/windows-create-user-account)" en la documentación de Microsoft.

{% endwindows %}

## Lecturas adicionales
- "[Acerca de la autenticación en GitHub](/github/authenticating-to-github/about-authentication-to-github)"
