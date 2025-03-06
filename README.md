# Proyectos
#En este proyecto, su intención es poner en práctica los conocimientos adquiridos en la Unidad 1, por lo cual se menciona un formulario para poder calcular el IMC de las personas.
#Se conforma en solicitar un formulario donde el usuario tiene que ingresar el nombre completo.

print("Hola Mundo")

# Solicitar nombre completo
nombre1 = input("¿Cuál es tu nombre o nombres?: \n")
nombre2 = input("¿Cuál es tu primer apellido?: \n")
nombre3 = input("¿Cuál es tu segundo apellido?: \n")
print("Hola " + nombre1 + " " + nombre2 + " " + nombre3)

#También se solicita la edad, peso y estatura, para realizar las operaciones necesarias.

# Solicitar edad
edad = int(input("¿Cuántos años tienes?: "))
print("Tienes: " + str(edad) + " años")
if edad < 18:
    print("Usted es menor de edad")
else:
    print("Usted es mayor de edad")

# Solicitar estatura y peso
try:
    estatura = float(input("Ingresa tu estatura en metros: "))  # Se solicita la unidad de medida en metros para el cálculo del IMC
except ValueError:
    print("Oops! Debes ingresar un dato numérico. Intenta de nuevo.")

try:
    peso = float(input("Ingresa tu peso en Kg: "))
except ValueError:
    print("Oops! Debes ingresar un dato numérico. Intenta de nuevo.")

print("Tu estatura es: " + str(estatura) + " m.")
print("Tu peso es: " + str(peso) + " Kg")

#Al momento de concluir las operaciones básicas, se realiza una valoración, para determinar el IMC el cual nos dará un resultado si se encuentra en desnutrición, normal o con obesidad.

# Calcular IMC
print("Calculando tu IMC")
imc = peso / (estatura ** 2)
print("Tu IMC es: " + str(imc))

# Determinar la categoría del IMC
if imc >= 0 and imc <= 15.99:
    print("Delgadez severa")
elif imc >= 16.00 and imc <= 16.99:
    print("Delgadez moderada")
elif imc >= 17.00 and imc <= 18.49:
    print("Delgadez leve")
elif imc >= 18.50 and imc <= 24.99:
    print("Normal")
elif imc >= 25.00 and imc <= 29.99:
    print("Sobrepeso")
elif imc >= 30.00 and imc <= 34.99:
    print("Obesidad leve")
elif imc >= 35.00 and imc <= 39.00:
    print("Obesidad media")
elif imc >= 40.00:
    print("Obesidad mórbida")
else:
    print("Valor de IMC no válido")
