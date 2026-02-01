# escala-de-notas
print("=== CALCULADORA DE PRUEBAS CON RÚBRICA ===")

# Pruebas ya definidas
pruebas = {
    "Lenguaje": {
        "Comprensión lectora": 40,
        "Ortografía": 20,
        "Redacción": 40
    },
    "Matemática": {
        "Ejercicios": 50,
        "Procedimiento": 30,
        "Resultados": 20
    },
    "Historia": {
        "Contenido": 60,
        "Análisis": 40
    }
}

# Mostrar pruebas
print("\nPruebas disponibles:")
for p in pruebas:
    print("-", p)

# Elegir prueba
while True:
    prueba = input("\nElige la prueba: ")
    if prueba in pruebas:
        break
    print("Prueba no existe")

rubrica = pruebas[prueba]
puntaje_total = sum(rubrica.values())
puntaje_obtenido = 0

# Mostrar rúbrica
print(f"\nRÚBRICA DE {prueba}:")
for criterio, max_p in rubrica.items():
    print(f"- {criterio}: {max_p} puntos")

# Ingresar puntajes
for criterio, max_p in rubrica.items():
