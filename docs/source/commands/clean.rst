# Número de participantes
num_participantes = 3

# Lista para almacenar las respuestas
respuestas = []

print(f"Vamos a registrar las respuestas de {num_participantes} participantes.")

for i in range(num_participantes):
    nombre = input(f"Nombre del participante {i+1}: ")
    respuesta = input(f"{nombre}, ingresa tu respuesta para el reto: ")
    respuestas.append((nombre, respuesta))

print("\nResumen de respuestas recibidas:")
for nombre, respuesta in respuestas:
    print(f"{nombre} respondió: {respuesta}")

# Aquí podrías agregar lógica para evaluar o procesar las respuestas

print("\n¡Gracias por participar en el reto!")
