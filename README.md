# wifi-security-lab
Laboratorio personal de auditoría WiFi WPA2/WPA3 para aprender seguridad de redes
WiFi Security Lab — Auditoría WPA2/WPA3

Proyecto personal de aprendizaje sobre la seguridad de redes WiFi. Consiste en una herramienta de auditoría desarrollada en Bash sobre Kali Linux, pensada para entender en profundidad —desde la práctica— cómo funcionan los mecanismos de protección WPA2/WPA3 y dónde están sus puntos débiles.

⚠️ Nota sobre este repositorio Por responsabilidad, este repositorio contiene únicamente la documentación del proyecto, no el código ofensivo. La herramienta se desarrolló y probó exclusivamente en un entorno de laboratorio propio, contra routers y redes de mi propiedad. Auditar redes ajenas sin autorización es ilegal.

Por qué lo hice

Quería entender la seguridad WiFi de verdad, no solo en teoría. Para ello monté un laboratorio propio con varios routers y distintas redes de prueba, y construí una herramienta que automatizara el proceso completo de auditoría. La idea: para saber defender una red, primero hay que entender cómo se audita una.

El desarrollo lo realicé de forma iterativa con desarrollo asistido por IA (Claude Code), depurando y probando contra mi propio entorno hasta conseguir un funcionamiento estable, y priorizando entender el porqué de cada paso antes que el resultado.

Qué aprendí
Cómo funciona el handshake WPA2/WPA3 (EAPOL / PMKID) y por qué es el punto clave de la auditoría.
El papel del modo monitor en una tarjeta inalámbrica y cómo se gestiona.
Técnicas de captura de handshake (deauth dirigido vs. broadcast) y por qué una red con clientes conectados es más vulnerable.
Cracking por diccionario con hashcat (modo 22000), el uso de reglas y la importancia de wordlists específicas frente a genéricas.
Buenas prácticas de OPSEC básicas, como el cambio de dirección MAC antes de operar.
La importancia de automatizar con control de errores y limpieza del entorno al finalizar.
Tecnologías y herramientas

Bash · Kali Linux · aircrack-ng (airodump-ng, aireplay-ng, airmon-ng) · hashcat · hcxtools · macchanger · Claude Code

Flujo de la herramienta (a alto nivel)
Comprobación de dependencias del sistema.
Activación del modo monitor y cambio de MAC.
Escaneo de redes del entorno y selección del objetivo.
Identificación del tipo de router/ISP para optimizar el diccionario.
Captura del handshake.
Cracking por diccionario en varias fases.
Conclusión

Más allá de la herramienta en sí, este proyecto me sirvió para entender la cadena completa de una auditoría WiFi y, sobre todo, para pensar como lo haría un atacante con el fin de saber defender mejor. Es la base sobre la que quiero seguir construyendo mi perfil en ciberseguridad defensiva (SOC / Blue Team).

Proyecto con fines educativos. Desarrollado y probado en un entorno de laboratorio propio.
