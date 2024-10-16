# Git - Comandi Base

Questo documento ti aiuterà a capire e usare i comandi più comuni di **Git**, uno strumento che gli sviluppatori usano per salvare le versioni del codice e lavorare in squadra.

### 1. **Configura Git**

Prima di iniziare, devi dire a Git chi sei. Questo serve per tenere traccia di chi fa le modifiche.

```bash
git config --global user.name "Il Tuo Nome"
git config --global user.email "la.tua.email@example.com"
```

### 2. **Scaricare un progetto (Clonare un repository)**

Se vuoi lavorare su un progetto che è già su internet (ad esempio su GitHub), puoi scaricarlo sul tuo computer con questo comando:

```bash
git clone https://github.com/username/progetto.git
```

### 3. **Crea un nuovo progetto (Inizializzare un repository)**

Se invece stai iniziando un nuovo progetto sul tuo computer, devi creare un "repository" (una cartella che Git controllerà per le modifiche).

```bash
git init
```

### 4. **Aggiungere un repository remoto**

Se hai creato un nuovo repository con `git init`, puoi collegarlo a un repository remoto (ad esempio su GitHub) usando il comando `git remote add`. Questo ti permette di caricare e scaricare le modifiche tra il tuo computer e GitHub.

```bash
git remote add origin https://github.com/username/progetto.git
```

- `origin` è il nome che di solito si dà al repository remoto principale.
- L'URL è l'indirizzo del repository su GitHub o un altro servizio.

### 5. **Controlla lo stato dei file**

Questo comando ti dice quali file hai modificato, quali sono pronti per essere salvati e se ci sono problemi da risolvere.

```bash
git status
```

### 6. **Aggiungi file alla "storia" (Stage dei file)**

Quando hai fatto delle modifiche che vuoi salvare, devi prima "preparare" i file con questo comando:

- Per preparare **tutti i file** modificati:

  ```bash
  git add .
  ```

- Per preparare un **singolo file**:
  ```bash
  git add nomefile
  ```

### 7. **Salva le modifiche (Commit)**

Dopo aver preparato i file, salvali definitivamente nella "storia" di Git. Ogni volta che fai un commit, dovresti scrivere un messaggio che descriva le modifiche fatte.

- Questo comando salva solo i file che hai preparato con `git add`:

  ```bash
  git commit -m "Ho fatto queste modifiche"
  ```

- Se vuoi salvare **tutti i file modificati** senza doverli prima aggiungere manualmente, usa `-a` (che significa "add all"):
  ```bash
  git commit -a -m "Ho fatto queste modifiche"
  ```
  **Attenzione**: `git commit -a` non aggiunge file nuovi; solo quelli già tracciati.

### 8. **Vedi la cronologia (Log)**

Puoi vedere tutti i salvataggi (commit) che hai fatto con questo comando:

```bash
git log
```

### 9. **Carica le tue modifiche online (Push)**

Se stai lavorando su un progetto con altre persone, devi caricare le tue modifiche su un server (ad esempio su GitHub). Questo comando invia le modifiche salvate (commit) al progetto online.

```bash
git push origin main
```

### 10. **Scarica le modifiche di altri (Pull)**

Se stai lavorando in squadra e qualcuno ha fatto delle modifiche, puoi aggiornare il tuo progetto locale per avere anche le loro modifiche.

```bash
git pull origin main
```

### 11. **Lavora su una nuova parte (Branch)**

Quando vuoi lavorare su una nuova parte del progetto senza toccare il codice principale, puoi creare un "branch" (ramo) per tenere separate le tue modifiche. Dopo aver finito di lavorare sul branch, puoi unire le tue modifiche nel progetto principale.

- Crea un nuovo branch e spostati su di esso:
  ```bash
  git checkout -b nuovo-branch
  ```

### 12. **Unire il tuo lavoro (Merge)**

Quando hai finito di lavorare sul tuo branch, puoi unire (merge) le modifiche nel progetto principale:

```bash
git checkout main
git merge nuovo-branch
```

### 13. **Stash delle modifiche**

Se hai fatto delle modifiche ma non sei pronto a fare un commit, puoi metterle "in sospeso" con `git stash`. Questo ti permette di pulire il tuo ambiente di lavoro senza perdere le modifiche.

```bash
git stash -m "Commento descrittivo delle modifiche"
```

Quando sei pronto a riprendere il lavoro, puoi ripristinare le modifiche con:

```bash
git stash pop
```

### 14. **Gestire gli stash**

Puoi vedere un elenco delle modifiche messe in stash con:

```bash
git stash list
```

Per applicare uno specifico stash:

```bash
git stash apply stash@{n}
```

Dove `n` è l'indice dello stash nella lista.

---

### Suggerimenti per l'uso di Git

- **Fai commit frequenti**: è meglio fare piccoli cambiamenti e salvarli spesso.
- **Scrivi messaggi chiari**: quando fai un commit, scrivi chiaramente cosa hai modificato.
- **Usa i branch per nuove funzionalità**: quando stai lavorando su qualcosa di nuovo o fai esperimenti, usa un branch per tenere il codice principale pulito.

Buon lavoro con Git! 🎉
