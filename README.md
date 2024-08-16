# Kj
Pequeños trabajos de la universidad
# Pedir valores
monto_inicial = float(input("Ingresa el monto inicial: "))
tasa_interes_anual = float(input("Ingresa el interés anual: "))
num_total_pagos = int(input("Número total de pagos: "))
pagos_realizados = int(input("Número de pagos realizados: "))
mensualidad = tasa_interes_anual 
Total = num_total_pagos + tasa_interes_anual + mensualidad

tasa_interes_mensual = tasa_interes_anual / 12 / 100
def calcular_saldo_insoluto(monto_inicial, tasa_interes_anual, num_total_pagos, pagos_realizados):
    # Convertir la tasa de interés anual a mensual
    tasa_interes_mensual = tasa_interes_anual / 12 / 100
    
    # Calcular la cuota mensual 
    cuota_mensual = monto_inicial * (tasa_interes_mensual * (1 + tasa_interes_mensual)**num_total_pagos) / ((1 + tasa_interes_mensual)**num_total_pagos - 1)
    
    # Calcular el saldo insoluto 
    saldo_insoluto = monto_inicial * (1 + tasa_interes_mensual)**pagos_realizados - (cuota_mensual * ((1 + tasa_interes_mensual)**pagos_realizados - 1) / tasa_interes_mensual)
    
    return saldo_insoluto
    # Calcular la cuota fija mensual

cuota_fija = monto_inicial * tasa_interes_mensual / (1 - (1 + tasa_interes_mensual)**-num_total_pagos)
print(f"La cuota fija mensual es: {cuota_fija:.2f}")
# Calculo
saldo_insoluto = calcular_saldo_insoluto(monto_inicial, tasa_interes_anual, num_total_pagos, pagos_realizados)

print(f"El saldo insoluto es: {saldo_insoluto:.2f}")
print(f"El monto total tiene un valor de {Total:.2f}")
total_pagado = cuota_fija * num_total_pagos
total_intereses = total_pagado - monto_inicial

print(f"La cuota fija mensual es: {cuota_fija:.2f}")
print(f"El total pagado al final del préstamo será: {total_pagado:.2f}")
print(f"El total de intereses pagados será: {total_intereses:.2f}")


#Python
#Visiaul Studio
#Santiago Anillo, NIcoll Aparicio
