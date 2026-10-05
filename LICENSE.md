# ACUERDO DE LICENCIA Y CONDICIONES DE USO · KYRN DEVDOCK

**Versión:** 1.0.0  
**Fecha de Vigencia:** Octubre 2026  
**Titular de Derechos:** KyrnForge (`https://kyrnforge.dev`)  
**Contacto Oficial:** `dev@kyrnforge.dev`  

---

### 1. CONCESIÓN DE LICENCIA (EDICIÓN COMUNITARIA / BINARIOS PÚBLICOS)
KyrnForge otorga al usuario una licencia revocable, personal, gratuita, no exclusiva e intransferible para descargar, instalar y utilizar los binarios compilados de **Kyrn DevDock** (`Kyrn-DevDock-Setup-1.0.0.exe` y `Kyrn-DevDock-Portable-1.0.0.exe`) con propósitos de desarrollo de software, diagnóstico de red y administración local de procesos.

### 2. CÓDIGO FUENTE Y PROPIEDAD INTELECTUAL (PROPIETARIO / CLOSED-SOURCE)
- **Titularidad:** Kyrn DevDock, incluyendo su núcleo nativo en Rust, interfaz de usuario en React, logotipo oficial, marcas comerciales, sello PE y documentación asociada son propiedad exclusiva de **KyrnForge**.
- **Distribución sin Código Fuente:** Esta distribución pública proporciona únicamente paquetes ejecutables optimizados. El código fuente original se mantiene cerrado como tecnología propietaria de KyrnForge.
- **Restricciones:** Queda terminantemente prohibido descompilar, realizar ingeniería inversa, desensamblar, modificar, eliminar sellos de copyright o revender este software o sus partes sin autorización expresa y por escrito de KyrnForge.

### 3. POLÍTICA DE PRIVACIDAD Y PROCESAMIENTO 100% LOCAL
KyrnForge garantiza la absoluta soberanía y privacidad de los datos del desarrollador:
1. **Procesamiento en Máquina Local:** El escaneo de tablas de sockets TCP/UDP, la resolución de PIDs, el cálculo de consumo de RAM/CPU y la terminación de procesos se ejecutan 100% en la CPU y memoria RAM de tu equipo mediante APIs nativas de Windows en Rust.
2. **Cero Fuga de Código o Tráfico:** Kyrn DevDock jamás lee, inspecciona, registra ni transmite el código fuente de tus proyectos, archivos de variables de entorno (`.env`), contraseñas o datos transmitidos por los sockets de red.
3. **Cero Telemetría Oculta:** La aplicación no incluye rastreadores de publicidad ni servicios de recolección de datos de terceros.

### 4. SINCRONIZACIÓN EN LA NUBE · KYRN CLOUD (`https://kyrnforge.dev`)
- **Carácter Opcional:** El módulo Kyrn Cloud es totalmente opcional. La aplicación es 100% funcional sin conexión a internet ni registro de cuenta.
- **Datos Sincronizados:** Si decides registrar una cuenta en Kyrn Cloud, únicamente se sincronizarán metadatos ligeros de configuración:
  - Nombres y etiquetas de Workspaces creados.
  - Puertos favoritos o preconfigurados (ej. 3000, 5173, 8080).
  - Alias de dominios virtuales locales (ej. `api.devdock.local`).
  - Preferencias de interfaz (intervalos de escaneo y temas).
- **Aislamiento Criptográfico Multi-Inquilino (Multi-Tenant):** Cada cuenta de usuario se aísla mediante un identificador universal único (`UUIDv4`). El acceso a la nube requiere un token firmado criptográficamente (JWT) validado en los servidores Edge de Cloudflare con derivación de claves mediante algoritmos seguros. Ningún usuario puede visualizar o interactuar con los datos de otro.

### 5. SEGURIDAD DE PROCESOS Y EXENCIÓN DE RESPONSABILIDAD
- Kyrn DevDock incorpora un sistema de centinela preventivo que advierte y bloquea intentos accidentales de terminación de procesos críticos de Windows (tales como `System`, `svchost.exe`, `csrss.exe`, `lsass.exe` o PIDs $\le$ 4).
- No obstante, la acción final de purgar procesos (incluyendo el botón *Clean Slate* o *Zombie Purge*) es ejecutada bajo el consentimiento y discreción del usuario. KyrnForge no se hace responsable por la pérdida de datos o cierres inesperados derivados de la terminación forzada voluntaria de aplicaciones de desarrollo.

### 6. INTEGRIDAD Y CANALES OFICIALES DE DESCARGA
Para salvaguardar la seguridad de tu sistema frente a ejecutables manipulados por terceros, descarga siempre las versiones oficiales y verifica los hashes criptográficos (SHA-256) en:
- **Sitio Web Oficial:** [https://kyrnforge.dev](https://kyrnforge.dev)
- **Repositorio Oficial de Lanzamientos:** [https://github.com/devlwte/kyrn-devdock](https://github.com/devlwte/kyrn-devdock)

---
*Copyright © 2026 KyrnForge. Todos los derechos reservados.*
