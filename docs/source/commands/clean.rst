# Simular una lista de reproducción con muchas canciones
lista_canciones = [
    "Shape of You - Ed Sheeran",
    "Blinding Lights - The Weeknd",
    "Levitating - Dua Lipa",
    "Peaches - Justin Bieber",
    "Save Your Tears - The Weeknd",
    "Bad Habits - Ed Sheeran",
    # ... (imagina que hay cientos más)
]

# Función para buscar canciones por artista o palabra clave
def buscar_canciones(lista, palabra_clave):
    resultados = []
    for cancion in lista:
        if palabra_clave.lower() in cancion.lower():
            resultados.append(cancion)
    return resultados

# Buscar canciones del artista 'Ed Sheeran'
resultados = buscar_canciones(lista_canciones, "Ed Sheeran")

print("Canciones encontradas:")
for cancion in resultados:
    print("-", cancion)
