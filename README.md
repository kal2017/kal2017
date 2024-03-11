ListaDeMercado
	Definir lista[100] Como Cadena
	Definir opcion, i, j, eliminar Como Entero
	
	opcion <- 0
	i <- 0
	
	Mientras opcion <> 4 Hacer
		Escribir "----------- Lista de Mercado -----------"
		Escribir "1. Agregar producto"
		Escribir "2. Mostrar lista"
		Escribir "3. Eliminar producto"
		Escribir "4. Salir"
		Escribir "-----------------------------------------"
		Escribir "Seleccione una opción: "
		Leer opcion
		
		Segun opcion Hacer
			1:
				Escribir "Ingrese el nombre del producto: "
				Leer lista[i]
				i <- i + 1
			2:
				Escribir "----------- Lista de Mercado -----------"
				Para j <- 0 Hasta i - 1 Hacer
					Escribir j + 1, ". ", lista[j]
				FinPara
				Escribir "-----------------------------------------"
			3:
				Si i > 0 Entonces
					Escribir "Ingrese el número del producto a eliminar: "
					Leer eliminar
					Si eliminar > 0 Y eliminar <= i Entonces
						Para j <- eliminar - 1 Hasta i - 2 Hacer
							lista[j] <- lista[j + 1]
						FinPara
						i <- i - 1
					Sino
						Escribir "Número de producto no válido."
					FinSi
				Sino
					Escribir "La lista está vacía."
				FinSi
			4:
				Escribir "¡Hasta luego!"
			De Otro Modo:
				Escribir "Opción no válida. Por favor, seleccione una opción válida."
		FinSegun
	FinMientras
