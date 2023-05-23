#PRECIOS
PrecioCarillasPorcelana = 250000
PrecioImplantesDentales = 475000
PrecioOrtodonciaBrakets = 800000
#DESCUENTOS
DsctoAuxiliar = 0.85
DsctoAdministrativo = 0.9
DsctoDocente = 0.95
opc = 0
Descuentos = ['15%','10%','5%']
#DATOSCOTIZACION
contadorCarillas = 0 
contadorImplantes = 0
contadorOrtodoncia = 0
totalCarillas = 0
totalImplantes = 0
totalOrtodoncia = 0
subTotal = 0
while opc != 3:
    print("-"*30)
    print("\tMENU")
    print("-"*30)
    print("1.- Cotizacion\n2.- Renunciar\n3.- SALIR")
    try:
        opc = int(input())
    except:
        print("Ingrese Un N° De las opciones!!!")
    if opc == 1:
        while True:  #Preguntar por tipo de tratamiento
            while True:
                print("-"*30)
                print("Indique que tratamiento se desea realzar:")
                print("1.- Carillas Porcelana\n2.- Implantes Dentales\n3.- Ortodoncia Brakets\n4.- FINALIZAR COTIZACION")
                try:
                    opcTratamiento = int(input())
                    break
                except:
                    print("Ingrese Un N°!!!")
            flag = True
            if opcTratamiento in range(1,4):    #PREGUNTARLA CANTIDAD DE TRATAMIENTO QUE DESEA COtiZAR
                tratamientos = ['Carillas Porcelana','Implantes Dentales','Ortodoncia Brakets']
                print(f"¿Cuantos tratamientos de {tratamientos[opcTratamiento - 1]} desea cotizar?") 
                try:
                    cantidad = int(input())
                    if cantidad >= 1:
                        subTotal += [PrecioCarillasPorcelana, PrecioImplantesDentales,
                                    PrecioOrtodonciaBrakets][opcTratamiento - 1] * cantidad
                        if opcTratamiento == 1:
                            contadorCarillas += cantidad
                            totalCarillas += PrecioCarillasPorcelana * cantidad
                        elif opcTratamiento == 2:
                            contadorImplantes += cantidad
                            totalImplantes += PrecioImplantesDentales * cantidad
                        elif opcTratamiento == 3:
                            contadorOrtodoncia += cantidad
                            totalOrtodoncia += PrecioOrtodonciaBrakets * cantidad
                    else:
                        print("ingrese un N° mayor a 0")
                except:
                    print("Ingrese Un N°!!!")
            
            elif opcTratamiento == 4:
                while True:
                    print("-"*30)
                    print("¿Tiene Ud. alguno de los sgts Descuentos?")
                    print('''1.- Trabajador Auxiliar, se aplicará un descuesto del 15%
2.- Trabajador Administrativo, se aplica un descuento del 10%
3.- Trabajador Docente, descuento del 5% .
4.- NO tengo descuento''')
                    try:
                        tieneDescuento = int(input())
                        if tieneDescuento not in range(1,5):
                            print("Opcion no encontrada")
                        else:
                            break
                    except:
                        print("Ingrese Un N°!!!")
                print("-"*50)
                print("\t\tCOTIZACION")
                print("-"*50)
                if contadorCarillas >= 1:
                    print(f"--> {contadorCarillas}\t Tratamiento(s) Carillas Poecelana \t${totalCarillas}")
                if contadorImplantes >= 1:
                    print(f"--> {contadorImplantes}\t Tratamiento(s) Impantes Dentales \t${totalImplantes}")
                if contadorOrtodoncia >= 1:
                    print(f"--> {contadorOrtodoncia}\t Tratamiento(s) Ortodoncia Brakets \t${totalOrtodoncia}")
                print("-"*30)
                print(f"SubTotal \t\t${subTotal}")
                if tieneDescuento in range(1,4):
                    descuento = subTotal * [DsctoAuxiliar, DsctoAdministrativo, DsctoDocente][tieneDescuento - 1]
                    print(f"Descuento {Descuentos[tieneDescuento - 1]} \t\t${int(subTotal - descuento)}")
                    totalCompra = descuento
                else:
                    print("Descuento \t\tNO tiene descuento")
                    print("-"*30)
                    totalCompra = subTotal
                print(f"Toal \t\t\t${int(totalCompra)}")
                print("-"*30)
                valorCuotas = totalCompra/12
                print(f"Son 12 cuotas de: \t${int(valorCuotas)}")
                print("\nSonria BONITO!!!")
                break
            elif opcTratamiento not in range(1,5):
                print("Opcion fuerea de rango!!!")      
    elif opc == 2:
        contadorCarillas = 0 
        contadorImplantes = 0
        contadorOrtodoncia = 0
        totalCarillas = 0
        totalImplantes = 0
        totalOrtodoncia = 0
        subTotal = 0 
        print("-"*30)
        print("  DATOS REESTABLECIDOS!!!")
    elif opc not in range(1,4):
        print("OPCION INVALIDA!!!")        
