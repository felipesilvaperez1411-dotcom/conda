# Número de participantes
num_participantes = 3

# Lista para almacenar las respuestas
respuestas = []

print(f"Vamos a registrar las respuestas de {num_participantes} participantes.")

for i in range(num_participantes):
    nombre = input(f"Nombre del participante {i+1}: ").strip()
    while not nombre:
        nombre = input("Por favor, ingresa un nombre válido: ").strip()
        
    respuesta = input(f"{nombre}, ingresa tu respuesta para el reto:

