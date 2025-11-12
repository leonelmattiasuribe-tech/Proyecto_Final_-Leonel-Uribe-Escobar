# Movimiento Armónico Simple
# Autor: Leonel Mattías Uribe Escobar
# Fecha: 12 Noviembre 2025

import matplotlib.pyplot as plt

# Datos experimentales
datos = {
    "4m": {
        "t": [0.000, 0.200, 0.400, 0.600, 0.800, 1.000],
        "x": [0.000, 0.951, 0.809, 0.588, 0.309, 0.000],
        "v": [0.000, -0.485, -0.923, -1.271, -1.494, -1.571]
    },
    "3m (tabla 2)": {
        "t": [0.000, 0.200, 0.400, 0.600, 0.800, 1.000],
        "x": [0.707, 0.410, 0.060, -0.298, -0.618, -0.856],
        "v": [-1.283, -1.654, -1.811, -1.731, -1.427, -0.936]
    },
    "3m (tabla 3)": {
        "t": [0.000, 0.200, 0.400, 0.600, 0.800, 1.000],
        "x": [0.000, 0.710, 1.327, 1.772, 1.986, 1.941],
        "v": [3.628, 3.392, 2.714, 1.683, 0.433, -0.873]
    },
    "2m (tabla 4)": {
        "t": [0.000, 0.200, 0.400, 0.600, 0.800, 1.000],
        "x": [0.000, 0.860, 1.552, 1.944, 1.958, 1.591],
        "v": [4.443, 4.012, 2.801, 1.047, -0.910, -2.691]
    },
    "2m (tabla 5)": {
        "t": [0.000, 0.200, 0.400, 0.600, 0.800, 1.000],
        "x": [2.000, 1.806, 1.261, 0.471, -0.410, -1.211],
        "v": [0.000, -1.910, -3.448, -4.318, -4.349, -3.535]
    },
    "m": {
        "t": [0.000, 0.200, 0.400, 0.600, 0.800, 1.000],
        "x": [-1.000, -0.809, -0.309, 0.309, 0.809, 1.000],
        "v": [0.000, 1.847, 2.988, 2.988, 1.847, 0.000]
    }
}

# Graficar posición y velocidad
for masa, d in datos.items():
    plt.figure(figsize=(10,4))
    
    # Gráfico de posición
    plt.subplot(1,2,1)
    plt.plot(d["t"], d["x"], 'o-', label="x(t)")
    plt.title(f"Posición - Masa {masa}")
    plt.xlabel("Tiempo [s]")
    plt.ylabel("Posición [m]")
    plt.grid(True)
    
    # Gráfico de velocidad
    plt.subplot(1,2,2)
    plt.plot(d["t"], d["v"], 'o-', color='r', label="v(t)")
    plt.title(f"Velocidad - Masa {masa}")
    plt.xlabel("Tiempo [s]")
    plt.ylabel("Velocidad [m/s]")
    plt.grid(True)
    
    plt.tight_layout()
    plt.show()
