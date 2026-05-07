# Introducere în Gihub

## 1. Get Started (Configurare Cont)
* **Creare cont:** Accesați [github.com](https://github.com) și creați un cont folosind adresa de email.
* **Profil:** Settings -> Public Profile -> Name -> Introduceți numele complet.
* **Organizație:** Acceptați invitația primită pe email sau accesați pagina organizației ROBOHaret pentru a deveni membri.

## 2. Configurare Repository Echipă
* **Creare:** Un membru al echipei apasă butonul "New" în interiorul organizației.
* **Setări obligatorii:**
    * Owner: `ROBOHaret`
    * Repository name: `[nume-proiect]-[nume-echipa]`
    * Visibility: `Public` 
    * Bifați: `Add a README file`.
* **Invitații:** Settings -> Collaborators -> Add people -> Căutați username-ul colegilor de echipă.

## 3. Structură Proiect
Toate proiectele trebuie să aibă următoarea structură:
* `/software/` : Codul sursă (.ino, .cpp).
* `/hardware/` : Scheme electrice și poze cu montajul.
* `/design-3d/` : Fișiere de imprimare 3D (.stl, .step).
* `README.md` : Documentația principală a proiectului (se află în rădăcina/root-ul proiectului).

## 4. Markdown Tutorial
Folosiți aceste sintaxe pentru a edita fișierul `README.md`:

```
# Titlu Mare (H1)
## Subtitlu (H2)
### Secțiune (H3)


**Text Bold** sau *Text Italic*

* Listă cu puncte
1. Listă numerotată

[Link către site școală](https://cni-sv.ro)
![Nume Imagine](cale/catre/imagine.jpg)

> Citat sau notă importantă

`Cod pe un singur rând`
```
```cpp
// Bloc de cod C++
void setup() { }
```

## 5. Reguli

- **Fiecare cu folderul lui**: Membrul de la software nu modifică folderul de 3D fără acordul colegului.
- **Mesaje Commit**: Scurte și clare (Ex: "Adăugat schemă baterie", "Update cod motoare").
- **Documentare constantă**: Orice progres hardware trebuie fotografiat și urcat în folderul `/hardware`.

### Competențele de GitHub pe care le dobândiți acum reprezintă standardul real în industria de engineering și vor fi piesa de rezistență din portofoliul vostru pentru facultate sau viitoarea carieră.
