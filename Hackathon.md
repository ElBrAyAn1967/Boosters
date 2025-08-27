# Boosters: Tu Librería de Componentes para el Hackathon 🚀🇦🇷

Este proyecto, **Boosters**, es una librería de componentes y lógica reutilizable construida con Next.js y TypeScript. El objetivo es crear un conjunto de piezas de UI y funciones listas para usar, que nos permitirán construir aplicaciones de forma increíblemente rápida durante el hackathon de Argentina.

Este archivo es tu mapa y tu lista de tareas. ¡A construir!

---

## Filozofía y Principios

Todo booster creado en este proyecto, ya sea visual o lógico, debe seguir estos principios:

* **Modularidad:** Deben ser autocontenidos y fáciles de integrar en cualquier parte del proyecto.
* **Reusabilidad:** Diseñados para ser usados en múltiples contextos sin modificaciones.
* **Tipado Estricto:** Todas las `props` y funciones deben estar definidas con interfaces de TypeScript.
* **Estilo Atómico (UI):** Los componentes visuales se manejarán exclusivamente con **Tailwind CSS**.
* **Eficiencia (Lógica):** Las funciones lógicas deben ser performantes y manejar errores de forma clara.

---

## 🤖 Boosters Visuales (Componentes de UI)

Componentes visuales organizados por complejidad y siguiendo la metodología de *Atomic Design*.

### 1. Atoms (Átomos)

Los bloques de construcción más pequeños de nuestra UI.

| Componente | Descripción | Dificultad | Estado |
| :--- | :--- | :--- | :--- |
| **`Button`** | Botón personalizable (primario, secundario). | Fácil | ⏳ Pendiente |
| **`Input`** | Campo de texto, número, etc. | Fácil | ⏳ Pendiente |
| **`Label`** | Etiqueta de texto para formularios. | Fácil | ⏳ Pendiente |
| **`Icon`** | Renderiza íconos SVG. | Fácil | ⏳ Pendiente |
| **`Badge`** | Pequeña insignia de estado o notificación. | Fácil | ⏳ Pendiente |
| **`Spinner`** | Animación de carga para indicar procesos. | Fácil | ⏳ Pendiente |
| **`Avatar`** | Imagen de perfil de usuario circular. | Fácil | ⏳ Pendiente |

### 2. Molecules (Moléculas)

Grupos de átomos que funcionan como una unidad.

| Componente | Descripción | Dificultad | Estado |
| :--- | :--- | :--- | :--- |
| **`FormControl`** | Agrupa `Label` e `Input` para formularios. | Fácil | ⏳ Pendiente |
| **`Alert`** | Mensaje de notificación con ícono. | Fácil | ⏳ Pendiente |
| **`SearchBar`** | Un `Input` con un `Button` de búsqueda. | Intermedio | ⏳ Pendiente |
| **`UserAvatar`** | `Avatar` con el nombre/dirección del usuario. | Intermedio | ⏳ Pendiente |

### 3. Organisms (Organismos)

Secciones de UI complejas que forman una parte distintiva de la interfaz.

| Componente | Descripción | Dificultad | Estado |
| :--- | :--- | :--- | :--- |
| **`Header`** | Barra de navegación principal con links. | Intermedio | ⏳ Pendiente |
| **`Footer`** | Pie de página con links a redes. | Intermedio | ⏳ Pendiente |
| **`Card`** | Contenedor genérico para mostrar contenido. | Intermedio | ⏳ Pendiente |
| **`Modal`** | Ventana emergente para acciones importantes. | Difícil | ⏳ Pendiente |
| **`Sidebar`** | Menú de navegación lateral colapsable. | Difícil | ⏳ Pendiente |

---

## 🧠 Boosters Lógicos (Funcionalidad Core)

Estos son módulos no visuales que encapsulan lógica compleja y la hacen fácil de reusar en cualquier parte de la aplicación.

| Booster Lógico | Descripción | Dificultad | Estado |
| :--- | :--- | :--- | :--- |
| **`NetworkDetector`** | **Detecta y gestiona la red de Ethereum (L1/L2) a la que está conectada la wallet.** | Intermedio | ⏳ Pendiente |
| **`QRScanner`** | Utiliza la cámara del dispositivo para leer códigos QR y devolver su contenido. | Intermedio | ⏳ Pendiente |
| **`NFCReader`** | **Detecta e interactúa con etiquetas NFC a través de la API Web NFC del navegador.** | Difícil | ⏳ Pendiente |
| **`BluetoothConnector`** | Permite buscar y conectarse a dispositivos Bluetooth cercanos vía Web Bluetooth API. | Difícil | ⏳ Pendiente |

---

## 💎 Boosters Web3

Componentes y lógica que combinan UI y funcionalidad específica para blockchain.

| Componente | Descripción | Dificultad | Estado |
| :--- | :--- | :--- | :--- |
| **`ConnectWalletButton`**| Botón que gestiona todo el flujo de conexión. | Intermedio | ⏳ Pendiente |
| **`WalletInfo`** | Muestra la dirección acortada y el balance. | Intermedio | ⏳ Pendiente |
| **`NFTCard`** | `Card` especializada para mostrar un NFT. | Intermedio | ⏳ Pendiente |
| **`TransactionStatusModal`** | `Modal` que sigue el estado de una transacción. | Difícil | ⏳ Pendiente |

---

## ✅ Cómo Añadir un Nuevo Booster

Sigue estos pasos para mantener el orden:

1.  **Ubicación:**
    * **Visual:** Crea tu componente en `src/components/`, en su carpeta (`atoms`, `molecules`, etc.).
    * **Lógico:** Crea tu función o hook en `src/logic/` o `src/hooks/`.
2.  **Definir Tipos:** Usa una `interface` o `type` de TypeScript para las `props` o los argumentos de tu función.
3.  **Desarrollar:** Escribe el código de tu Booster.
4.  **Documentar:** Añade el nuevo Booster a la tabla correspondiente en este archivo `README.md` y define su `Dificultad` y `Estado`.