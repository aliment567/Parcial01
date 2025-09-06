#Parcial - 4
---
##1. Estructural

El error está en la línea 11 del código, falta un paréntesis de cierre al final de la instrucción print para que el código funcione correctamente.

Aquí está el código con el error:
def invertir_lista(lista):
    for i in range(len(lista)//2):
        temp = lista[i]
        lista[i] = lista[len(lista)-i-1]
        lista[len(lista)-i-1] = temp
    return lista

print(invertir_lista([1,2,3,4,5])

Aquí sin el error:
def invertir_lista(lista):
    for i in range(len(lista)//2):
        temp = lista[i]
        lista[i] = lista[len(lista)-i-1]
        lista[len(lista)-i-1] = temp
    return lista

print(invertir_lista([1,2,3,4,5]))
---
##2. OOP

En este código no hay un error de sintaxis, sino un error lógico relacionado con la condición al retirar dinero en la línea 9.
Se usa <, lo que impide retirar todo el saldo disponible.
Al usar <=, se permite retirar una cantidad menor o igual al saldo, incluyendo el total.

Código con el error lógico:
class CuentaBancaria:
    def __init__(self, titular, saldo):
        self.titular = titular
        self.saldo = saldo
    def retirar(self, cantidad):
        if cantidad < self.saldo:
            self.saldo = self.saldo - cantidad
        else:
            print('Fondos insuficientes')

c = CuentaBancaria('Ana', 100)
c.retirar(150)

Código sin el error lógico:
class CuentaBancaria:
    def __init__(self, titular, saldo):
        self.titular = titular
        self.saldo = saldo
    def retirar(self, cantidad):
        if cantidad <= self.saldo:
            self.saldo = self.saldo - cantidad
        else:
            print('Fondos insuficientes')

c = CuentaBancaria('Ana', 100)
c.retirar(150)
ias, videojuegos, sistemas de inventario, plataformas educativas, etc.

---

¡Éxito en el examen!
