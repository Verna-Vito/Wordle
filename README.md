[![CI/CD](https://github.com/Verna-Vito/Wordle/actions/workflows/deploy.yml/badge.svg)](https://github.com/Verna-Vito/Wordle/actions/workflows/deploy.yml) [![Auto Merge Dev into Main](https://github.com/Verna-Vito/Wordle/actions/workflows/auto_merge_dev_to_main.yml/badge.svg)](https://github.com/Verna-Vito/Wordle/actions/workflows/auto_merge_dev_to_main.yml) [![Close Issues on PR Merge](https://github.com/Verna-Vito/Wordle/actions/workflows/close-issue.yml/badge.svg)](https://github.com/Verna-Vito/Wordle/actions/workflows/close-issue.yml)

# 🟩 Wordle 🟨  
Un'implementazione di Wordle in Java, sviluppata con Gradle.

## 🎮 Cos'è Wordle?
**Wordle** è un gioco di parole in cui il giocatore ha **sei tentativi** per indovinare una parola segreta di cinque lettere.  
Dopo ogni tentativo, il gioco fornisce un **feedback visivo** per aiutare il giocatore:  

✅ **Verde** → Lettera corretta nella posizione giusta.  
🟡 **Giallo** → Lettera presente, ma nella posizione sbagliata.  
⚪ **Grigio** → Lettera non presente nella parola segreta.  

L'obiettivo è trovare la parola segreta nel minor numero di tentativi possibile! 🎯  

---

## 🚀 Installazione e Esecuzione
### 📥 Opzione 1: Scaricare una Release Precompilata
1. Vai alla sezione [Releases](https://github.com/Verna-Vito/Wordle/releases) della repository.
2. Scarica l'ultima versione disponibile:  
   - **Versione CLI**: `Wordle-vX.Y.Z_Amelia.0-cli.jar`  
   - **Versione GUI**: `Wordle-vX.Y.Z_Amelia.0-gui.jar`  
3. Esegui il gioco con uno dei seguenti comandi:  
   - Per la versione **CLI**:  
     ```
     java -jar Wordle-vX.Y.Z_Amelia.0-cli.jar
     ```
   - Per la versione **GUI**:  
     ```
     java -jar Wordle-vX.Y.Z_Amelia.0-gui.jar
     ```
📌 **Nota:** X.Y.Z corrisponde alla versione rilasciata e "\<NomeRelease>" indica il nome assegnato alla release.

### 🔧 Opzione 2: Buildare il Progetto con Gradle
Se non è disponibile una release o se la release è danneggiata, puoi compilare il progetto manualmente.

1. Installare Gradle (se non lo hai già)
   - Verifica se Gradle è installato:
      ```
      gradle -v
      ```
    - Se Gradle non è installato, puoi usare Gradle Wrapper fornito nel progetto:
      - Per la versione **CLI**:  
         ```
         ./gradlew buildCli   # Linux/macOS
         gradlew.bat buildCli # Windows
         java -jar build/libs/wordle-cli.jar
         ```
      - Per la versione **GUI**:  
         ```
         ./gradlew buildGui   # Linux/macOS
         gradlew.bat buildGui # Windows
         java -jar build/libs/wordle-gui.jar
         ```
2. Clonare la Repository
   ```
    git clone https://github.com/Verna-Vito/Wordle.git
    cd Wordle
   ```
3. Compilare ed Eseguire il Progetto
   - Per la versione **CLI**:  
     ```
     ./gradlew buildCli   # Linux/macOS
      gradlew.bat buildCli # Windows
      java -jar build/libs/wordle-cli.jar
     ```
   - Per la versione **GUI**:  
     ```
     ./gradlew buildGui   # Linux/macOS
      gradlew.bat buildGui # Windows
      java -jar build/libs/wordle-gui.jar
     ```

📌 **Nota:** Dopo la build, il file eseguibile sarà disponibile nella cartella `build/libs/` con il nome:
- `wordle-cli.jar` per la versione CLI
- `wordle-gui.jar` per la versione GUI

## 🛠 Tecnologie Utilizzate
- Java 1.8 🟦
- Gradle ⚙️
- JUnit 5 (per i test) ✅
- Checkstyle (per la qualità del codice) 🔍

## 🤝 Come Contribuire
Vuoi contribuire al progetto? Dai un'occhiata alle nostre [Linee Guida per i Contributori](CONTRIBUTING.md) prima di aprire una Issue o una Pull Request.  
💡 **Ricorda:** Tutti i partecipanti devono rispettare il [Codice di Condotta](CODE_OF_CONDUCT.md). 🚀

## 📢 Contatti e Supporto
Se hai problemi o suggerimenti, apri una issue con label **`question`** nella repository.