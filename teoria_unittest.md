# Teoría de Unit Testing

## ¿Qué es Unit Testing?
El *unit testing* o prueba unitaria es una técnica del desarrollo de software que consiste en probar de forma aislada cada componente o función del programa  
El objetivo es asegurar que cada unidad del código funcione correctamente antes de integrarse con el resto

Según CodiLime (2023), las pruebas unitarias son una parte fundamental del desarrollo moderno porque ayudan a detectar errores tempranamente y garantizan que el sistema sea más estable  
(Fuente: CodiLime – “The Importance and Benefits of Unit Testing”)

## ¿Por qué usar Unit Testing?
Las pruebas unitarias ofrecen múltiples beneficios:
- Aumentan la calidad del software
- Reducen el costo y tiempo de corrección de errores
- Aseguran que las funciones nuevas no dañen el código existente
- Mejoran la confianza del desarrollador en su propio código

De acuerdo con Codefresh (2024), las pruebas unitarias también facilitan el mantenimiento y la refactorización del código, ya que sirven como una verificación automática  
(Fuente: Codefresh – “Unit Testing: Principles and Benefits”)

## ¿Cuándo usar Unit Testing?
Las pruebas unitarias deben aplicarse de manera continua durante el desarrollo del proyecto  
Se recomienda usarlas cada vez que se escribe una función o módulo nuevo, antes de integrarlo al sistema completo 
En entornos empresariales, suelen automatizarse para ejecutarse cada vez que se actualiza el códig

## ¿Cómo usar Unit Testing?
Cada lenguaje tiene su propia librería de pruebas:
- En **Python** se usa `unittest` o `pytest`
- En **Java**, `JUnit` 
- En **JavaScript**, `Jest` o `Mocha`

Ejemplo en Python:
```python
import unittest

class TestCalculadora(unittest.TestCase):
    def test_suma(self):
        self.assertEqual(2 + 3, 5)

if __name__ == '__main__':
    unittest.main()
