⚠️ **Polska wersja poniżej ⬇️**  
Polish version below – scroll down to read in Polish.
---

<br>

# 🧪 Flask REST API – Decision Model (Educational Project)

This is a simple REST API project written in Python using the **Flask** framework.  
The application exposes a few endpoints and a basic decision logic based on the sum of two numbers.

---

## 📁 Repository Contents

- `app.py` - Flask application source code  
- `requirements.txt` - List of required packages  
- `Dockerfile` - Docker container configuration
- `Lab2.ipynb` - Interactive notebook demonstrating REST API usage and test cases
- `README.md` - Project documentation and run instructions

---

## 📡 API Endpoints

| Endpoint                          | Method | Description                                                        |
|-----------------------------------|--------|--------------------------------------------------------------------|
| `/`                               | GET    | Welcome page                                                       |
| `/mojastrona`                     | GET    | Returns: "To jest moja strona!" (demo route)                       |
| `/hello`                          | GET    | Greets user, supports `?name=` parameter                           |
| `/api/v1.0/predict?num1=3&num2=4` | GET    | Returns prediction based on two input numbers e.g.(?num1=3&num2=4) |

---

## 🚀 Run locally (Python)

```bash
git clone https://github.com/hubert99x/rest-api-flask-project
cd rest-api-flask-project
```

### Create a virtual environment:

#### Linux/macOS:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

#### Windows (PowerShell or CMD):
```powershell
.venv\Scripts\activate
```

#### Windows (Git Bash):
```bash
python3 -m venv .venv
source .venv/Scripts/activate
```

### Install dependencies:
```bash
pip install -r requirements.txt
```

### Run the application:
```bash
python app.py
```

The app will be available at: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---
## 🐳 Running with Docker

### 🔧 Build the Docker image:

```bash
docker build --no-cache -t modelml .
```

### ▶️ Run the container:

```bash
docker run --name Flask_REST_API -p 127.0.0.1:5001:5000 modelml
```

Access the app locally at: http://127.0.0.1:5001

📌 If port `5001` is in use, you can change it (e.g. `-p 5002:5000`)

---

## 🔁 Updating `requirements.txt`

To refresh dependencies list:
```bash
pip freeze > requirements.txt
```

---

## ℹ️ Additional Info

The app contains a simple decision rule:  
It adds two numbers (`num1` and `num2`), and compares the result to a threshold (5.8).  
Returns `1` if the total is greater, otherwise `0`.

---

## 🐍 Requirements

- Python 3.10+ or Docker
- pip

---

# 🧪 Flask REST API – Model decyzyjny (Projekt edukacyjny)

Prosty projekt REST API napisany w Pythonie z użyciem frameworka **Flask**. Aplikacja udostępnia kilka endpointów oraz prostą regułę decyzyjną opartą na sumie dwóch liczb.

---

## 📁 Zawartość repozytorium

- `app.py` - Kod aplikacji Flask
- `requirements.txt` - Lista zależności
- `Dockerfile` - Plik konfiguracyjny do uruchomienia aplikacji w kontenerze Docker
- `Lab2.ipynb` - Interaktywny notatnik prezentujący użycie i testy REST API
- `README.md` - Instrukcja uruchomienia i opis projektu


---

## 📡 Endpointy API

| Endpoint                          | Metoda | Opis                                                           |
|-----------------------------------|--------|----------------------------------------------------------------|
| `/`                               | GET    | Strona powitalna                                               |
| `/mojastrona`                     | GET    | Zwraca tekst: "To jest moja strona!"                           |
| `/hello`                          | GET    | Wita użytkownika (?name=Imię)                                  |
| `/api/v1.0/predict?num1=3&num2=4` | GET    | Zwraca predykcję na podstawie dwóch liczb np. (?num1=3&num2=4) |

---

## 🚀 Uruchomienie lokalne (Python)

### 1️⃣ Sklonuj repozytorium:

```bash
git clone https://github.com/hubert99x/rest-api-flask-project
cd rest-api-flask-project
```

### 2️⃣ Utwórz środowisko wirtualne:

#### ✅ Dla Linux/macOS:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

#### ✅ Dla Windows:

##### PowerShell / CMD:
```powershell
.venv\Scripts\activate
```

##### Git Bash (na Windowsie):
```bash
python3 -m venv .venv
source .venv/Scripts/activate
```

---

### 📦 Zainstaluj zależności:

```bash
pip install -r requirements.txt
```

---

### ▶️ Uruchom aplikację:

```bash
python app.py
```

Aplikacja będzie dostępna pod adresem: http://127.0.0.1:5001

---

## 🐳 Uruchomienie w Dockerze

### 🔧 Zbuduj obraz Dockera:

```bash
docker build --no-cache -t modelml .
```

### ▶️ Uruchom kontener:

```bash
docker run --name Flask_REST_API -p 127.0.0.1:5001:5000 modelml
```

Aplikacja będzie dostępna pod adresem: [http://127.0.0.1:5001](http://127.0.0.1:5001)

📌 **Uwaga:** jeśli port `5001` jest zajęty na Twoim komputerze, możesz zmienić mapowanie np. na `-p 5002:5000`

---

## 🔁 Aktualizacja `requirements.txt`

Jeśli zainstalujesz nowe biblioteki lub zaktualizujesz istniejące, zaktualizuj plik `requirements.txt`, aby inni mogli poprawnie odtworzyć środowisko.

### 📌 Jak to zrobić:

```bash
pip freeze > requirements.txt
```

To polecenie nadpisze stary plik `requirements.txt` aktualną listą bibliotek z Twojego środowiska.

---

## ℹ️ Informacje dodatkowe

Projekt zawiera prostą regułę decyzyjną: suma dwóch liczb (`num1` i `num2`) jest porównywana do wartości progowej 5.8.  
Jeśli suma jest większa, zwracana jest decyzja `1`, w przeciwnym razie `0`.

---

## 📌 Wymagania

- Python 3.10+ lub Docker
- pip (Python package manager)
