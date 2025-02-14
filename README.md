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
2. Scarica l'ultima versione disponibile (`wordle.jar`).
3. Esegui il gioco con il seguente comando:
   ```
   java -jar wordle.jar
   ```
### 🔧 Opzione 2: Buildare il Progetto con Gradle
Se non è disponibile una release o se la release è danneggiata, puoi compilare il progetto manualmente.

1. Installare Gradle (se non lo hai già)
   - Verifica se Gradle è installato:
      ```
      gradle -v
      ```
    - Se Gradle non è installato, puoi usare Gradle Wrapper fornito nel progetto:
      ```
        ./gradlew build   # Linux/macOS
        gradlew.bat build # Windows
       ```
2. Clonare la Repository
   ```
    git clone https://github.com/user/repo.git
    cd repo
   ```
3. Compilare ed Eseguire il Progetto
    Per buildare il progetto ed eseguire il gioco:
    ```
    ./gradlew build   # Linux/macOS
    gradlew.bat build # Windows
    java -jar build/libs/wordle-java.jar
   ```

## 🛠 Tecnologie Utilizzate
- Java 1.8 🟦
- Gradle ⚙️
- JUnit 5 (per i test) ✅
- Checkstyle (per la qualità del codice) 🔍

## 📢 Contatti e Supporto
Se hai problemi o suggerimenti, apri una issue con label **`question`** nella repository.