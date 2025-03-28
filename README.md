https://github.com/vitaliy-pg/vitaliy-pg.git

Parte I: Conceptos y Teoría

Pregunta 1: Modelos OSI y TCP/IP

a) Diferencias principales:

b) Ventajas y limitaciones:

Modelo OSI:

Ventajas: Claramente estructurado; útil para aprendizaje.

Limitaciones: No se implementa directamente en la práctica.


Modelo TCP/IP:

Ventajas: Muy utilizado; más simple y práctico.

Limitaciones: Menos modular; no define capas de presentación ni sesión.




---

Pregunta 2: Función de la Capa de Transporte

La capa de transporte proporciona comunicación extremo a extremo entre aplicaciones. En OSI es la capa 4, y en TCP/IP también está presente.

Funciones:

Segmentación de datos

Control de errores y retransmisión (TCP)

Control de flujo

Multiplexación de conexiones


Protocolos comunes:

TCP: Orientado a conexión, confiable.

UDP: No orientado a conexión, rápido pero sin garantías.



---

Pregunta 3: TCP vs. UDP


---

Pregunta 4: Protocolo para Transferencia de Archivos

a) Protocolo tradicional: FTP (File Transfer Protocol)

b) Alternativas:

SFTP: Transferencia segura basada en SSH.

HTTPS: Descarga de archivos con cifrado SSL/TLS.



---

Pregunta 5: Resolución de Nombres en DNS

1. El usuario escribe una URL en el navegador.


2. Se consulta la caché local.


3. Si no está, se pregunta al DNS recursivo.


4. Este consulta al servidor raíz.


5. El servidor raíz responde con el TLD correspondiente.


6. El TLD devuelve el servidor autoritativo.


7. El servidor autoritativo proporciona la dirección IP.


8. El navegador se conecta al servidor.


9. La IP se guarda en caché para futuras solicitudes.




---

Pregunta 6: Comunicación en el Modelo TCP/IP

1. Aplicación: Se generan los datos (por ejemplo, en un navegador).


2. Transporte: Se segmentan los datos y se añaden puertos (TCP/UDP).


3. Internet: Se añade dirección IP origen y destino.


4. Acceso a red: Se encapsulan en tramas para su envío físico (bits).




---

Parte II: Capa Física y Ejercicios Prácticos

Pregunta 7: Tasa de Transmisión Máxima (Fórmula de Shannon)

Datos:

Ancho de banda: 500 MHz = 500×10⁶ Hz

SNR: 20 dB → SNR lineal = 10^(20/10) = 100


Fórmula de Shannon: C = B × log₂(1 + SNR)
C = 500×10⁶ × log₂(1 + 100) ≈ 500×10⁶ × 6.658 ≈ 3.33 Gbps


---

Pregunta 8: Ubicación de Portadoras para Eficiencia Espectral

Datos:

Primera portadora: 1.2 GHz

Ancho de banda: 300 MHz


a) Portadora anterior: 1.2 GHz – 300 MHz = 0.9 GHz
b) Portadora posterior: 1.2 GHz + 300 MHz = 1.5 GHz

Importancia: Ubicar bien las portadoras evita solapamientos y mejora la eficiencia del espectro.


---

Pregunta 9: Identificación de Modulación en función del BER

Orden de mayor a menor robustez al ruido:

1. BPSK (2 símbolos)


2. QPSK (4 símbolos)


3. 16-QAM


4. 64-QAM


5. 256-QAM



Justificación: A mayor número de símbolos, mayor eficiencia espectral, pero menor tolerancia al ruido.


---

Pregunta 10: Eficiencia del Sistema de Encapsulamiento

Datos:

Capa 5: 1.5 KB = 1536 bytes

Cabeceras en Capa 4 y 3: 80 bytes

Tamaño total: 1536 + 80 = 1616 bytes


a) Tamaño del mensaje: 1616 bytes

b) Tramas de 400 bytes → ceil(1616 / 400) = 5 tramas

c) Sobrecarga de capa 1:
Cada 2 bytes → 3 bytes extra (inicio, parada, CRC)
Ratio: 3/2 → para 400 bytes de datos se generan 600 bytes
Sobrecarga = 600 – 400 = 200 bytes por trama

d) Total transmitido = 5 × 600 = 3000 bytes
Eficiencia = (1536 / 3000) × 100 = 51.2%

