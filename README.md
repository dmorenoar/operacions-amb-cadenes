# Operacions amb Cadenes en Python

Aquest document conté exemples pràctics d'operacions amb cadenes de text (strings) en Python.

## Creació d'una Cadena
```python
message = "Hello"
print(message)
```

Una cadena és text que es defineix amb cometes simples o dobles. El tipus de dada és `str`.

## Operacions Bàsiques

### Concatenació (+)

Unir cadenes de text:
```python
user_name = "Dani"
age = 1987
text = "Hola " + user_name + ", vas néixer " + str(age)
print(text)

# Opció amb f-string
print(f"Hola {user_name}, vas néixer {age}")
```

**Observació:** Cal convertir els números a text amb `str()`.

### Repetició (*)

Repetir una cadena un nombre determinat de vegades:
```python
print("*" * 10)  # **********
print("A" * 3)   # AAA
```

### Longitud (len())

Saber quants caràcters té una cadena:
```python
manga = "One piece"
print(f"Longitud de la paraula: {len(manga)}")
```

**Observació:** Els espais compten.

### Accés als Caràcters

Accedir a caràcters concrets de la cadena de text:
```python
anime = "Kimetsu No Yaiba"
print(f"Primera posició: {anime[0]}")    # K
print(f"Posició 2: {anime[2]}")          # m
print(f"Última posició: {anime[-1]}")    # a
print(f"Antepenúltima: {anime[-2]}")     # b
```

**Observacions:**
- Les cadenes comencen amb l'índex 0
- Accés positiu (de 0 a len(paraula)) i negatiu (de len(paraula) a 0)

### Subcadenes (Slicing)

Extreure parts d'una cadena:
```python
film = "The lord of the rings"
print(f"Primeres 4 posicions: {film[0:4]}")  # The 
print(f"Paraula 'lord': {film[4:8]}")         # lord
print(f"A partir posició 12: {film[12:]}")    # the rings
```

## Mètodes Essencials

### Canvi de Format
```python
phrase = " buFaR i fer AmpoLles "

phrase.upper()       # Tot majúscules
phrase.lower()       # Tot minúscules
phrase.capitalize()  # Primer caràcter en majúscula
phrase.title()       # Primer caràcter de cada paraula en majúscula
```

### Eliminació i Substitució
```python
phrase.strip()                    # Elimina espais al principi i final
phrase.replace("fer", "hacer")    # Reemplaça text
phrase.replace("A", "9")          # Reemplaça caràcters
```

### Cerca i Recompte
```python
frase = "Caga tió, tió de Nadal"

# find() - Retorna la posició (o -1 si no la troba)
frase.find("tió")    # 5
frase.find("Nadal")  # 18
frase.find("Marta")  # -1

# count() - Retorna quantes vegades apareix
frase.count("tió")   # 2
frase.count("a")     # 5

# Operador in - Retorna True o False
if "tió" in frase:
    print("La paraula tió està al text")
```

## Validació de Cadenes
```python
user = "dmoren10"
password = "12345"
secret_message = "El gos s'ha menjat els meus deures"

user.isalpha()              # Només lletres? False
password.isdigit()          # Només números? True
user.isalnum()              # Números i lletres? True
" " in secret_message       # Hi ha espais? True
```

## Comparació de Cadenes
```python
if password == "12345":
    print("Has endevinat el password")
else:
    print("Password incorrecte")
```

**Observació:** Python distingeix entre minúscules i majúscules.

## Recorregut de Cadenes

### Recórrer caràcter per caràcter
```python
text = "La ment que s'obre a una nova idea, mai torna a la seva mida original."

# Mostrar sense salt de línia
for lletra in text:
    print(lletra, end="")

# Comptar ocurrències
countA = 0
for character in text:
    if character == "a":
        countA += 1
print(f"He trobat {countA} a en el text")
```

### Recórrer per índex (accés positiu)
```python
for i in range(len(text)):
    print(text[i], end="")
```

### Recórrer per índex (accés negatiu)
```python
# Mostrar la cadena al revés
for i in range(1, len(text) + 1):
    print(text[-i], end="")
```

**Explicació:** 
- `len(text) + 1`: Afegim 1 perquè `range` no inclou l'últim valor
- A cada iteració, `-i` accedeix des del final cap al principi

---
