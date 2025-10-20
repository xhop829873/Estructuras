class Nodo():
    def _init_(self,dato):
        self.dato=dato
        self.siguiente=None #define el apuntador al siguiente nodo como nulo


class Lista:
    def _init_(self):
        self.primero=None #inicia como nulo el primer nodo
        
    def agregar(self,dato):
        nuevo=Nodo(dato) # crea el nodo con el dato a recibir
        if not self.primero: 
            self.primero=nuevo # vaida si no existe el nodo primero,si no existe define el nuevo nodo como primero
        else:
            actual=self.primero            # si ya existe el nodo primero define acual como el primero
            while actual.siguiente: # recorre toda la lista hasta llegar al ultimo nodo
                actual=actual.siguiente # iguala el ultio nodo con el nuevo que se va a gregar
            actual.siguiente=nuevo            
        return 1 
        
    
    def eliminar(self,dato):
        actual=self.primero
        anterior=None
        while actual and actual.dato!=dato: #recorre mientras existan los nodos y no coincidan con el dato buscad
            anterior=actual
            actual=actual.siguiente
        if not actual: # si no encuentra el dato no hace nada
            return
        if not anterior:
            self.primero=actual.siguiente #si el dato se encuentra en el primer nodo mueve el primero al siguiente para poderlo eliminar
        else:
            anterior.siguiente=actual.siguiente 
            
    
    def imprimir(self): # mediante esta funcion recorre toda la lista y la muestra con el print
        actual=self.primero
        while actual:
            print(actual.dato)
            actual=actual.siguiente

lili=Lista()
#print(type(lili))
lili.agregar('k')
lili.agregar(999)
lili.agregar(1000)

# l1.agregar(111)
# l1.eliminar(1112)
# l1.imprimir()
# l1.agregar(111)
# l1.agregar(333)
# l1.agregar(444)
# l1.imprimir()
# print("="*50)
# l1.eliminar(111)
# l1.imprimir(
