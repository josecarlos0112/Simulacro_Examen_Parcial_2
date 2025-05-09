
# Simulacro Examen Parcial 2 - Redes de Computadoras

## Parte I: Capa de Red

### Pregunta 1: Cálculo de Ruta Más Corta
- **Algoritmo de Dijkstra**: Utiliza una tabla de distancias desde el nodo origen, actualizando las rutas más cortas mediante un enfoque iterativo hasta alcanzar el destino.
- **Enrutamiento por Inundación (Flooding)**: Envía paquetes por todas las salidas excepto la de entrada. Garantiza entrega, pero con alto coste de ancho de banda. Comparado con Dijkstra, es menos eficiente.

### Pregunta 2: Direcciones de Broadcast y Subredes
- **172.29.152.0/21**: Broadcast = `172.29.159.255`
- **172.18.26.0/23**: Broadcast = `172.18.27.255`

### Pregunta 3: Última Dirección y Rango de Hosts
- **172.30.67.192/26**: Último host válido = `172.30.67.254`
- **172.22.53.199/22**: Rango = `172.22.52.1` - `172.22.55.254`

### Pregunta 4: Capacidad y Segmentación
- **172.26.0.0/26**: 62 hosts por subred
- **172.18.171.190/23**: Subred = `172.18.170.0/23`

### Pregunta 5: Subredes Necesarias
- Fórmula: `2^s` subredes. Si se necesitan al menos 4 subredes, se prestan 2 bits (s=2). Ejemplo: /18 en una red clase B.

## Parte II: Capa de Transporte

### Pregunta 6: TCP vs UDP
- **TCP**: Conexión orientada, fiable, control de flujo y congestión, más lento.
- **UDP**: No orientado a conexión, no garantiza entrega ni orden, más rápido.
- **Aplicaciones UDP**: Videollamadas, juegos online.

### Pregunta 7: Conexiones TCP
- **Establecimiento (3-way handshake)**: SYN → SYN-ACK → ACK
- **Terminación (4-way handshake)**: FIN → ACK → FIN → ACK

### Pregunta 8: Multiplexación
- **Descendente**: Varios procesos comparten una conexión.
- **Ascendente**: Se enrutan datos entrantes al proceso correcto por número de puerto.

### Pregunta 9: Tamaño de Ventana TCP
- **RTT = 0.05s**, **BW = 100 Mbps**, **MSS = 1500 bytes**
- Ventana óptima: 5,000,000 bits = 625,000 bytes ≈ 416 segmentos MSS

### Pregunta 10: Control de Congestión en TCP
- **Slow Start**: crecimiento exponencial al inicio.
- **Nagle**: agrupa pequeños segmentos.
- **Clark (Delayed ACK)**: retrasa ACK para combinarlo con datos de salida.

## Parte III: Capa de Aplicación y Multimedia

### Pregunta 11: DNS
- Consulta caché local → DNS recursivo → raíz → TLD → autoritativo → IP al cliente → conexión

### Pregunta 12: Protocolos de Correo
- **POP3**: Descarga y elimina del servidor.
- **IMAP**: Sincroniza correos, mantiene en el servidor.
- **SMTP**: Envío de correos.

### Pregunta 13: HTTP y FTP
- **HTTP**: Sin estado, usa GET, POST, PUT, DELETE.
- **FTP**: Usa conexiones separadas para control y datos.

### Pregunta 14: Streaming y VoIP
- **Tipos de Streaming**:
  - UDP: videollamadas
  - HTTP: YouTube clásico
  - DASH: YouTube/Netflix adaptativo
- **VoIP**: Voz digitalizada → paquetes → RTP sobre UDP → reconstrucción. Problemas: retardo, pérdida, eco.

### Pregunta 15: Congestión en Multimedia
- **Buffering**: suaviza variaciones.
- **DiffServ**: marca paquetes para priorización.

### Pregunta 16: Best-Effort vs Multiclase
- **Best-Effort**: sin garantía de QoS. Ej: navegación web.
- **Multiclase**: tráfico priorizado. Ej: videoconferencia.

## Parte IV: Seguridad en Redes

### Pregunta 17: Áreas Críticas
- **Confidencialidad**: cifrado
- **Autenticación**: MFA
- **No repudio**: firmas digitales
- **Integridad**: hashing + HMAC

### Pregunta 18: Cifrado Simétrico vs Asimétrico
- **Simétrico**: 1 clave, rápido (AES)
- **Asimétrico**: 2 claves, lento (RSA)

### Pregunta 19: Algoritmo RSA
- **Ejemplo**: p=3, q=11 → n=33, ϕ=20, e=7, d=3
- **Mensaje M=4** → cifrado = 16, descifrado = 4

### Pregunta 20: Firewalls, VPN e IPSec
- **Firewalls**: filtrado de paquetes y con estado.
- **VPN**: túneles cifrados, acceso remoto.
- **IPSec**: cifrado IP, entre routers o redes.

### Pregunta 21: SSL/TLS y DNS Spoofing
- **SSL/TLS**: HTTPS seguro con cifrado y certificados.
- **DNS Spoofing**: ataques con IP falsas. DNSSEC usa firmas digitales para proteger.
