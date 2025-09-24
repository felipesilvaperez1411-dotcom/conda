# Número de palabras secretas
num_palabras = 5

# Pedimos las palabras secretas
palabras = []
print(f"Por favor, cada una de las {num_palabras} personas ingrese su palabra secreta:")
for i in range(num_palabras):
    palabra = input(f"Palabra secreta {i+1}: ").strip().lower()
    palabras.append(palabra)

print("\nPalabras secretas ingresadas (no mostradas para que nadie vea):")
print(" " * 20, "[Palabras ocultas]")

# Ahora la persona ordenadora puede preguntar letras una por una
print("\nLa persona ordenadora puede preguntar letras para ordenar las palabras.")
print("Por ejemplo, puede preguntar: ¿La primera letra de la palabra 1 es 'a'?")

while True:
    preguntar = input("\n¿Quieres preguntar una letra? (s/n): ").strip().lower()
    if preguntar != 's':
        break

    num_palabra = int(input(f"¿De qué palabra quieres preguntar la letra? (1 a {num_palabras}): "))
    posicion_letra = int(input("¿Qué posición de letra quieres preguntar? (1 para primera letra, 2 para segunda, etc.): "))
    letra_preguntada = input("¿Qué letra quieres preguntar?: ").lower()

    # Ajustamos índices para Python (que comienza en 0)
    indice_palabra = num_palabra - 1
    indice_letra = posicion_letra - 1

    # Verificamos que la posición sea válida para la palabra
    if 0 <= indice_letra < len(palabras[indice_palabra]):
        letra_real = palabras[indice_palabra][indice_letra]
        if letra_real == letra_preguntada:
            print("¡Sí! La letra coincide.")
        else:
            print(f"No, la letra es '{letra_real}'.")
    else:
        print("La posición de letra no es válida para esta palabra.")

# Finalmente, ordenamos las palabras alfabéticamente
palabras_ordenadas = sorted(palabras)

print("\nPalabras ordenadas alfabéticamente:")
for palabra in palabras_ordenadas:
    print(palabra)
