# Lista de palabras (puedes cambiarla o pedir al usuario que la ingrese)
palabras = ["manzana", "banana", "pera", "kiwi", "naranja"]

print("Lista original:")
print(palabras)

# Algoritmo bubble sort para ordenar alfabéticamente
n = len(palabras)
for i in range(n):
    # Cada pasada coloca la palabra más grande al final
    for j in range(0, n - i - 1):
        # Comparamos palabras adyacentes
        if palabras[j] > palabras[j + 1]:
            # Intercambiamos si están en el orden incorrecto
            palabras[j], palabras[j + 1] = palabras[j + 1], palabras[j]
        # Imprimir el estado actual de la lista para ver la iteración
        print(f"Iteración {i+1}-{j+1}: {palabras}")

print("\nLista ordenada alfabéticamente:")
print(palabras)


