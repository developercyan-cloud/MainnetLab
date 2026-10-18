# MainNet Lab — Uniswap V3

Interfaz independiente para pruebas de cotización e interacción con Uniswap V3.

## Archivos
- `index.html`: interfaz MainNet Lab.
- `server.js`: servidor HTTP Express.
- `package.json`: dependencias y comando de inicio.

## Despliegue en Railway como servicio separado
1. Sube la carpeta `mainnet-lab` al repositorio del fork sin sobrescribir archivos existentes.
2. En Railway, crea un servicio nuevo desde el mismo repositorio.
3. Configura el directorio raíz/working directory del nuevo servicio como `mainnet-lab`.
4. Usa `npm start` como comando de inicio.
5. En Settings → Networking, genera un dominio público.

No reemplaces el Dockerfile, comando de inicio, variables ni volúmenes del servicio actual del fork.

## Precaución
La interfaz requiere que la wallet esté conectada al RPC de pruebas previsto. Chain ID 1 coincide con Ethereum Mainnet; verifica el RPC activo antes de firmar. Usa únicamente una wallet de pruebas sin fondos reales.
