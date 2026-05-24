# ============================================
# PROBLEMA 3 - AUDITORÍA DE INVENTARIO
# ============================================

# Matriz de artículos
# [Código, Nombre, Stock Actual, Stock Mínimo]

inventario = [
    [101, "Cuadernos", 15, 20],
    [102, "Lapices", 30, 25],
    [103, "Borradores", 8, 15],
    [104, "Marcadores", 12, 12],
    [105, "Reglas", 5, 10]
]

# --------------------------------------------
# Función para calcular cantidad a pedir
# --------------------------------------------

def calcular_pedido(stock_actual, stock_minimo):
    
    # Si el stock actual es menor al mínimo
    if stock_actual < stock_minimo:
        
        # Se calcula la diferencia
        cantidad = stock_minimo - stock_actual
    
    # Si el stock es suficiente
    else:
        cantidad = 0
    
    return cantidad


# --------------------------------------------
# Informe de pedidos
# --------------------------------------------

print("===== INFORME DE REABASTECIMIENTO =====\n")

# Recorrer la matriz
for articulo in inventario:
    
    codigo = articulo[0]
    nombre = articulo[1]
    stock_actual = articulo[2]
    stock_minimo = articulo[3]
    
    # Llamar la función
    pedido = calcular_pedido(stock_actual, stock_minimo)
    
    # Mostrar resultados
    print("Artículo:", nombre)
    print("Código:", codigo)
    print("Stock Actual:", stock_actual)
    print("Stock Mínimo:", stock_minimo)
    print("Cantidad a Pedir:", pedido)
    print("-----------------------------------")
