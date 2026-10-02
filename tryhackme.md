## Especializacion THM

### Host Virtual
- **Qué demuestra:** Cómo los archivos `/etc/hosts` (Linux) y `C:\Windows\System32\drivers\etc\hosts` (Windows) permiten ocultar subdominios o puertos de administración en desarrollo.
- **Evidencia/herramientas:** Ejemplos de registro DNS privado y asignación de nombre de dominio a IP, laboratorio de descubrimiento de hosts.

### IDOR
- **Qué demuestra:** Cómo acceder a objetos directamente (archivos, cuentas, registros) sin verificar permisos de autorización.
- **Evidencia/herramientas:** Laboratorio THM/HTB con Burp Suite para manipular parámetros y probar identificadores de objeto.

### Manipulación de Cookies
- **Qué demuestra:** Cómo interceptar, modificar y analizar cookies HTTP para evaluar su seguridad y encontrar fallos de autenticación.
- **Evidencia/herramientas:** Capturas de tráfico HTTP, ejemplos de cookies manipuladas en laboratorios THM.

### Path Transversal
- **Qué demuestra:** Cómo acceder a archivos del sistema fuera del directorio de la aplicación mediante entrada no validada.
- **Evidencia/herramientas:** Imágenes de laboratorio THM, payloads con `../` sequences, comandos de exploración.

### SSRF (Servidor-Sede Repuesto Former)
- **Qué demuestra:** Cómo engañar a un servidor para que realice solicitudes HTTP a recursos internos o externos sin autorización.
- **Evidencia/herramientas:** Técnicas de escalada en THM, ejemplos de endpoints internos expuestos.

### LFI (Inclusión de archivos locales)
- **Qué demuestra:** Cómo forzar a una aplicación web a incluir archivos internos del sistema mediante entrada del usuario no validada.
- **Evidencia/herramientas:** 12 bloques de código con payloads y ejemplos de URLs vulnerables en THM.

### RFI (Inclusión remota de archivos)
- **Qué demuestra:** Cómo cargar archivos remotos en un servidor web para lograr ejecución de código malicioso y toma de control.
- **Evidencia/herramientas:** Ejemplos de payloads RFI en laboratorios THM, impacto en ejecución de código.

### Descubrimiento automatizado
- **Qué demuestra:** Cómo usar herramientas automatizadas (gobuster) para descubrir contenido ocuito en lugar de hacerlo manualmente.
- **Evidencia/herramientas:** Uso de gobuster en laboratorio THM, resultados de directorios y archivos encontrados.

### Google Hacking / Dorking
- **Qué demuestra:** Cómo usar operadores avanzados de Google (site:, filetype:, etc.) para encontrar información sensible en resultados de búsqueda.
- **Evidencia/herramientas:** Ejemplos de dorks aplicados a tryhackme.com, resultados obtenidos en laboratorio.

### S3 Buckets
- **Qué demuestra:** Cómo identificar y acceder a buckets de Amazon S3 mal configurados que exponen archivos web estáticos.
- **Evidencia/herramientas:** Ejemplos de acceso HTTP/HTTPS a buckets públicos, enfoque en tryhackme.

### Command Injection / RCE
- **Qué demuestra:** Cómo ejecutar comandos del sistema operativo desde una aplicación web cuando la entrada del usuario no es validada correctamente.
- **Evidencia/herramientas:** Ejemplos de payloads en THM, resultados de ejecución de comandos remotos.

### Burp Suite (Buro Quite)
- **Qué demuestra:** Cómo interceptar, modificar y analizar el tráfico HTTP entre navegador y servidor para pruebas de seguridad.
- **Evidencia/herramientas:** Herramienta profesional de PortSwigger, uso de módulos Proxy, capturas de tráfico.

### Intruder
- **Qué demuestra:** Cómo realizar ataques automatizados sobre peticiones HTTP interceptadas: fuerza bruta, fuzzing, inyección de payloads.
- **Evidencia/herramientas:** Módulo de Burp Suite, payloads configurables, resultados de fuerza bruta y fuzzing.

### Repeater
- **Qué demuestra:** Cómo enviar manualmente solicitudes HTTP modificadas al servidor para evaluar su comportamiento ante diferentes parámetros.
- **Evidencia/herramientas:** Módulo de Burp Suite, historial de peticiones, modificaciones de parámetros.

### Favicon
- **Qué demuestra:** Cómo identificar tecnologías de un sitio web a partir del favicon (icono de la pestaña) usando herramientas como Wappalyzer.
- **Evidencia/herramientas:** Imágenes de favicon en laboratorios tryhackme, uso de extensiones de navegador.

### Walking an Application
- **Qué demuestra:** Cómo explorar manualmente una aplicación web (inspeccionar código fuente, navegar por la app) como primer paso en el hacking web.
- **Evidencia/herramientas:** Capturas de pantalla de la aplicación THM, uso de "ver código fuente" (U), URLs de laboratorio.

### Blind XSS
- **Qué demuestra:** Cómo explotar XSS donde el payload se almacena pero no es visible directamente para el atacante (ej. en logs de admin).
- **Evidencia/herramientas:** Capturas de payloads, escenarios de exposición a otros usuarios, técnicas de detección.

### XSS Basado en el DOM
- **Qué demuestra:** Cómo explotar XSS que ocurre en el navegador del cliente mediante manipulación del DOM sin envío al servidor.
- **Evidencia/herramientas:** Análisis de árbol DOM, JavaScript malicioso, resultados de ejecución en navegador.

### XSS Reflejado
- **Qué demuestra:** Cómo inyectar código malicioso a través de una URL que la aplicación procesa sin validar, ejecutándose en el navegador de la víctima.
- **Evidencia/herramientas:** Capturas de URLs con payloads, explicación de que no se almacena en el servidor.

### XSS Almacenado
- **Qué demuestra:** Cómo inyectar código que se almacena permanentemente en la aplicación (base de datos) y se ejecuta para todos los usuarios.
- **Evidencia/herramientas:** Imágenes de ejemplo, escenario de comentarios públicos vulnerables.

### ¿Qué es XSS?
- **Qué demuestra:** Concepto básico de Cross-Site Scripting: inyección de JavaScript malicioso en páginas web para robar información o manipular la página.
- **Evidencia/herramientas:** Capturas de payloads, ejemplos de robo de información, uso en laboratorios THM.

### Fuerza Bruta de usernames
- **Qué demuestra:** Cómo usar ataques de fuerza bruta automatizados para descubrir nombres de usuario válidos contra una lista predefinida.
- **Evidencia/herramientas:** Comandos de terminal, archivos de wordlists, laboratorio tryhackme.

### Enumeración de nombres de usuario
- **Qué demuestra:** Cómo usar mensajes de error específicos (ej. "Ya existe una cuenta con este nombre") para identificar usuarios válidos.
- **Evidencia/herramientas:** Formularios de registro/login, análisis de respuestas de error, laboratorio tryhackme.

### Blind SQL Injection - Boolean Based
- **Qué demuestra:** Cómo explotar inyecciones SQL ciegas que devuelven respuestas binarias (true/false) para extraer datos poco a poco.
- **Evidencia/herramientas:** 32 bloques de código con payloads booleanos, laboratorio THM, resultados de extracción.

### Blind SQL Injection (General)
- **Qué demuestra:** Cómo realizar inyecciones SQL cuando la aplicación no muestra errores ni resultados visibles, pero la inyección aún funciona.
- **Evidencia/herramientas:** Payloads de inyección, técnicas de detección, resultados de explotación.

### In-Band SQL Injection
- **Qué demuestra:** Cómo explotar inyecciones SQL usando el mismo canal de comunicación para enviar el ataque y recibir resultados (errores o datos directos).
- **Evidencia/herramientas:** Técnicas de error-based y union-based, resultados visibles en la aplicación.

### SQL Injection
- **Qué demuestra:** Cómo manipular consultas SQL de una aplicación web mediante inserción de código malicioso en datos de entrada.
- **Evidencia/herramientas:** Ejemplos de payloads, laboratorios THM, resultados de manipulación de base de datos.

### Metasploit - Búsqueda de vulnerabilidades
- **Qué demuestra:** Cómo usar Metasploit para buscar, identificar y explotar vulnerabilidades conocidas en sistemas, servicios o aplicaciones.
- **Evidencia/herramientas:** msfconsole, módulos de exploit y payload, integración con nmap, resultados de explotación.

### Metasploit Database
- **Qué demuestra:** Cómo conectar Metasploit a una base de datos PostgreSQL para guardar información de auditoría (hosts, servicios, vulnerabilidades, credenciales).
- **Evidencia/herramientas:** 34 bloques de código, configuración de base de datos, integración con nmap.

### Metasploit Exploitation
- **Qué demuestra:** Cómo usar Metasploit para automatizar la explotación de vulnerabilidades: ejecución de código arbitrario, escalada de privilegios, toma de control.
- **Evidencia/herramientas:** msfconsole, payloads, módulos de exploit, ejemplos en tryhackme.

### Metasploit (Qué es)
- **Qué demuestra:** Cómo la plataforma Metasploit Framework se usa para desarrollar, probar y ejecutar exploits contra sistemas en pruebas de penetración y Red Team.
- **Evidencia/herramientas:** Laboratorios THM, componentes (exploits, payloads, auxiliares), ejemplos prácticos.

### Introducción al análisis de vulnerabilidades
- **Qué demuestra:** Cómo identificar fallos en un sistema que generan riesgo, clasificados en físicos y lógicos, usando herramientas como Metasploit.
- **Evidencia/herramientas:** Capturas de análisis, uso de metasploit, evaluación de riesgos.

### Fallas criptográficas
- **Qué demuestra:** Cómo identificar y explotar fallos en implementaciones criptográficas usando herramientas como hashcat, hydra y john.
- **Evidencia/herramientas:** hashcat, hydra, john, resultados de descifrado de contraseñas.

### Inyección (OWASP Top 10)
- **Qué demuestra:** Cómo explotar vulnerabilidades de inyección (SQL, comando, LDAP, etc.) que pasan datos maliciosos a sistemas subyacentes sin validación.
- **Evidencia/herramientas:** Burp Suite, sqlmap, payloads, laboratorios tryhackme.

### Hydra - Herramienta de Fuerza Bruta
- **Qué demuestra:** Cómo realizar ataques de fuerza bruta contra servicios de autenticación remotos usando THC-hydra.
- **Evidencia/herramientas:** 22 bloques de código, laboratorios tryhackme, resultados de fuerza bruta.

### Protocolos, ataques y mitigaciones
- **Qué demuestra:** Cómo analizar protocolos de red (FTP, HTTP, SMTP, etc.) y sus ataques asociados (sniffing, MITM) con herramientas de captura y Metasploit.
- **Evidencia/herramientas:** Capturas de tráfico, metasploit, módulos tryhackme.

### Reconocimiento Pasivo
- **Qué demuestra:** Cómo recopilar información sobre un objetivo sin interactuar directamente con él, usando fuentes públicas.
- **Evidencia/herramientas:** Técnicas de OSINT, ejemplos en tryhackme.

### Escaneos TCP avanzados con Nmap
- **Qué demuestra:** Cómo realizar escaneos TCP especializados (nulo, fin, xmas, etc.) para eludir firewalls y detectar puertos abiertos.
- **Evidencia/herramientas:** Comandos nmap (-sN, -sF, -sX, etc.), tabla de tipos de escaneo.

### Escaneos post-port Nmap
- **Qué demuestra:** Cómo usar opciones avanzadas de nmap para identificar servicios, versiones, sistema operativo y guardar resultados en diferentes formatos.
- **Evidencia/herramientas:** Opciones de nmap (-sV, -O, -oN, etc.), resultados de escaneo.

### ¿Qué es Nmap?
- **Qué demuestra:** Cómo nmap (Network Mapper) escanea redes y sistemas en busca de hosts activos, puertos abiertos y servicios disponibles.
- **Evidencia/herramientas:** Imágenes de herramienta, uso en auditoría de seguridad.

### Opciones de Ping y Escaneo en Nmap
- **Qué demuestra:** Cómo usar opciones de ping (-sn, -Pn) y escaneo de nmap para descubrir hosts activos en una red.
- **Evidencia/herramientas:** Comandos nmap, explicación de opciones, resultados de escaneo.

### Socat
- **Qué demuestra:** Cómo usar Socat para dirigir conexiones de red, flujo de datos y pseudo-terminal de manera flexible, incluyendo conexiones cifradas con OpenSSL.
- **Evidencia/herramientas:** Comparación con netcat, ejemplos de uso, resultados de conexión.

### Escalada de privilegios en Windows mediante Servicios
- **Qué demuestra:** Cómo abusar de la configuración de servicios de Windows (SCM) para ejecutar código con privilegios elevados.
- **Evidencia/herramientas:** 52 bloques de código, laboratorios THM, payloads y resultados.

### Escalada de privilegios con tareas programadas (Windows)
- **Qué demuestra:** Cómo usar AlwaysInstallElevated y tareas programadas para escalar privilegios en Windows.
- **Evidencia/herramientas:** 22 bloques de código, laboratorios, payloads, resultados.

### Recolección de credenciales en Windows
- **Qué demuestra:** Cómo encontrar credenciales en archivos de instalación desatendida (Unattend.xml, sysprep.xml) y en registro de Windows.
- **Evidencia/herramientas:** Laboratorios THM/tryhackme, análisis de archivos de configuración.

### Enumeración en Linux (Post-Exploitation)
- **Qué demuestra:** Cómo realizar enumeración del sistema en Linux tras comprometerlo para identificar oportunidades de escalada y movimiento lateral.
- **Evidencia/herramientas:** Comandos de enumeración, análisis de entorno, resultados de escalada.

### Escalada de privilegios mediante PATH en Linux
- **Qué demuestra:** Cómo manipular la variable de entorno $PATH para ejecutar binarios maliciosos con privilegios elevados.
- **Evidencia/herramientas:** Laboratorios THM/tryhackme, ejemplos de manipulación de PATH, exploits.

### Escalada de privilegios con Cron Jobs
- **Qué demuestra:** Cómo usar tareas programadas (crontab) propietarias de root como vía de escalada de privilegios.
- **Evidencia/herramientas:** Análisis de crontabs, ejemplos de tareas programadas vulnerables.

### Linux Capabilities
- **Qué demuestra:** Cómo analizar capacidades de Linux (capabilities) que asignan privilegios específicos a binarios sin necesidad de bit SUID.
- **Evidencia/herramientas:** Ejemplos de capacidades, comparación con SUID, resultados de análisis.

### SUID
- **Qué demuestra:** Cómo explotar binarios con bit SUID que se ejecutan con privilegios del propietario (root) para escalar privilegios.
- **Evidencia/herramientas:** Ejemplos de binarios SUID, técnicas de explotación, resultados.

### Escalada mediante Kernel Exploits
- **Qué demuestra:** Cómo escalar privilegios en Linux explotando vulnerabilidades conocidas en el kernel (ej. CVE-2015-1328).
- **Evidencia/herramientas:** Capturas de contexto, exploit de kernel, resultados de escalada a root.

### Escalada de privilegios con SUDO
- **Qué demuestra:** Cómo abusar de permisos sudo configurados en /etc/sudoers para ejecutar comandos como root.
- **Evidencia/herramientas:** Comandos sudo, hashcat, nmap, laboratorios THM, resultados.

### Ataque SSRF (Máquina THM)
- **Qué demuestra:** Cómo explotar una vulnerabilidad SSRF en un sitio web de soporte técnico para acceder a información restringida en /private.
- **Evidencia/herramientas:** Writeup paso a paso de laboratorio THM, descubrimiento de endpoints, resultados de acceso.

### Evadiendo filtro en LFI - Challenge 2
- **Qué demuestra:** Cómo evadir filtros en una vulnerabilidad LFI de TryHackMe para leer archivos protegidos como /etc/flag2.
- **Evidencia/herramientas:** 14 bloques de código, modificación de cookies, writeup de challenge THM/tryhackme.
