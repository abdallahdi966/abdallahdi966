def recherche_binaire(liste, item):
    bas = 0
    haut = len(liste) - 1

    while bas <= haut:
        milieu = (bas + haut) // 2
        guess = liste[milieu]
        if guess == item:
            return milieu
        if guess > item:
            haut = milieu - 1
        else:
            bas = milieu + 1
    return None

# Test de la fonction
ma_liste = [1, 3, 5, 7, 9]

print(recherche_binaire(ma_liste, 3))  # Renvoie 1
print(recherche_binaire(ma_liste, -1))  # Renvoie None
