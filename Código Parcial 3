###Códigos parte práctica###
##Se tomó la opción de la implementación de un conjunto de ejemplos de aplicación de programación asincrónica###
##Se realizaron 3 ejemplos##
##Ejemplo 1 Simular un servidor web asincrónico##

import asyncio

async def manejar_solicitud(id_solicitud):
    print(f"Solicitud {id_solicitud} iniciada...")
    await asyncio.sleep(2)  # Simula una espera de 2 segundos (como si fuera una consulta de base de datos)
    print(f"Solicitud {id_solicitud} completada.")

async def servidor():
    tareas = []
    for i in range(1, 6):  # Simula 5 solicitudes
        tarea = asyncio.create_task(manejar_solicitud(i))
        tareas.append(tarea)
    await asyncio.gather(*tareas)  # Ejecuta todas las tareas simultáneamente

await servidor()  


##Ejemplo 2 Simular una búsqueda de archivos ##

async def buscar_archivo(directorio, archivo):
    print(f"Buscando '{archivo}' en {directorio}...")
    await asyncio.sleep(3)  # Simula la espera de una búsqueda que demora 3 segundos
    print(f"Archivo '{archivo}' encontrado en {directorio}.")

async def main():
    directorios = ['Directorio A', 'Directorio B', 'Directorio C']
    archivos = ['archivo1.txt', 'archivo2.txt', 'archivo3.txt']

    # Crear tareas asincrónicas para buscar archivos
    tareas = []
    for i in range(len(directorios)):
        tarea = asyncio.create_task(buscar_archivo(directorios[i], archivos[i]))
        tareas.append(tarea)

    await asyncio.gather(*tareas)

await main()

##Ejemplo 3 Simular un proceso de pago##

async def procesar_pago(id_pago):
    print(f"Iniciando procesamiento de pago {id_pago}...")
    await asyncio.sleep(5)  # Simula la espera de 5 segundos para procesar el pago
    print(f"Pago {id_pago} procesado correctamente.")

async def main():
    pagos = [1, 2, 3, 4, 5]

    # Procesar pagos de manera asincrónica
    tareas = [procesar_pago(pago) for pago in pagos]
    await asyncio.gather(*tareas)


await main()
