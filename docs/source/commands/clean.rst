print("Hola, elige una opción según sea tu caso:")
print("1. Soy usuario registrado")
print("2. Soy usuario nuevo")

# Base de datos simulada (diccionario)
usuarios = {
    "alice": "password123",
    "bob": "qwerty456"
}

codigo_admin_correcto = "admin2025"  # Código para registrar nuevos usuarios

opcion = input("Ingresa el número de la opción deseada: ")

if opcion == "1":
    print("Has elegido la opción 1")
    usuario = input("Ingresa tu nombre de usuario: ")
    contrasena = input("Ingresa tu contraseña: ")
    
    if usuario in usuarios and usuarios[usuario] == contrasena:
        print(f"Bienvenido, {usuario}!")
        # Aquí puedes agregar más funciones para el usuario autenticado
    else:
        print("Usuario o contraseña incorrectos.")
        
elif opcion == "2":
    print("Vamos a registrarte")
    codigo_admin = input("Ingresa el código de administrador: ")
    
    if codigo_admin == codigo_admin_correcto:
        nuevo_usuario = input("Ingresa tu_
