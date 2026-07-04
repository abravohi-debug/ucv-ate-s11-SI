# Laboratorio: Minimax y Poda Alfa-Beta

## Descripción
Este proyecto implementa los algoritmos Minimax y Poda Alfa-Beta para resolver un árbol de decisión simplificado.

## Objetivo
Comparar el resultado y la eficiencia de Minimax frente a la optimización mediante Poda Alfa-Beta.

---

## Instalación

python -m venv .venv

Activar entorno:

Windows:
.venv\Scripts\activate

Linux / Mac:
source .venv/bin/activate

Instalar dependencias:
pip install -r requirements.txt

---

## Ejecución

python -m src.main

---

## Pruebas

pytest --cov=src --cov-report=term-missing --cov-report=xml

---

## Laboratorio UCV - Sistemas Inteligentes

---

## Preguntas de análisis

1. ¿Por qué Minimax y Alfa-Beta devuelven el mismo valor?  
Porque ambos algoritmos exploran el mismo árbol de decisión y buscan la jugada óptima. La diferencia es que Alfa-Beta optimiza el proceso eliminando ramas innecesarias, pero el resultado final es el mismo.

2. ¿Cuándo Alfa-Beta reduce más nodos?  
Reduce más nodos cuando el árbol está bien ordenado, ya que permite podar ramas temprano y evitar evaluaciones innecesarias.

3. ¿Qué ocurre si el árbol está mal ordenado?  
La poda es menos eficiente y se evalúan más nodos, acercándose a Minimax. Sin embargo, el resultado final no cambia.

4. ¿Cómo se aplicaría este algoritmo en ajedrez, damas o tres en raya?  
Se usa para evaluar movimientos futuros. Cada estado del juego es un nodo del árbol, y el algoritmo selecciona la jugada que maximiza la probabilidad de ganar o minimizar la derrota.

---

## Conclusión
Minimax garantiza la solución óptima, pero es más costoso. Alfa-Beta mejora la eficiencia reduciendo nodos sin cambiar el resultado final.