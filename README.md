Descripción
E-mailicioso es una herramienta desarrollada en Python diseñada para ayudar a los usuarios a identificar correos electrónicos maliciosos, distinguiéndolos de mensajes legítimos o spam. Esta aplicación analiza archivos en formato .eml, verifica mecanismos de autenticación como SPF, DKIM y DMARC, y evalúa la reputación del remitente mediante consultas OSINT a servicios públicos como WHOIS, VirusTotal y otros.

Este proyecto surge como Trabajo Fin de Grado (TFG) en la Escuela Internacional de Posgrados, supervisado por Gino Alberto Veronesse, y busca proporcionar una solución ligera y accesible para usuarios y profesionales en ciberseguridad. No pretende reemplazar herramientas corporativas avanzadas, sino servir como recurso educativo y práctico para aumentar la conciencia frente a ataques de ingeniería social por correo.

Características principales
Análisis de cabeceras: Verificación automática de SPF, DKIM y DMARC para detectar spoofing.
Previsualización segura: Muestra el contenido del correo en HTML sin riesgos de ejecución.
Consultas OSINT: Búsqueda de reputación del dominio e IP en bases públicas (e.g., AbuseIPDB, Cisco Talos).
Interfaz intuitiva: Desarrollada con GTK y PyWebView para una experiencia de usuario sencilla.
Informes visuales: Alertas con iconos y colores para resaltar riesgos.
Requisitos
Python 3.8 o superior.
Bibliotecas necesarias (instalables vía pip):
gtk3 (para la interfaz).
pywebview (para renderizado HTML).
requests y beautifulsoup4 (para web scraping y OSINT).
email (módulo estándar para parsing de .eml).
Otras: dnspython (para validaciones DNS como SPF), dkimpy (para DKIM).
Asegúrate de tener instaladas las dependencias del sistema para GTK (e.g., en Ubuntu: sudo apt install libgtk-3-dev).

Instalación
Clona el repositorio:

text

Contraer

Ajuste

Copiar
git clone https://github.com/tu-usuario/e-mailicioso.git
cd e-mailicioso
Crea un entorno virtual (recomendado):

text

Contraer

Ajuste

Copiar
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
Instala las dependencias:

text

Contraer

Ajuste

Copiar
pip install -r requirements.txt
Si no hay un requirements.txt, instala manualmente:

text

Contraer

Ajuste

Copiar
pip install pywebview requests beautifulsoup4 dnspython dkimpy
Uso
Ejecuta la aplicación:
text

Contraer

Ajuste

Copiar
python main.py
En la interfaz:
Carga un archivo .eml (puedes descargar correos de clientes como Outlook o Gmail en este formato).
La app mostrará una previsualización, análisis de cabeceras y resultados OSINT.
Interpreta las alertas: Verde para legítimo, Rojo para sospechoso.
Ejemplo de flujo:

Selecciona un correo sospechoso.
Verifica si SPF/DKIM/DMARC fallan.
Revisa la reputación del dominio.
Para más detalles, consulta la Guía de uso o el TFG completo en el repositorio.

Ejemplos
Incluye correos de prueba en la carpeta examples/:

legitimo.eml: Correo válido.
malicioso.eml: Ejemplo con spoofing.
Contribuciones
¡Las contribuciones son bienvenidas! Sigue estos pasos:

Forkea el repositorio.
Crea una rama: git checkout -b feature/nueva-funcion.
Commitea cambios: git commit -m 'Añade nueva función'.
Push: git push origin feature/nueva-funcion.
Abre un Pull Request.
Asegúrate de seguir el código de conducta y probar los cambios.

Licencia
Copyright © 2025 Antonio Carranza Barroso. Todos los derechos reservados. Queda prohibida la reproducción total o parcial sin autorización.

Este proyecto se distribuye bajo la licencia MIT License (ajusta según tu preferencia).

Contacto
Autor: Antonio Carranza Barroso
Email: antoniocarranza14@gmail.com
GitHub: tu-usuario
Para más información, consulta el TFG: E-mailicioso. Desarrollo de una herramienta Python para evitar ataques de ingeniería social por correo.

¡Gracias por usar E-mailicioso! Si encuentras bugs o sugerencias, abre un issue.
