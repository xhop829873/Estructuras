class NodoDoble:
    def _init_(self,dato): #se definen los nodosDobles
        self.dato=dato
        self.siguiente=None # se define como nulo el apuntadro hacia adelante
        self.anterior=None # se define como nulo el apuntador hacia atras

class ListaDoble:
    def _init_(self):
        self.cabeza=None #se define la caneza como nula(el inicio de la lista)
        self.cola=None  # se defin la cola de la lista como nula,( el final)
    def agregar(self,dato): # la funcion para agregar al final se dfefine
        nuevo=NodoDoble(dato) # crea un nuevo nododoble con el dato
        if not self.cabeza: # se comprueba si la lista esta vacia o no
            self.cabeza=nuevo
            self.cola=nuevo #si resulta estar vacia se indica que tanto la cabeza como la cola son el nuevo nodo que se va a ingresar
        else: #esto es si ya tieene datos la lista
            self.cola.siguiente=nuevo #se posiciona en la cola e indica que el siguiente nodo que antes estaba en nulo ahora sera "nuevo"
            nuevo.anterior=self.cola  #coloca el puntero hacia el anterior
            self.cola=nuevo #ahora al estar posicionado en la cola indica que esta sera "nuevo"
    
    def adelante(self): # se define el metodo para recorrer de atras hacia adelante la lista 
        actual=self.cabeza # define actual como la cabeza
        while actual:
            print(actual.dato) # mientras actual eexista mostrara el dato que este contiene
            actual=actual.siguiente # hace que se mueva al nodo siguiente
        print("None") #indica el final de la lista(que ya se recorrio toda)
        
    def atras(self): # con este se recorre del fianl al princiio
        actual=self.cola # define la cola como el actual
        while actual:
            print(actual.dato) #hace lo mismo que el metodo adelante solo que este en vez de recorrer hacia adelante la lista la recorre hacia atras
            actual=actual.anterior
        print("None")

l1=ListaDoble()
l1.agregar(456)
l1.agregar(444)
l1.agregar(555)
l1.agregar(678)

l1.adelante()
l1.atras()
