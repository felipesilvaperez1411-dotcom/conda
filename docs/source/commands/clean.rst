# Número de participantes
num_participantes = 3

# Lista para almacenar las respuestas
respuestas = []

print(f"Vamos a registrar las respuestas de {num_participantes} participantes.")

for i in range(num_participantes):
    nombre = input(f"Nombre del participante {i+1}: ").strip()
    while not nombre:
        nombre = input("Por favor, ingresa un nombre válido: ").strip()
        
    respuesta = input(f"{nombre}, ingresa tu respuesta para el reto: ").strip()
    while not respuesta:
        respuesta = input("Por favor, ingresa una respuesta válida: ").strip()
        
    respuestas.append((nombre, respuesta))

print("\nResumen de respuestas recibidas:")
for nombre, respuesta in respuestas:
    print(f"{nombre} respondió: {respuesta}")

# Guardar respuestas en un archivo
with open("respuestas_reto.txt", "w", encoding="utf-8") as archivo:
    archivo.write("Resumen de respuestas del reto\n\n")
    for nombre, respuesta in respuestas:
        archivo.write(f"{nombre} respondió: {respuesta}\n")

print("\n¡Gracias por participar en el reto! Las respuestas se guardaron en 'respuestas_reto.txt'.")
