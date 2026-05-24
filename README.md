 MATRIZ DEL INVENTARIO
inventario = [
    [101, "Cuadernos", 5, 10],
    [102, "Lapices", 20, 15],
    [103, "Borradores", 3, 8],
    [104, "Marcadores", 12, 12],
    [105, "Colores", 2, 6]
]

# FUNCION PARA CALCULAR LA CANTIDAD A PEDIR
def calcular_pedido(stock_actual, stock_minimo):

    # Verifica si el stock actual es menor al mínimo
    if stock_actual < stock_minimo:

        # Calcula la diferencia
        cantidad = stock_minimo - stock_actual

    else:
        # Si el stock es suficiente
        cantidad = 0

    return cantidad


# MOSTRAR LISTA DE PEDIDOS
print("LISTA DE PEDIDOS")
print("---------------------------")

# RECORRER LA MATRIZ
for articulo in inventario:

    codigo = articulo[0]
    nombre = articulo[1]
    stock_actual = articulo[2]
    stock_minimo = articulo[3]

    # LLAMAR LA FUNCION
    pedido = calcular_pedido(stock_actual, stock_minimo)

    # MOSTRAR RESULTADOS
    print("Articulo:", nombre)
    print("Cantidad a pedir:", pedido)
    print("---------------------------")
