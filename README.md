# taller-de-programacion
def calcular_potencia(x, k):
    return x ** k

def contar_digitos(x):
    return len(str(abs(x)))

def es_capicua(x):
    x_str = str(x)
    return x_str == x_str[::-1]

def menu():
    while True:
        print("\n----- MENÚ -----")
        print("1. Calcular la potencia K de un número X")
        print("2. Obtener la cantidad de dígitos de un número X")
        print("3. Determinar si un número es capicúa")
        print("4. Salir")
        
        opcion = input("Seleccione una opción: ")
        
        if opcion == '1':
            x = int(input("Ingrese el número X: "))
            k = int(input("Ingrese la potencia K: "))
            print(f"{x} elevado a la {k} es: {calcular_potencia(x, k)}")
        
        elif opcion == '2':
            x = int(input("Ingrese el número X: "))
            print(f"El número {x} tiene {contar_digitos(x)} dígitos.")
        
        elif opcion == '3':
            x = int(input("Ingrese el número X: "))
            if es_capicua(x):
                print(f"El número {x} es capicúa.")
            else:
                print(f"El número {x} no es capicúa.")
        
        elif opcion == '4':
            print("¡Hasta luego!")
            break
        else:
            print("Opción inválida. Intente de nuevo.")

# Ejecutar el menú
menu()
