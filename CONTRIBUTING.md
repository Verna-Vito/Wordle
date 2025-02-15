# 🚀 Linee Guida per Contribuire

Grazie per voler contribuire a questo progetto! 🎉  
Per mantenere il repository organizzato e garantire un ambiente di sviluppo produttivo, segui queste linee guida quando apri una **Issue** o una **Pull Request**.

---

## 📝 Come Aprire una Issue
Quando apri una nuova **issue**, segui queste regole:

- Ogni issue di qualsiasi tipo, deve avere la/e label(s) che indicano il tipo (feature, pbi, bug, ...), devono essere collegate ad una milestone e devono essere inserite all'interno della project board di progetto.
- **Ogni issue deve essere collegata a una milestone**, se applicabile.
- **Le issue feature devono avere almeno una PBI collegata**.

### **📌 Convenzione per i Titoli delle Issue**
- `[FEATURE #<numero>] - Breve descrizione` → Per richieste di nuove funzionalità. 
- `[PRODUCT BACKLOG ITEM] - PBI #<numero> - Breve descrizione` → Per richieste figle di una funzionalità.
- `[BUG #<numero>] - Breve descrizione` → Per segnalare un problema o malfunzionamento.  

### **🛠 Struttura consigliata per una Issue**
Quando crei una issue, usa questa struttura per facilitarne la comprensione:
- Descrizione → Descrivi chiaramente il problema o la funzionalità richiesta
- Criteri di Accettazione → ✅ Lista puntata con i criteri di successo

📌 **Esempio di Issue di tipo feature:**  
```
[FEATURE 102] - Aggiungere la modalità hard

### Descrizione
In questa modalità, il giocatore deve obbligatoriamente riutilizzare le lettere corrette nei tentativi successivi.

### Criteri di Accettazione
✅ Il giocatore deve riutilizzare lettere corrette nei tentativi successivi.  
✅ Se non segue la regola, il gioco deve mostrare un avviso.  
```

#### Passaggi per riprodurre il problema (solo per bug)
- (Primo passaggio)
- (Secondo passaggio)
- (Risultato atteso vs risultato effettivo)
- Ambiente di sviluppo
- Java Version: X
- OS: Windows/Linux/macOS
- Gradle Version: X

📌 **Esempio di Issue di tipo bug:**  
```
[BUG] - Il feedback delle lettere non è corretto

Descrizione
Quando il giocatore inserisce una parola con lettere duplicate, il feedback colorato non è corretto.

Criteri di Accettazione
✅ Il feedback deve rispettare le regole di Wordle.
✅ Le lettere duplicate devono essere gestite correttamente.

Passaggi per riprodurre il problema
Avvia il gioco.
Inserisci la parola "LIVRE" quando la parola segreta è "VIRUS".
Il feedback dovrebbe mostrare solo la "V" in verde e la "I" in giallo, ma attualmente non lo fa.
```

---

## 🔀 Creare una Pull Request (PR)
La PR va collegata alla milestone ma non alla project board.

Prima di aprire una PR, assicurati di:
1. Aver creato un **branch separato** per il tuo lavoro.  
2. Aver scritto **commit chiari e descrittivi**.  
3. Aver eseguito `./gradlew build` per verificare che il codice funzioni.  

### 📌 **Convenzione per i Titoli delle PR**
`PR - Issue #<numero> | Titolo dell'issue che si vuole chiudere`

#### 📌 **Esempio di PR**
PR - Issue #34 | Aggiunto supporto per il feedback visivo delle lettere

#### **📜 Struttura consigliata per una PR**
Ogni PR dovrebbe seguire questa struttura:

```
## 📌 Descrizione
Questa pull request implementa le modifiche richieste nell'[Issue #34](https://github.com/Verna-Vito/Wordle/issues/34).

### 🔧 Modifiche Apportate
- Implementata la logica per il feedback visivo delle lettere.
- Aggiunti nuovi test unitari per la funzionalità.

### ✅ Issue Correlata
Closes #34

### 🔍 Test e Verifiche
- [x] Il gioco fornisce correttamente il feedback visivo.
- [x] I test unitari passano con successo.
```

## 🔀 Flusso di Lavoro Git

Per mantenere un repository ordinato e un flusso di sviluppo chiaro, segui queste regole quando lavori con i branch e le PR.

### 📌 Regole sui Branch
- **Ogni issue deve avere un branch dedicato** con il nome `issue#<numero>` (es. `issue#21`).
- **Le PR devono essere aperte da `issue#<numero>` a `dev`**.
- **Dopo il merge in `dev`, il branch `issue#<numero>` deve essere eliminato**.
- **Il branch `dev` non deve mai essere cancellato**.
- **Non devono essere aperte PR da `dev` a `main`**, perché il rilascio su `main` avviene automaticamente quando viene chiusa una milestone.

### 🔧 Procedura per aprire una PR
1. Crea un nuovo branch dal branch `dev`:
   ```
   git checkout dev
   git pull origin dev
   git checkout -b issue#<numero>
   ```
2. Implementa le modifiche e fai i commit con un messaggio chiaro:
    ```
    git commit -m "Fix #<numero>: Breve descrizione della modifica"
    ```
3. Pusha il branch remoto:
    ```
    git push origin issue#<numero>
    ```
4. Apri una PR da issue#<numero> a dev e segui le Linee Guida per le PR. Una volta che la PR è mergiata, elimina il branch locale e remoto:
    ```
    git branch -d issue#<numero>
    git push origin --delete issue#<numero>
    ```

### 🚀 Pipeline di Rilascio
Il branch main rappresenta solo le versioni rilasciate.
La pipeline di rilascio viene avviata automaticamente alla chiusura della milestone.
Non devono essere aperte PR manuali da dev a main.

---
📌 Per ulteriori dettagli, consulta il [README.md](README.md) per le istruzioni generali.

Grazie per il tuo contributo! 🚀
