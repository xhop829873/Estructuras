class NodoDoble:
    def __init__(self, dato):
        # Guarda el valor del nodo
        self.dato = dato
        # Referencia al siguiente nodo
        self.siguiente = None
        # Referencia al nodo anterior 
        self.anterior = None
# ListaDoble: lista doblemente enlazada que además se mantiene circular
class ListaDoble:
    def __init__(self):
        # puntero al primer nodo de la lista
        self.cabeza = None
        # puntero al último nodo de la lista
        self.cola = None
        # Contador de nodos 
        self.cont = 0

    def agregar(self, dato):
        # Crea un nuevo nodo con el dato recibido
        nuevo = NodoDoble(dato)
        # Si la lista está vacía (no hay cabeza)
        if not self.cabeza:
            # El nuevo nodo pasa a ser la cabeza
            self.cabeza = nuevo
            # Y también la cola este seria el unico nodo
            self.cola = nuevo
        else:
            # Si ya hay elementos, enlazamos el último con el nuevo
            # El siguiente de la cola actual será el nuevo nodo
            self.cola.siguiente = nuevo
            # El nuevo nodo apunta hacia atrás a la cola anterior
            nuevo.anterior = self.cola
            # Actualizamos la cola para que sea el nuevo nodo agregado
            self.cola = nuevo

        # para mantener la circularidad el siguiente de la cola apunta a la cabeza
        self.cola.siguiente = self.cabeza
        # observamos la circularidad, la anterior de la cabeza apunta a la cola
        self.cabeza.anterior = self.cola
        # Incrementa el contador de nodos porque se agregó uno nuevo
        self.cont += 1

    def adelante(self):
        # Comenzamos a recorrer desde la cabeza
        actual = self.cabeza
        i = 0
        # Recorremos mientras exista nodo y no hayamos mostrado todos (evita bucle infinito)
        while actual and i < self.cont:
            # Imprime el dato del nodo actual
            print(actual.dato)
            # Avanza al siguiente nodo
            actual = actual.siguiente
            # Incrementa el índice del recorrido
            i += 1

    def atras(self):
        # Comenzamos a recorrer desde la cola (recorrido inverso)
        actual = self.cola
        i = 0
        # Recorremos mientras exista nodo y no hayamos mostrado todos (evita bucle infinito)
        while actual and i < self.cont:
            # Imprime el dato del nodo actual (desde atrás hacia adelante)
            print(actual.dato)
            # Retrocede al nodo anterior
            actual = actual.anterior
            # Incrementa el índice del recorrido
            i += 1


l1 = ListaDoble()
l1.agregar(456)
l1.agregar(444)
l1.agregar(555)
l1.agregar(678)

l1.adelante()         
print("=" * 50)
l1.atras() 
