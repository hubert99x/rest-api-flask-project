# 🧪 Flask REST API – Model decyzyjny (Projekt edukacyjny)

Projekt REST API napisany w Pythonie z użyciem frameworka **Flask**. Aplikacja udostępnia kilka endpointów oraz prostą regułę decyzyjną opartą na sumie dwóch liczb.

---

## 📁 Zawartość repozytorium

- `app.py` – kod aplikacji Flask
- `requirements.txt` – lista zależności Pythona
- `Dockerfile` – plik konfiguracyjny do uruchomienia aplikacji w kontenerze Docker
- `.gitignore` – ignorowanie `.venv` i innych niepotrzebnych plików

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

### 🔽 Sklonuj repozytorium:

```bash
git clone https://github.com/hubert99x/REST-API-project-140251
cd REST-API-project-140251
```

### 🧱 Utwórz środowisko wirtualne:

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

Aplikacja dostępna będzie pod adresem: [http://127.0.0.1:5000](http://127.0.0.1:5000)

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

📌 **Uwaga:** Jeśli port `5001` jest już zajęty, możesz go zmienić, np.:

```bash
docker run -p 5002:5000 modelml
```

Wtedy aplikacja będzie dostępna pod: [http://127.0.0.1:5002](http://127.0.0.1:5002)

---

## 🔁 Aktualizacja requirements.txt

Jeśli dodasz lub zaktualizujesz pakiety w swoim środowisku `.venv`, możesz zaktualizować `requirements.txt`, aby inni użytkownicy mogli odtworzyć dokładnie takie samo środowisko:

```bash
pip freeze > requirements.txt
```

To polecenie **nadpisze plik `requirements.txt`** aktualną listą zainstalowanych pakietów w środowisku.

---

## ℹ️ Informacje dodatkowe

Projekt zawiera prostą regułę decyzyjną: suma dwóch liczb jest porównywana z wartością progową 5.8. Jeśli suma jest większa, zwracana jest decyzja 1, w przeciwnym razie 0.

---

## 📌 Wymagania

- Python 3.10+ lub Docker
- pip (Python package manager)
