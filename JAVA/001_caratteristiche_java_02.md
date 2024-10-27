# Guida Introductiva al Linguaggio di Programmazione Java

## 1. Cos'è Java? ☕

Java è un linguaggio di programmazione ad alto livello, orientato agli oggetti, progettato per essere portatile, sicuro e semplice da usare. È ampiamente utilizzato per lo sviluppo di applicazioni desktop, web e mobile.

## 2. Differenza tra Linguaggi Compilati e Interpretati ⚙️

- **Compilati**: Il codice sorgente è tradotto in codice macchina da un compilatore prima dell'esecuzione. Esempio: Java (compilato in bytecode).
- **Interpretati**: Il codice sorgente viene eseguito direttamente da un interprete. Esempio: JavaScript.

## 3. Tipi di Dato Primitivi in Java 📊

Java supporta otto tipi di dato primitivi:

- `int`: numeri interi (es. 5)
- `double`: numeri decimali (es. 5.75)
- `char`: caratteri singoli (es. 'a')
- `boolean`: valori veri o falsi (es. true, false)
- `byte`, `short`, `long`, `float`: varianti per diverse esigenze di memorizzazione

## 4. Oggetti di Sistema in Java 📦

### Stringhe

Le stringhe sono utilizzate per rappresentare sequenze di caratteri. Esempio:

```java
String nome = "Mario";
```

### Array

Un array è una struttura dati che memorizza una collezione di elementi dello stesso tipo. Esempio:

```java
int[] numeri = {1, 2, 3, 4, 5};
```

### Liste

Le liste sono collezioni dinamiche di elementi. In Java, puoi utilizzare `ArrayList` per gestire liste di dimensioni variabili. Esempio:

```java
import java.util.ArrayList;
ArrayList<String> nomi = new ArrayList<>();
nomi.add("Mario");
```

## 5. Concetti Fondamentali di OOP 🏗️

### Classe

Una classe è un modello per creare oggetti. Contiene attributi (variabili) e metodi (funzioni).

### Oggetto

Un oggetto è un'istanza di una classe. Rappresenta un'entità concreta con stato e comportamento.

### Interfaccia

Un'interfaccia è un contratto che definisce metodi che una classe deve implementare, senza fornire l'implementazione stessa.

### Metodo

Un metodo è un blocco di codice che esegue una specifica operazione. Può accettare parametri e restituire un valore.

### Metodo `main`

Il metodo `main` è il punto di ingresso di un'applicazione Java. La sua dichiarazione è:

```java
public static void main(String[] args) {
    // codice
}
```

## 6. Passaggio di Parametri: Per Valore e Per Riferimento 🔄

### Passaggio per Valore

Quando i tipi primitivi sono passati ai metodi, viene passata una copia del valore:

```java
int x = 5;
modificaValore(x); // x rimane 5
```

### Passaggio per Riferimento

Quando un oggetto è passato ai metodi, viene passato il riferimento all'oggetto:

```java
Punto p = new Punto(5, 10);
modificaPunto(p); // p.x viene modificato
```

## 7. Input e Output in Console 💻

### Richiesta di Input dall'Utente

Per ottenere input dall'utente, utilizza la classe `Scanner`:

```java
import java.util.Scanner;
Scanner scanner = new Scanner(System.in);
System.out.print("Inserisci il tuo nome: ");
String nome = scanner.nextLine();
scanner.close();
```

### Output in Console

Per stampare informazioni nella console, usa `System.out.println()`:

```java
System.out.println("Ciao, " + nome + "!");
```

## 8. Esempio Completo di Programma Java 📄

```java
import java.util.Scanner;

public class EsempioJava {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Inserisci il tuo nome: ");
        String nome = scanner.nextLine();

        System.out.print("Inserisci la tua età: ");
        int eta = scanner.nextInt();

        System.out.println("Ciao " + nome + ", hai " + eta + " anni.");
        scanner.close();
    }
}
```

## 9. Concetti Avanzati per Studenti 📚

### 9.1. Eccezioni

Le eccezioni sono eventi anomali che possono verificarsi durante l'esecuzione di un programma. È importante gestirle per evitare che il programma si interrompa. Utilizza `try`, `catch` e `finally` per gestire le eccezioni.

### 9.2. Classi Astratte e Metodi Astratti

Una **classe astratta** è una classe che non può essere istanziata e può contenere metodi astratti, che sono metodi senza implementazione. Le sottoclassi devono fornire un'implementazione per questi metodi.

### 9.3. Costruttori

Un **costruttore** è un metodo speciale utilizzato per inizializzare gli oggetti. Ha lo stesso nome della classe e non ha un tipo di ritorno.

```java
public class Punto {
    int x, y;

    // Costruttore
    Punto(int x, int y) {
        this.x = x;
        this.y = y;
    }
}
```

### 9.4. Overloading e Overriding

- **Overloading**: Consente di avere più metodi con lo stesso nome ma parametri diversi nella stessa classe.
- **Overriding**: Permette a una sottoclasse di fornire una specifica implementazione di un metodo già definito nella sua superclasse.

Buona programmazione! 🚀
