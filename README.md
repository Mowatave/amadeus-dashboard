# Dashboard de Monitorización

Proyecto sencillo para monitorizar el estado de las apps en producción.

- Chequeos cada 30s.
- Historial de los últimos 5 minutos.
- Dashboard web para ver rápidamente qué endpoints están disponibles.

## Añadir URLs a monitorizar

Edita el archivo `index.html` y modifica la lista `ENDPOINTS`, por ejemplo:

```js
const ENDPOINTS = [
      {
        url: "https://staging.amadeusmagister.com/api/v1/health",
        name: "Staging"
      },
      // Agrega más si lo deseas...
    ];
```

## Personalizar intervalos

En el script de `index.html` se define `FETCH_INTERVAL_SEC` para el tiempo entre chequeos (por defecto, `30 = 30s`), y `MAX_HISTORY` para el número de resultados en el historial (por defecto, `10`).  