```
⚡ Guía de Inicio Rápido

1. **Instalar Dependencias:** Descarga todas las librerías del proyecto.
   ```bash
   npm install

```
Boosters/
├── public/
│   └── # Imágenes, íconos y fuentes estáticas
│
├── src/
│   ├── app/
│   │   ├── globals.css      # Estilos globales de Tailwind
│   │   ├── layout.tsx       # Plantilla principal de la aplicación
│   │   └── page.tsx         # Página de inicio
│   │
│   ├── components/          # === ★ BOOSTERS VISUALES (UI) ===
│   │   │
│   │   ├── atoms/           # Componentes más pequeños e indivisibles
│   │   │   ├── Button.tsx
│   │   │   ├── Input.tsx
│   │   │   └── Spinner.tsx
│   │   │
│   │   ├── molecules/       # Combinación de átomos
│   │   │   ├── FormControl.tsx
│   │   │   └── Alert.tsx
│   │   │
│   │   ├── organisms/       # Secciones de UI complejas
│   │   │   ├── Header.tsx
│   │   │   ├── Modal.tsx
│   │   │   └── Card.tsx
│   │   │
│   │   └── web3/            # Componentes UI específicos para Web3
│   │       ├── ConnectWalletButton.tsx
│   │       ├── NFTCard.tsx
│   │       └── WalletInfo.tsx
│   │
│   ├── hooks/               # === ★ BOOSTERS LÓGICOS (Funcionalidad) ===
│   │   │
│   │   ├── useInteraction/  # Hooks para interactuar con hardware/APIs del navegador
│   │   │   ├── useNFCReader.ts
│   │   │   ├── useQRScanner.ts
│   │   │   └── useBluetooth.ts
│   │   │
│   │   └── useWeb3/         # Hooks para lógica de Blockchain
│   │       ├── useNetworkDetector.ts
│   │       └── useWalletBalance.ts
│   │
│   ├── lib/                 # Funciones de utilidad (helpers)
│   │   └── utils.ts         # Ej: formatear direcciones, cálculos, etc.
│   │
│   └── styles/              # (Opcional) Si necesitas CSS más complejo
│       └── custom.css
│
├── tailwind.config.ts       # Configuración de Tailwind CSS
├── package.json
└── README.md                # Tu guía del proyecto


2.  **Configurar Tailwind (si falta):** Si el archivo `tailwind.config.ts` no existe, créalo en la raíz del proyecto y pega este código:
    
    ```
    import type { Config } from 'tailwindcss'
    
    const config: Config = {
      content: [
        './src/pages/**/*.{js,ts,jsx,tsx,mdx}',
        './src/components/**/*.{js,ts,jsx,tsx,mdx}',
        './src/app/**/*.{js,ts,jsx,tsx,mdx}',
      ],
      theme: {
        extend: {
          backgroundImage: {
            'gradient-radial': 'radial-gradient(var(--tw-gradient-stops))',
            'gradient-conic':
              'conic-gradient(from 180deg at 50% 50%, var(--tw-gradient-stops))',
          },
        },
      },
      plugins: [],
    }
    export default config
    
    ```
    
3.  **Ejecutar en Desarrollo:** Inicia el servidor local en `http://localhost:3000` con auto-recarga.
    
    ```
    npm run dev
    
    ```