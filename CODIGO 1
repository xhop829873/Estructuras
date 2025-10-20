class Nodo:
    def __init__(self, dato):
        # Se guarda el dato que contendrá el nodo
        self.dato = dato
        # Puntero que apuntará al siguiente nodo 
        self.siguiente = None

# la Clase Circular define la estructura y operaciones de una lista circular simple
class Circular:
    def __init__(self):
        # Puntero al primer nodo de la lista 
        self.primero = None
        # Contador de elementos para mostrar o recorrer
        self.cont = 0
    # Método para agregar un nuevo nodo al final de la lista circular
    def agregar(self, dato):
        # Se crea un nuevo nodo con el dato recibido
        nuevo = Nodo(dato)
        # Si la lista está vacía (no hay primer nod)
        if not self.primero:
            # El nuevo nodo pasa a ser el primero
            self.primero = nuevo
            # Y su siguiente apunta a sí mismo (forma el círculo)
            nuevo.siguiente = self.primero
        # Si ya existen nodos en la lista
        else:
            # Se crea una variable auxiliar para recorrer la lista
            actual = self.primero
            # Recorremos la lista hasta encontrar el último nodo
            while actual.siguiente != self.primero:
                actual = actual.siguiente
                # Incrementamos el contador al recorrer cada nodo
                self.cont += 1
            # Una vez en el último nodo, lo conectamos con el nuevo
            actual.siguiente = nuevo
            # Y el nuevo nodo apunta al primero, manteniendo la circularidad
            nuevo.siguiente = self.primero
            # Aumentamos el contador total de nodos
            self.cont += 1
    # este metodo lo utilizamos para mostrar todos los elementos de la lista circular
    def mostrar(self):
        # Comenzamos desde el primer nodo
        actual = self.primero
        i = 0
        # Recorremos los nodos mientras no hayamos pasado por todos
        while actual and i < self.cont:
            # Mostramos el dato del nodo actual
            print(actual.dato)
            # Avanzamos al siguiente nodo
            actual = actual.siguiente
            i += 1

k = Circular()

k.agregar(12)
k.agregar(9)
k.agregar(88)
k.agregar(8800)
k.agregar(9988)
k.mostrar()
