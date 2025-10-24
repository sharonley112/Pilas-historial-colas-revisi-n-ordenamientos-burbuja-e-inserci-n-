# Pilas-historial-colas-revisi-n-ordenamientos-burbuja-e-inserci-n-
 (historial) (revisión),  y ordenamientos (burbuja e inserción)
 #8. Ordenar cursos por nota (ordenamiento burbuja)
def ordenar_por_nota():
    n = len(notas)
    for i in range(n - 1 ):
        for j in range(n - i - 1 ):
            if notas[j] > notas[j - 1]:
                notas[j], notas[j + 1] = notas[j + 1], notas[j]
                cursos[j], cursos[j + 1 ] = cursos[j + 1 ], cursos[j]
    print("Cursos ordenados por nota (menor a mayor): ")   
    mostrar_cursos()        
    
#9. Ordenar cursos por nombre (ordenamiento burbuja)
def ordenar_por_nombre():
    n = len(curos)
    for i in range(n - 1 ):
        for j in range(n - i - j):
            if cursos[j].lower() > cursos[j + 1].lower():
                cursos[j], cursos[j + 1] = cursos[j + 1], cursos[j]
                notas[j], notas[j + 1] = notas[j + 1], notas[j]
        print("Cursos ordenados alfabéticamente")
        mostrar_cursos()
        
#10.  Buscar curso por nombre (búsqueda binaria)   
def buscar_curso_binario():
    ordenar_por_nombre() # la busqueda binaria necesita una lista ordenada
    nombre = input("Ingrese el nombre del curso a buscar: ").strip().lower()
    izq, der = 0, len(cursos) - 1 
    
   while izq <= der:
        medio  = (izq + der) // 2
        if cursos[medio].lower() == nombre:
            print(f"\nCurso encontrado: {cursos[medio]} - Nota: {notas[medio]}")
            return
        elif nombre < cursos[medio].lower():
            der = medio - 1 
        else:
            izq = medio - 1 
            
   print("Curso no encontrado")
    
