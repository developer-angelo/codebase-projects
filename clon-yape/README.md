
# Proyecto: YapeFake — Clon educativo inspirado en una app de pago móvil popular en Perú (Yape)

Resumen:
Yape es un proyecto educativo que recrea la experiencia de UI/UX de una conocida app de pagos peruana, implementando flujos de interfaz y funcionalidades de pago de manera totalmente simulada. Este repositorio servirá para practicar diseño de interfaces, arquitectura cliente/servidor, pruebas y despliegue. No procesa pagos reales ni emplea marcas, logos ni materiales protegidos — todos los elementos visuales y la identidad deben modificarse para evitar conflictos legales.

Objetivos:
- Recrear la interfaz y experiencia de usuario de una app de pagos para aprendizaje de diseño web.
- Implementar lógica de pagos simulada (envío/recepción de dinero, historial, contactos).
- Proveer guías de seguridad, privacidad y buenas prácticas para cuando se reemplace la simulación por integraciones reales (con cumplimiento legal y de seguridad).

Alcance:
- UI/UX: pantallas de inicio, registro/inicio de sesión, pantalla principal con balance, enviar/solicitar dinero, historial, perfil, contacto y notificaciones.
- Simulación: transacciones ficticias con estado ( pendiente, completado, fallido ), saldo simulado, validaciones y confirmaciones.
- Manejo de Datos: API local, con almacenamiento en el Navegador (localStorage) para datos de prueba.

Advertencias legales y de marca:
- Cambiar todos los logos, nombres, paletas de color y elementos identificativos originales antes de publicar el repositorio público.
- Incluir un aviso claro en la app y en el README indicando que es una simulación educativa y no un servicio de pagos real.
- No colectar ni almacenar datos financieros reales ni credenciales sensibles en entornos no seguros.

Funcionalidades principales:
- Autenticación básica (numero de celular simulado).
- Pantalla principal con saldo ficticio y accesos a enviar/solicitar pagos.
- Envío de dinero (simulado): búsqueda de contacto, monto, confirmación, PIN simulado y actualización de saldo.
- Solicitud de dinero: generación de petición y notificación simulada.
- Historial de transacciones con detalles.
- Gestión de perfiles y contactos.
- Notificaciones locales para cambios de estado en transacciones.
- Panel de administración simple para generar datos de prueba.

Flujo de pagos simulado:
- Validaciones en frontend (formatos, límites).
- Backend crea una transacción con estado "pending".
- Simulador de procesamiento (worker asíncrono o cron) que actualiza a "completed" o "failed" según reglas de prueba.
- Webhooks locales para notificar al cliente (opcional, simulados).

Arquitectura recomendada:
- Frontend: React Native (móvil) o React (web PWA) para reproducir UX móvil; UI component library personalizada.
- Base de datos: localStorage para producción de prueba.

Buenas prácticas de UI/UX:
- Inspirarse en patrones de diseño móvil: claridad, accesibilidad, microinteracciones.
- Cambiar colores y tipografía para evitar similitud con la app real.
- Proveer estados de error y confirmación claros.
- Accesibilidad: navegación por teclado, contraste adecuado y textos alternativos.

Seguridad y privacidad (simulación):
- Nunca almacenar números de tarjetas reales ni datos sensibles.
- En entornos de pruebas, usar datos ficticios generados.
- Si se integra una pasarela real en el futuro, seguir PCI-DSS y normativas locales (BV/PCI/BNP/etc.) y obtener asesoría legal.

> [!NOTE]
> Este proyecto es para aprendizaje y prototipado. Si en el futuro se quiere aceptar pagos reales, contactar a un especialista en cumplimiento, seguridad y asesoría legal antes de integrar cualquier pasarela o procesar datos reales.


