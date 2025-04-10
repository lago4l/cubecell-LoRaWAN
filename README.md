# CubeCell LoRaWAN – Comunicación con TTN y Gateway Dragino LPS8v2

Este proyecto demuestra cómo conectar uno o más dispositivos **Heltec CubeCell HTCC-AB02** a través de **LoRaWAN**, utilizando un gateway **Dragino LPS8v2** y la red de **The Things Network (TTN)**. Se implementa la activación **OTAA** para registrar los dispositivos y enviar datos periódicos.

---

## Requisitos

- 2 placas Heltec **CubeCell HTCC-AB02**
- 2 antenas LoRa (una por placa)
- 1 Gateway **Dragino LPS8v2**
- Cuenta gratuita en [The Things Network](https://www.thethingsnetwork.org/)
- Arduino IDE con soporte para CubeCell
---

## Contenido del repositorio

- `LoRaWAN.ino/` – Código de ejemplo completo para conectar un CubeCell a TTN usando OTAA.
- `CONFIGURACIÓN GATEWAY DRAGINO LPS8v2_TTN_CUBECELL.pdf/` – Puedes encontrar aquí la documentación del proyecto.
- `README.md` – Este archivo.

---

## Funcionalidad

### Emisor (CubeCell)
- Se configura con las claves OTAA (`DevEUI`, `JoinEUI`, `AppKey`) obtenidas de TTN.
- Se conecta automáticamente a la red TTN usando el gateway Dragino.
- Envía datos cada 15 segundos a través de LoRaWAN.

### Receptor (TTN)
- El gateway Dragino reenvía los paquetes recibidos al servidor de TTN.
- En la consola TTN, dentro del apartado "Live Data" del dispositivo, pueden verse los mensajes uplink y su contenido.

---

## Para más detalles

Consulta la documentación paso a paso (puedes llamarla `CONFIGURACIÓN GATEWAY DRAGINO LPS8v2_TTN_CUBECELL.pdf`) que incluye:

- Cómo registrar el **gateway Dragino LPS8v2** en TTN.
- Cómo crear una **aplicación** y añadir **end devices** (CubeCell) con OTAA.
- Cómo configurar las claves en el archivo `.ino`.
- Cómo compilar y cargar el sketch desde Arduino IDE.
- Verificación de datos en el panel TTN.

---

## Estado actual

- Gateway conectado a TTN
- CubeCell-1 y CubeCell-2 registrados y funcionando con OTAA
- Comunicación bidireccional verificada en TTN (uplink funcionando)

---

## Licencia

Este proyecto está bajo la licencia MIT. Puedes modificarlo y compartirlo libremente.
