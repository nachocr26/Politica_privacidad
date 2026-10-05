# 🛡️ Política de Privacidad — FamFinance P2P

> **Última actualización:** Octubre de 2026  
> **Versión oficial para Google Play Console y usuarios.**  
> *Versión web pública alojada en:* [`public/politica-privacidad.html`](./public/politica-privacidad.html)

---

## 1. Introducción y Filosofía "Zero-Server"

En **FamFinance P2P**, la privacidad y la confidencialidad de la economía familiar son la base absoluta sobre la que se ha diseñado el sistema.

- **Arquitectura Zero-Server:** FamFinance **no almacena tus datos financieros en servidores centrales en la nube** ni los transmite a servidores de nuestra propiedad.
- **Soberanía del Usuario:** Tus saldos, transacciones, presupuestos y notas de voz pertenecen exclusivamente a los dispositivos de tu hogar.
- La aplicación cumple estrictamente con el **Reglamento General de Protección de Datos (RGPD UE 2016/679)**, la **Ley Orgánica 3/2018 (LOPD-GDD)** de España y las **Políticas de Datos de Usuario de Google Play**.

---

## 2. Datos Tratados y Cifrado

La aplicación gestiona localmente las siguientes categorías de información:

1. **Movimientos Contables y Presupuestos:** Ingresos, gastos, categorías, metas de ahorro y cuentas bancarias registradas por el usuario.
2. **Cifrado Militar de Extremo a Extremo (E2EE):** Todo el estado familiar viaja cifrado entre dispositivos con **AES-GCM de 256 bits** y derivación de claves mediante **PBKDF2** (100.000 iteraciones con HMAC-SHA-256). Nadie ajeno a tu familia puede descifrar la información.
3. **Identificador del Dispositivo:** Un identificador criptográfico pseudo-aleatorio generado en el dispositivo para sellar licencias locales contra manipulaciones.

---

## 3. Permisos Solicitados en Android y Justificación de Uso

| Permiso | Finalidad Técnica y Garantía de Privacidad |
|---|---|
| **Cámara** (`android.permission.CAMERA`) | Utilizado **únicamente** para escanear el código QR de invitación familiar entre móviles. El flujo de vídeo no se graba ni se sube a ninguna parte. |
| **Micrófono** (`android.permission.RECORD_AUDIO`) | Utilizado para la grabación opcional de notas de voz de gastos. El audio se procesa en el dispositivo. |
| **Servicio de Notificaciones Bancarias** (`BIND_NOTIFICATION_LISTENER_SERVICE`) | Permite detectar notificaciones de bancos españoles (BBVA, Santander, CaixaBank, ING, Sabadell, Revolut, etc.) y Google Wallet para registrar gastos automáticamente. **Los datos se procesan en la memoria local y jamás se transmiten a terceros.** |
| **Biometría y Huella Dactilar** (`USE_BIOMETRIC` / `USE_FINGERPRINT`) | Permite proteger el acceso a la app con la huella del usuario. Gestionado por el hardware seguro del teléfono; la app nunca tiene acceso a los datos biométricos. |
| **Internet** (`INTERNET`) | Necesario para la sincronización P2P directa entre dispositivos (WebRTC y red Nostr cifrada) y para la gestión de publicidad y compras en Google Play. |
| **Facturación de Google Play** (`BILLING`) | Gestiona la compra opcional de la versión Pro sin anuncios a través de la pasarela oficial de Google Play. |

---

## 4. Publicidad y Terceros (Google AdMob)

- En su versión gratuita, FamFinance muestra anuncios no intrusivos servidos por **Google AdMob** (Google LLC).
- Google AdMob puede procesar identificadores del dispositivo (como el ID de publicidad de Android), dirección IP y datos de diagnóstico conforme a la [Política de Privacidad de Google](https://policies.google.com/technologies/ads).
- **Eliminación Total de Publicidad (FamFinance Pro):** Al adquirir la versión Pro mediante Google Play Billing, la publicidad y el SDK de AdMob se desactivan permanentemente para todo el grupo familiar.

---

## 5. Derechos de Acceso, Supresión (Derecho al Olvido) y Portabilidad

El usuario mantiene el control total sobre su información en todo momento:

- **Borrado Cero Inmediato:** Desde *Ajustes > Avanzado > "Borrar todos los datos y reiniciar a 0"*, el usuario puede eliminar instantáneamente el 100% de la base de datos local y destruir las claves criptográficas.
- **Portabilidad de Datos:** En cualquier momento puedes exportar tus finanzas a formatos universales (.xlsx, .csv o JSON cifrado).
- **Abandono / Expulsión Familiar:** Si un miembro abandona el grupo, se ejecuta un formateo automático a 0 de su copia local.

---

## 6. Contacto del Desarrollador

Para cualquier consulta relativa a la privacidad de FamFinance P2P:

- **Responsable:** Ignacio Cantero
- **Correo electrónico:** nachocr26@gmail.com
- **Repositorio del proyecto:** [https://github.com/nachocr26/famfinance](https://github.com/nachocr26/famfinance)
