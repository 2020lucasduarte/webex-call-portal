# Portal de llamadas Webex

Página estática para intentar iniciar una llamada a la extensión/cola `9672` mediante Cisco Webex App.

## Archivos

- `index.html`: página completa (HTML, CSS y JavaScript). No requiere dependencias ni proceso de build.
- `.nojekyll`: evita el procesamiento Jekyll de GitHub Pages.
- `README.md`: estas instrucciones.

## Publicar en GitHub Pages

1. Creá un repositorio en GitHub.
2. Subí los archivos de este ZIP a la raíz del repositorio.
3. Entrá a **Settings → Pages**.
4. En **Build and deployment**, seleccioná **Deploy from a branch**.
5. Elegí la rama `main` y la carpeta `/(root)`, y guardá.
6. Esperá a que GitHub Pages publique el sitio y abrí la URL que indique.

## Requisitos de prueba

- Webex App instalada y con sesión iniciada.
- El usuario puede llamar manualmente a `9672` desde Webex App.
- El sistema operativo/navegador debe reconocer el protocolo `clicktocall:` y asociarlo con Webex App.

## Importante

El portal solo intenta abrir el cliente de llamadas; no contiene credenciales ni usa API/backend. El protocolo `clicktocall:` puede variar según la versión de Webex App, navegador y sistema operativo. Si no funciona, probá el protocolo SIP documentado por Cisco (por ejemplo, `sip:9672`) luego de confirmar que sea compatible con la configuración de tu tenant.

Una página publicada en GitHub Pages suele ser pública, incluso si el repositorio es privado según las condiciones del plan y la organización. No incluyas información sensible. GitHub Pages no proporciona por sí solo autenticación para restringir un sitio a los usuarios del tenant.

La llamada a una Call Queue de Webex Calling es una llamada de voz; este botón no garantiza activar video ni habilita video de extremo a extremo a través de la cola.
