# DictionaryApp
A simple and efficient Android Dictionary application built entirely in Kotlin. The app lets users search for English words and view phonetics, part of speech, definition, synonyms, antonyms, and example usage using the free Dictionary API.

---

## Features

- **Search Word**: Look up word definitions using the search field.
- **Phonetic & Part of Speech**: Displays phonetic spelling and part of speech.
- **Definition**: Shows the primary definition for the searched word.
- **Synonyms & Antonyms**: Displays synonyms and antonyms when available.
- **Example Usage**: Shows an example sentence when available.
- **Clean Compose UI**: Built with Jetpack Compose and Material3.

---

### Usage

1. Launch the app on an emulator or device.
2. Type a word into the search field at the top.
3. Tap the search icon to fetch results.
4. View the word, phonetic, part of speech, definition, synonyms/antonyms, and example in the result cards.

---

### Code Structure

- **Model**
app/src/main/java/com/dinakaran/dictionaryapp/model/
Contains data classes (DictionaryData, Meaning, Definition) and network setup (RetrofitInstance, DictionaryApi).
Network: Uses Retrofit + GsonConverterFactory to call https://api.dictionaryapi.dev (no API key required).

- **View**
app/src/main/java/com/dinakaran/dictionaryapp/view/
UI composables implemented with Jetpack Compose. Main UI is DictionaryScreen.kt which renders the search field and result cards.

- **ViewModel**
app/src/main/java/com/dinakaran/dictionaryapp/viewmodel/
DictionaryViewModel handles search logic, coroutine usage, and exposes observable state for the UI.

- **Entrypoint**
app/src/main/java/com/dinakaran/dictionaryapp/MainActivity.kt
Sets up the Compose theme and provides DictionaryViewModel to DictionaryScreen.

---

### Technologies Used

- **Kotlin** — 100% Kotlin-based application.
- **Jetpack Compose (Material3)** — UI toolkit.
- **Retrofit** — HTTP client.
- **Gson Converter** — JSON parsing for Retrofit.
- **Coroutines** — Asynchronous network calls (viewModelScope).
- **AndroidX ViewModel** — MVVM architecture.
- **Compose Column + verticalScroll** — UI layout for results.

---

## Getting Started

### Prerequisites

- Android Studio (Arctic Fox / Electric Eel / Bumblebee or newer recommended)
- JDK 11 or higher
- A connected Android device or emulator

---

### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/Dinakaran-k/DictionaryApp.git
    ```

2. Open the project in Android Studio:

    - File -> Open... -> select the cloned repository
    - Let Gradle sync and download dependencies
    
3. Build the project:

    - Click on `Build` -> `Make Project` or use the `Ctrl+F9` shortcut

4. Run the project:

    - Click on `Run` -> `Run 'app'` or use the `Shift+F10` shortcut
  
---

## Configuration

- The app uses the public Dictionary API at https://api.dictionaryapi.dev and does not require an API key.
- No additional configuration is required to run basic word lookups.
- If you want to change base URLs or network settings, edit: app/src/main/java/com/dinakaran/dictionaryapp/model/RetrofitInstance.kt

---

## Acknowledgments

- Dictionary data provided by  https://dictionaryapi.dev
- Thanks to the authors and maintainers of Retrofit, Gson, Jetpack Compose, and AndroidX libraries.
- Where to look in the code (quick links):

  - **MainActivity**: app/src/main/java/com/dinakaran/dictionaryapp/MainActivity.kt
  - **UI / Screen**: app/src/main/java/com/dinakaran/dictionaryapp/view/DictionaryScreen.kt
  - **ViewModel**: app/src/main/java/com/dinakaran/dictionaryapp/viewmodel/DictionaryViewModel.kt
  - **Models & API**: app/src/main/java/com/dinakaran/dictionaryapp/model/
