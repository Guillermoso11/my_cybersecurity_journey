# my_cybersecurity_journey

# 🛡️ Mi Bóveda de Aprendizaje en Ciberseguridad

¡Bienvenido a mi portafolio técnico! En este espacio documento de forma práctica y estructurada los conceptos clave, arquitecturas de seguridad y fundamentos tecnológicos que voy dominando desde la base.

---

## 🏛️ El Kilómetro Cero: La Tríada CIA (Fundamentos de Seguridad)

Cualquier estrategia de defensa, política o configuración de red tiene como único objetivo proteger uno o varios de los tres pilares de la Tríada CIA.

| Pilar | Concepto Clave | ¿Qué significa? | Herramientas / Controles de Defensa |
| :--- | :--- | :--- | :--- |
| **Confidenciality** *(Confidencialidad)*  | Asegurar que los datos solo sean accesibles por el personal autorizado. | Evitar que personas no autorizadas husmeen o roben información confidencial. | * Cifrado (AES, SSL/TLS)<br>* Listas de Control de Acceso (ACL)<br>* Autenticación Multifactor (MFA) |
| **Integrity** *(Integridad)*  | Garantizar que la información sea exacta, completa y no haya sido modificada. | Asegurar que los datos no se alteren de forma maliciosa o accidental durante el camino. | * Funciones Hash (SHA-256)<br>* Firmas Digitales<br>* Control de versiones y auditoría |
| **Availability** *(Disponibilidad)* | Asegurar que los sistemas y los datos estén accesibles cuando se necesiten. | Garantizar que si un usuario legítimo necesita trabajar, el sistema no esté caído. | * Copias de seguridad (Backups)<br>* Redundancia de sistemas y hardware<br>* Mitigación de ataques DoS/DDoS |

## 🔐 Kilómetro 1: Autenticación vs. Autorización en la Práctica 

### 🛠️ Mi Entorno de Pruebas (Home Lab)
Para aplicar los conceptos teóricos de ciberseguridad en un entorno real, mantengo un **Home Lab** gestionado sobre un PC antiguo con:
* **Sistema Operativo:** Ubuntu Server
* **Gestor de Entorno:** CasaOS
* **Tecnología Principal:** Contenedores Docker para el despliegue y aislamiento de servicios.

Para dominar el Control de Accesos (Dominio 2 del examen CC de ISC2), he conectado la teoría con la práctica analizando la seguridad de mi propio servidor casero gestionado con Docker y CasaOS. 

Mucha gente confunde estos dos términos, pero en seguridad son capas totalmente distintas:

### 1. Autenticación (¿Quién eres?)
Es el proceso de verificar la identidad de un usuario. Es la puerta de entrada.
* **En mi Home Lab:** Ocurre cuando accedo a la interfaz web de administración e introduzco mis credenciales de usuario protegidas. El sistema comprueba que "yo soy quien digo ser".

### 2. Autorización (¿A qué tienes permiso?)
Es el proceso de verificar qué privilegios tiene esa identidad ya autenticada. Es lo que puedes hacer una vez estás dentro.
* **En mi Home Lab:** Ocurre a través de la gestión de contenedores aislados. Aunque yo esté autenticado para usar un servicio específico (como el servidor de fotos de Immich), ese servicio no tiene autorización ni permisos para modificar la configuración de red raíz de Ubuntu Server ni para acceder a los datos de otros contenedores. 

