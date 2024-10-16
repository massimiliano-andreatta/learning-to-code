# Introduzione alla Programmazione Orientata agli Oggetti (OOP)

## Cos'è la Programmazione Orientata agli Oggetti?

La Programmazione Orientata agli Oggetti (OOP) è un paradigma di programmazione che utilizza "oggetti" per rappresentare dati e metodi. Questo approccio è particolarmente utile per gestire applicazioni complesse, poiché facilita l'organizzazione del codice e la sua riutilizzabilità.

### Concetti Fondamentali dell'OOP

1. **Oggetti**:

   - Gli oggetti sono istanze di classi e rappresentano entità del mondo reale o concetti astratti. Ogni oggetto ha uno stato (definito dalle sue proprietà) e un comportamento (definito dai suoi metodi).
   - Esempio: un oggetto `Cane` potrebbe avere proprietà come `nome` e `razza`, e metodi come `abbaia()` o `mangia()`.

2. **Classi**:

   - Una classe è un modello o un "blueprint" per creare oggetti. Essa definisce le proprietà e i metodi comuni a tutti gli oggetti che ne derivano.
   - Esempio: una classe `Animale` potrebbe avere proprietà come `nome` e `età`, e metodi come `parla()`.

3. **Interfacce**:

   - Un'interfaccia è un contratto che definisce un insieme di metodi che una classe deve implementare. Le interfacce non contengono implementazioni di metodi, solo le loro dichiarazioni.
   - Esempio: un'interfaccia `Volante` potrebbe dichiarare un metodo `vola()`, che dovrebbe essere implementato da classi come `Uccello` e `Aereo`.

4. **Incapsulamento**:

   - Questo concetto si riferisce alla pratica di nascondere i dettagli interni di un oggetto e mostrare solo le funzionalità necessarie. Utilizzando modificatori di accesso (pubblico, privato, protetto), si controlla l'accesso ai dati e ai metodi.
   - Esempio: le proprietà di un oggetto possono essere private, consentendo l'accesso solo tramite metodi pubblici (getter e setter).

5. **Ereditarietà**:

   - Permette a una classe (detta classe derivata) di ereditare le proprietà e i metodi di un'altra classe (detta classe base). Questo consente di riutilizzare il codice e di creare una gerarchia di classi.
   - Esempio: una classe `Cane` può estendere la classe `Animale`, ereditando le sue proprietà e metodi.

6. **Polimorfismo**:
   - Consente a un'unica interfaccia di essere utilizzata per rappresentare diversi tipi di oggetti. Ciò significa che un metodo può comportarsi in modo diverso a seconda dell'oggetto su cui viene invocato.
   - Esempio: sia un oggetto `Cane` che un oggetto `Gatto` possono implementare un metodo `parla()`, ma restituiranno output diversi quando invocati.

### Principi SOLID

I principi SOLID sono una serie di linee guida progettate per migliorare la progettazione del software orientato agli oggetti. Ecco una spiegazione dei principi:

1. **Modularità**:

   - Si riferisce alla suddivisione del codice in moduli indipendenti che possono essere sviluppati, testati e mantenuti separatamente. La modularità facilita la gestione del codice e consente di lavorare su parti specifiche senza influenzare l'intero sistema.

2. **Riutilizzabilità**:

   - Questo principio implica che il codice può essere riutilizzato in più contesti o applicazioni. Le classi e le interfacce progettate in modo appropriato possono essere estese o implementate in nuovi progetti, riducendo il tempo e gli sforzi di sviluppo.

3. **Facilità di Manutenzione**:

   - Un codice ben progettato è più facile da mantenere. Gli aggiornamenti e le modifiche possono essere apportati con minor rischio di introdurre errori, grazie alla separazione delle preoccupazioni e alla modularità del codice.

4. **Rappresentazione Naturale**:
   - L'OOP consente di modellare il codice in modo che rappresenti concetti e oggetti del mondo reale. Ciò rende il codice più intuitivo e comprensibile, facilitando la comunicazione tra sviluppatori e stakeholders.

### Esempio di OOP in Java

Ecco un esempio di OOP in Java, con il codice suddiviso e commentato per facilitarne la comprensione:

```java
// Classe base per rappresentare un animale
class Animale {
    // Proprietà dell'animale
    String nome;

    // Costruttore per inizializzare il nome dell'animale
    Animale(String nome) {
        this.nome = nome;
    }

    // Metodo per far parlare l'animale (da sovrascrivere nelle classi derivate)
    void parla() {
        // Metodo vuoto
    }
}

// Classe derivata Cane che estende la classe Animale
class Cane extends Animale {
    // Costruttore per inizializzare il nome del cane
    Cane(String nome) {
        super(nome); // Chiamata al costruttore della classe base
    }

    // Implementazione del metodo parla per il cane
    @Override
    void parla() {
        System.out.println(nome + " dice: Woof!"); // Output specifico per il cane
    }
}

// Classe derivata Gatto che estende la classe Animale
class Gatto extends Animale {
    // Costruttore per inizializzare il nome del gatto
    Gatto(String nome) {
        super(nome); // Chiamata al costruttore della classe base
    }

    // Implementazione del metodo parla per il gatto
    @Override
    void parla() {
        System.out.println(nome + " dice: Meow!"); // Output specifico per il gatto
    }
}

// Interfaccia Volante che dichiara il metodo vola
interface Volante {
    void vola(); // Metodo da implementare
}

// Classe derivata Uccello che estende Animale e implementa Volante
class Uccello extends Animale implements Volante {
    // Costruttore per inizializzare il nome dell'uccello
    Uccello(String nome) {
        super(nome); // Chiamata al costruttore della classe base
    }

    // Implementazione del metodo parla per l'uccello
    @Override
    void parla() {
        System.out.println(nome + " dice: Ciao!"); // Output specifico per l'uccello
    }

    // Implementazione del metodo vola dell'interfaccia Volante
    @Override
    public void vola() {
        System.out.println(nome + " sta volando!"); // Output quando l'uccello vola
    }
}

// Classe principale per eseguire il programma
public class Main {
    public static void main(String[] args) {
        // Creazione di oggetti delle classi derivanti
        Cane cane = new Cane("Fido");
        Gatto gatto = new Gatto("Miao");
        Uccello uccello = new Uccello("Tweety");

        // Invocazione del metodo parla su ciascun oggetto
        cane.parla(); // Output: Fido dice: Woof!
        gatto.parla(); // Output: Miao dice: Meow!
        uccello.parla(); // Output: Tweety dice: Ciao!
        uccello.vola(); // Output: Tweety sta volando!
    }
}
```
