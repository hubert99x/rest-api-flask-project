---
⚠️ **Polska wersja poniżej ⬇️**  
Polish version below – scroll down to read in Polish.
---

# 🧪 Flask REST API – Decision Model (Educational Project)

This is a simple REST API project written in Python using the **Flask** framework.  
The application exposes a few endpoints and a basic decision logic based on the sum of two numbers.

---

## 📁 Repository Contents

- `app.py` – Flask application source code  
- `requirements.txt` – list of required Python packages  
- `Dockerfile` – Docker container configuration  

---

## 📡 API Endpoints

| Endpoint            | Method | Description                                                |
|---------------------|--------|------------------------------------------------------------|
| `/`                 | GET    | Welcome page                                               |
| `/mojastrona`       | GET    | Returns: "This is my page!" (demo route)                   |
| `/hello`            | GET    | Greets user, supports `?name=` parameter                   |
| `/api/v1.0/predict` | GET    | Returns prediction based on two input numbers (?num1=&num2=) |

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

## 🐳 Run with Docker

```bash
docker build -t modelml .
docker run -p 5001:5000 modelml
```

Access the app at: [http://127.0.0.1:5001](http://127.0.0.1:5001)

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

- `app.py` – kod aplikacji Flask
- `requirements.txt` – lista zależności Pythona
- `Dockerfile` – plik konfiguracyjny do uruchomienia aplikacji w kontenerze Docker

---

## 📡 Endpointy API

| Endpoint            | Metoda | Opis                                  |
|---------------------|--------|----------------------------------------|
| `/`                 | GET    | Strona powitalna                      |
| `/mojastrona`       | GET    | Zwraca tekst: "To jest moja strona!" |
| `/hello`            | GET    | Wita użytkownika (?name=Imię)         |
| `/api/v1.0/predict` | GET    | Zwraca predykcję na podstawie dwóch liczb (?num1=&num2=) |

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

Aplikacja będzie dostępna pod adresem: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## 🐳 Uruchomienie w Dockerze

### 🔧 Zbuduj obraz Dockera:

```bash
docker build -t modelml .
```

### ▶️ Uruchom kontener:

```bash
docker run -p 5001:5000 modelml
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
