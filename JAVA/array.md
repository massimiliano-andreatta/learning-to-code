# Introduzione agli Array in Java

Questa guida introduce gli array in Java, una struttura dati fondamentale che permette di memorizzare e gestire collezioni di elementi dello stesso tipo.

## 1. Cos'è un Array?

Un **array** è una struttura dati che permette di memorizzare una serie di elementi dello stesso tipo, come numeri o stringhe, in una sola variabile. Ogni elemento in un array è accessibile tramite un indice numerico.

## 2. Creazione di un Array

Per creare un array in Java, segui questi passaggi:

1. **Dichiarazione**: specifichi il tipo di dati degli elementi dell'array e il nome dell'array.
2. **Inizializzazione**: crei un'istanza dell'array, specificando la sua dimensione (numero di elementi che può contenere).

**Esempio di creazione di un array di interi:**

```java
int[] numeri = new int[5];
```

Qui, `numeri` è un array di interi con spazio per 5 elementi.

## 3. Accesso agli Elementi di un Array

Ogni elemento in un array è numerato a partire da 0 (indice zero), quindi:

- Il primo elemento è all'indice 0.
- Il secondo elemento è all'indice 1.
- E così via...

**Esempio di accesso e modifica degli elementi:**

```java
numeri[0] = 10; // Assegna il valore 10 al primo elemento
numeri[1] = 20; // Assegna il valore 20 al secondo elemento

System.out.println(numeri[0]); // Stampa 10
System.out.println(numeri[1]); // Stampa 20
```

## 4. Lunghezza di un Array

La lunghezza di un array rappresenta il numero di elementi che può contenere. Puoi ottenere la lunghezza di un array con la proprietà `.length`.

**Esempio:**

```java
System.out.println("Lunghezza dell'array: " + numeri.length); // Stampa 5
```

## 5. Stampa degli Elementi di un Array

Per stampare tutti gli elementi di un array, possiamo usare un ciclo `for`.

**Esempio:**

```java
for (int i = 0; i < numeri.length; i++) {
    System.out.println("Elemento " + i + ": " + numeri[i]);
}
```

## 6. Passaggio del Riferimento di un Array a un Metodo

Quando passi un array a un metodo, il metodo riceve un **riferimento** all'array, non una copia. Questo significa che le modifiche apportate all'interno del metodo influenzeranno l'array originale.

**Esempio:**

```java
public static void modificaArray(int[] arr) {
    arr[0] = 100; // Cambia il primo elemento a 100
}

public static void main(String[] args) {
    int[] numeri = {1, 2, 3, 4, 5};
    modificaArray(numeri);
    System.out.println(numeri[0]); // Stampa 100
}
```

---

## Esercizio Pratico

Ecco un esercizio per applicare i concetti appresi:

1. **Crea un array** di 5 numeri interi e assegna valori diversi a ciascun elemento.
2. **Stampa** tutti i valori dell'array usando un ciclo `for`.
3. **Scrivi un metodo** che riceva un array come parametro e che cambi il valore dell'ultimo elemento in 99.
4. **Chiama il metodo** passando l’array creato e verifica che l’ultimo elemento sia cambiato.

**Suggerimento**: prova a risolvere l'esercizio da solo prima di consultare la soluzione.
