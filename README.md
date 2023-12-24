# punto-4-trabajo-diciembre-
def main():
    # Inicializar contadores y acumuladores
    total_numeros = 0
    total_pares = 0
    suma_pares = 0
    suma_impares = 0
    cantidad_menores_10 = 0
    cantidad_entre_20_y_50 = 0
    cantidad_mayores_100 = 0

    # Ingresar números hasta que se ingrese un número negativo
    while True:
        numero = int(input("Ingrese un número entero positivo (ingrese un número negativo para finalizar): "))

        # Verificar si se ingresó un número negativo para finalizar
        if numero < 0:
            break

        # Actualizar contadores y acumuladores
        total_numeros += 1

        if numero % 2 == 0:
            total_pares += 1
            suma_pares += numero
        else:
            suma_impares += numero

        if numero < 10:
            cantidad_menores_10 += 1
        elif 20 <= numero <= 50:
            cantidad_entre_20_y_50 += 1
        elif numero > 100:
            cantidad_mayores_100 += 1

    # Calcular promedios
    promedio_pares = suma_pares / total_pares if total_pares > 0 else 0
    promedio_impares = suma_impares / (total_numeros - total_pares) if (total_numeros - total_pares) > 0 else 0

    # Mostrar el reporte
    print("\nReporte:")
    print(f"a. Total de números ingresados: {total_numeros}")
    print(f"b. Total de números pares ingresados: {total_pares}")
    print(f"c. Promedio de los números pares: {promedio_pares:.2f}")
    print(f"d. Promedio de los números impares: {promedio_impares:.2f}")
    print(f"e. Cuantos números son menores que 10: {cantidad_menores_10}")
    print(f"f. Cuantos números están entre 20 y 50: {cantidad_entre_20_y_50}")
    print(f"g. Cuantos números son mayores que 100: {cantidad_mayores_100}")

if __name__ == "__main__":
    main()
