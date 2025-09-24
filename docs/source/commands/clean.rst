lista_de_nombres = ["Juan", "Nerea", "Camila", "Esteban"]

# Forma 1: iterar directamente sobre los elementos
for nombre in lista_de_nombres:
    print("hola", nombre)

print()  # Separador de líneas

# Forma 2: iterar usando índices con range()
for indice in range(len(lista_de_nombres)):
    print("hola", lista_de_nombres[indice])
