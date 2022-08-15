# ChallDSLatam
ChallDSLatam

En el presente desafío se tiene una base de datos pública de vuelos (despegues y aterrizajes) en una ventana de tiempo de un año.
El problema consiste en predecir la probabilidad de atraso de los vuelos que aterrizan o despegan del aeropuerto de Santiago de
Chile (SCL). Cada fila corresponde a un vuelo que aterrizó o despegó de SCL, y cada columna representa variables que pueden o no ser relevantes.

Luego de una mirada descriptiva a los datas, y un exhaustivo tratamiento de estos, el problema se ataca creando nuevas características que permitan construir la solución.

Debido a que la variable respuesta se construyó binaria (existe atraso o no), se resolvió utilizar un algoritmo ML de clasificación logística, más luego de descubrir que la proporción de atrasos de vuelos era relativamente menor (clases desbalanceadas) respecto del total de vuelos, se decidió mejorar el algoritmo con un tratamiento de balance de muestras. Consecuentemente, se utilizó la precisión del aprendizaje como métrica de rendimiento, pero además una medida de precisión balanceada que funciona mejor aún en estos casos.

Conclusión: Si bien la clasificación logística dio buenos resultados, se demostró que la precisión no siempre es el mejor indicador cuando tenemos problemas de balance en la variable respuesta. Por ello escogimos el algoritmo junto al método de balance que brindó el mejor resultado. Cabe la pregunta de cómo se comportaría el rendimiento de otros algoritmos con y sin estos métodos de balance nombrados.
