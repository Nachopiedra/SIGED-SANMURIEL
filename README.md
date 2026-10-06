# SIGED SANMURIEL

Plataforma comunitaria de información meteorológica, predicción 24 h y supervisión de la red eléctrica mediante SIGED Edge.

## v0.1

La interfaz comunitaria integra cuatro bloques:

- **Meteorología local**: observaciones procedentes de la estación Ecowitt integrada en SIGED.
- **Predicción 24 h**: previsión horaria mediante Open-Meteo.
- **Grid Watch**: estado, tensión, frecuencia y calidad básica de la red.
- **Black Box**: histórico público y filtrado de incidencias eléctricas.

## Privacidad

SIGED SANMURIEL no publica consumos domésticos, producción fotovoltaica, SOC de baterías, vehículo eléctrico, aerotermia, agua ni credenciales/API keys. El fichero `data/sanmuriel.json` contiene exclusivamente información seleccionada para uso comunitario.

## Arquitectura

`SIGED Edge (privado) -> filtro/publicador -> data/sanmuriel.json -> SIGED SANMURIEL (público)`

La previsión meteorológica se consulta desde el navegador y se mantiene separada de la observación real de la estación local.

## Estado

La interfaz v0.1 está creada. Los valores actuales de `data/sanmuriel.json` constituyen la semilla inicial basada en la prueba de integración; el siguiente paso es conectar el publicador automático del mini-PC para mantenerlos actualizados.
