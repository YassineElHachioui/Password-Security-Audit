# Auditoría de Seguridad: Análisis de Contraseñas

> **Proyecto de Hacking Ético (Red Team) y Bastionado (Blue Team)**
>
> Este proyecto demuestra la vulnerabilidad de las contraseñas débiles mediante ataques de fuerza bruta y diccionario, y cómo mitigarlas mediante políticas de seguridad robustas.

## Fase Ofensiva (Pentesting)
Se realizó una auditoría utilizando la herramienta estándar **John The Ripper** sobre un fichero de hashes volcado de un sistema comprometido.
- **Herramienta:** John The Ripper (Ubuntu).
- **Ataque:** Diccionario y Fuerza Bruta.
- **Resultado:** Se obtuvieron credenciales de usuarios con contraseñas simples en menos de 2 minutos.

![Auditoría con John The Ripper](john-ripper-crack.png)

---

## Fase Defensiva (Hardening)
Para mitigar esta vulnerabilidad, se implementaron **Políticas de Grupo (GPO)** en el Directorio Activo:
1.  **Complejidad:** Se exige el uso de mayúsculas, minúsculas y caracteres especiales.
2.  **Longitud:** Mínimo de 10 caracteres (aumentando exponencialmente el tiempo de crackeo).
3.  **Bloqueo:** La cuenta se bloquea tras 3 intentos fallidos.

![Política de Contraseñas Segura](windows-policy.png)
