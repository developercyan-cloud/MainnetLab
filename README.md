# MainNet Lab — prueba controlada de 5 USDT

Esta versión deja **5 USDT** precargados para una prueba manual de USDT → WETH.

## Qué incluye
- `index.html`: interfaz independiente de ProEshop.
- Cotización directa con Uniswap V3 Quoter V2.
- Aprobación exacta, nunca ilimitada.
- Si la allowance actual es insuficiente y no es cero, primero solicita ponerla a cero, verifica el resultado y después solicita aprobar exactamente 5 USDT.
- Intercambio con límite de deslizamiento y confirmaciones explícitas en MetaMask.
- `server.js` y `package.json` para alojar el HTML como servicio Node en Railway.

## Despliegue
Sube el contenido de esta carpeta a un repositorio independiente o sustituye únicamente los archivos de la aplicación MainNet Lab en el repositorio/servicio que ya aloja esa interfaz. No reemplaces el servicio del fork Anvil ni modifiques `main.py`, la base de datos, snapshots o variables del fork.

## Pasos de prueba
1. Abre MainNet Lab en el navegador de MetaMask.
2. Confirma que la red seleccionada usa el RPC de Railway previsto.
3. Conecta la wallet y consulta la cotización para 5 USDT.
4. Pulsa **Aprobar cantidad exacta**. Si la allowance actual es distinta de cero e insuficiente, se pedirán dos firmas: primero ponerla a cero y luego aprobar exactamente 5 USDT.
5. Comprueba en MetaMask cada solicitud antes de firmar.
6. Solo cuando la aprobación quede confirmada, vuelve a cotizar si expiró y pulsa el intercambio.

## Advertencia
El RPC está configurado con Chain ID `1`, igual que Ethereum Mainnet. No firmes si no puedes confirmar que MetaMask está usando el RPC de Railway. Usa exclusivamente una wallet de pruebas y no mantengas activos reales de Mainnet en ella. Este archivo no contiene claves privadas ni frases semilla.
