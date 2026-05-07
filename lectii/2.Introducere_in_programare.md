# Introducere în programare

## 1. Structura Software (.ino)
Orice program Arduino este compus din două funcții obligatorii:

```cpp
void setup() {
  // Executat o singură dată la pornire
  // Aici se configurează pinii (INPUT/OUTPUT)
}

void loop() {
  // Executat în buclă infinită
  // Aici se scrie logica robotului
}
```

## 2. Configurare Pini (pinMode)
În funcția `setup()`, definim rolul pinilor folosind instrucțiunea `pinMode(pin, mod)`:

* **OUTPUT**: Pinul trimite curent (aprinde un LED, pornește un motor).
* **INPUT**: Pinul primește date (de la un buton sau senzor digital).
* **INPUT_PULLUP**: Folosit pentru butoane (activează rezistența internă a plăcii).

```cpp
void setup() {
  pinMode(13, OUTPUT); // LED-ul integrat de pe placă
  pinMode(2, INPUT);   // Pin setat pentru citire senzor
}
```

## 3. Comenzi Digitale și Analogice
Pentru a interacționa cu componentele, folosim următoarele funcții de bază:

* `digitalWrite(pin, stare)` : Trimite semnal **HIGH** (5V) sau **LOW** (0V).
* `digitalRead(pin)` : Citește starea digitală (0 sau 1) a unui senzor.
* `analogRead(pin)` : Citește valori între **0 și 1023** (pentru senzori analogici precum cel de lumină sau distanță).
* `analogWrite(pin, valoare)` : Control PWM (**0-255**) pentru a regla viteza motoarelor sau luminozitatea unui LED.

```cpp
void loop() {
  digitalWrite(13, HIGH); // Aprinde LED-ul
  int valoareSenzor = analogRead(A0); // Citește senzorul de pe pinul A0
}
```

## 4. Workflow Hardware în GitHub
Pentru succesul echipei, respectați fluxul de documentare în repository:

1. **Schema Electrică**: Înainte de alimentare, urcați în folderul `/hardware/` o poză cu schema sau montajul fizic.
2. **Tabel de Pini**: Specificați în `README.md` alocarea fiecărui pin pentru a evita conflictele între cod și fire.
3. **Serial Debug**: Folosiți `Serial.begin(9600);` în setup pentru a monitoriza datele trimise de senzori în Serial Monitor.

```cpp
void setup() {
  Serial.begin(9600); // Pornire comunicare serială
}

void loop() {
  Serial.println(analogRead(A0)); // Trimite datele către PC pentru verificare
}
```

## 5. Reguli
- **Verifică de două ori**: Nu alimenta circuitul până nu verifici conexiunile conform schemei din `/hardware`.
- **Comentează Codul**: Explică ce face fiecare funcție importantă pentru ca restul echipei să înțeleagă logica.
- **Commit după succes**: Ai reușit să citești senzorul? Fă un commit. Ai reușit să miști motorul? Alt commit.
