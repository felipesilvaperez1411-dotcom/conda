# Simulación básica de autenticación y autorización

# Base de datos simulada de usuarios y sus contraseñas
usuarios = {
    "alice": "password123",
    "bob": "qwerty456",
    "carol": "abc123"
}

# Permisos asignados a cada usuario (qué carpetas pueden acceder)
permisos = {
    "alice": ["carpeta1", "carpeta2"],
    "bob": ["carpeta2"],
    "carol": []
}

def autenticar(usuario, contrasena):
    """Verifica si el usuario y la contraseña son correctos."""
    if usuario in usuarios and usuarios[usuario] == contrasena:
        print(f"Usuario {usuario} autenticado correctamente.")
        return True
    else:
        print("Error de autenticación.")
        return False

def autorizar(usuario, carpeta):
    """Verifica si el usuario tiene permiso para acceder a la carpeta."""
    if carpeta in permisos.get(usuario, []):
        print(f"Acceso concedido a {carpeta} para {usuario}.")
        return True
    else:
        print(f"Acceso denegado a {carpeta} para {usuario}.")
        return False

# Ejemplo de uso
usuario = input("Usuario: ")
contrasena = input("Contraseña: ")

if autenticar(usuario, contrasena):
    carpeta = input("¿Qué carpeta quieres acceder?: ")
    autorizar(usuario, carpeta)
