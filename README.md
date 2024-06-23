# Correction et Analyse des Questions d'Examen de Text Mining

1. **Expressions régulières :** Quel est le résultat de l'expression régulière `r'(\b[A-Za-z]+)\1'` appliquée à la chaîne "Bonjour bonjour, c'est un beau jour" ?
   - **Réponse :** C) `[]`
   - **Analyse :** L'expression régulière `r'(\b[A-Za-z]+)\1'` recherche des mots consécutifs identiques. Dans la chaîne donnée, aucun mot n'est répété consécutivement.

2. **TF-IDF :** Dans une collection de documents, le terme "chat" apparaît 3 fois dans un document et 10 fois au total dans tous les documents. Si la collection contient 100 documents, quel est le TF-IDF du terme "chat" dans ce document ?
   - **Réponse :** D) 3 (Toutes les réponses A: 0.03, B: 0.09, C: 0.3, D: 0.9 sont possibles selon le nombre total de termes dans le document)
   - **Analyse :** 
     - **TF (Term Frequency) :** Si on suppose que le document a un nombre total de termes (N_d), alors \(\text{TF} = \frac{3}{N_d}\).
     - **IDF (Inverse Document Frequency) :** \(\text{IDF} = \log_{10}(10) = 1\).
     - **Calcul du TF-IDF :** Pour obtenir des valeurs comme 0.03, 0.09, 0.3, et 0.9, N_d doit être respectivement 100, 33, 10, et 3-4. Par défaut, avec N_d = 1, \(\text{TF-IDF} = 3\).

3. **N-grams :** Quels sont les bigrammes générés à partir de la phrase "Text mining est amusant" ?
   - **Réponse :** D) `['Text mining', 'mining est', 'est amusant']`
   - **Analyse :** Les bigrammes sont des séquences de deux mots consécutifs. Donc, à partir de "Text mining est amusant", nous obtenons "Text mining", "mining est", et "est amusant".

4. **Word2Vec :** Quelle est la principale différence entre les approches CBOW et Skip-gram de Word2Vec ?
   - **Réponse :** A) CBOW prédit le mot cible à partir des mots contextuels, tandis que Skip-gram prédit les mots contextuels à partir du mot cible.
   - **Analyse :** CBOW (Continuous Bag of Words) utilise les mots de contexte pour prédire un mot cible, tandis que Skip-gram utilise un mot cible pour prédire les mots de contexte.

5. **GloVe :** Quel est l'objectif principal de l'algorithme GloVe ?
   - **Réponse :** D) Combiner les avantages de la factorisation matricielle et des modèles de fenêtre contextuelle.
   - **Analyse :** GloVe (Global Vectors for Word Representation) utilise une matrice de co-occurrence globale pour capturer les statistiques globales des mots tout en capturant les relations contextuelles.

6. **Expressions régulières :** Quel est le rôle du lookaround positif `(?=...)` dans une expression régulière ?
   - **Réponse :** B) Vérifier la présence d'un motif à droite sans le consommer.
   - **Analyse :** Le lookaround positif `(?=...)` vérifie la présence d'un motif à droite de la position actuelle sans le consommer dans la correspondance finale.

7. **TF-IDF :** Pourquoi utilise-t-on l'inverse de la fréquence des documents (IDF) dans le calcul du TF-IDF ?
   - **Réponse :** A) Pour augmenter l'importance des termes rares et B) Pour réduire l'importance des termes fréquents.
   - **Analyse :** L'IDF augmente l'importance des termes rares en leur attribuant un poids plus élevé et réduit l'importance des termes fréquents en leur attribuant un poids plus faible.

8. **N-grams :** Quel est l'impact de l'augmentation de la taille des n-grams sur la modélisation du langage ?
   - **Réponse :** A) Augmentation de la précision mais réduction de la généralisation.
   - **Analyse :** Les n-grams plus grands capturent des séquences de mots plus longues, augmentant la précision pour des contextes spécifiques mais réduisant la capacité de généralisation du modèle.

9. **Word2Vec :** Quel est l'avantage principal de l'utilisation de embeddings de mots comme Word2Vec par rapport aux approches traditionnelles de représentation de mots ?
   - **Réponse :** B) Meilleure capture des relations sémantiques.
   - **Analyse :** Les embeddings de mots comme Word2Vec capturent efficacement les relations sémantiques et contextuelles entre les mots, contrairement aux représentations one-hot traditionnelles.

10. **GloVe :** Comment GloVe traite-t-il les mots rares dans le corpus ?
    - **Réponse :** D) En utilisant un mécanisme de lissage.
    - **Analyse :** GloVe utilise une fonction de pondération qui donne moins de poids aux co-occurrences rares, ce qui est une forme de lissage pour gérer les mots rares.

11. **Expressions régulières :** Quelle expression régulière correspond à une adresse e-mail valide ?
    - **Réponse :** A) `r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b'` et D) `r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9]+\.[A-Z|a-z]{2,}\b'`
    - **Analyse :** Ces expressions régulières permettent de correspondre à une adresse e-mail valide, comprenant des lettres, des chiffres et des caractères spéciaux autorisés, un symbole '@', un domaine et une extension de domaine de deux caractères ou plus.

12. **TF-IDF :** Quel est l'effet de l'utilisation de TF-IDF sur les mots communs comme "le", "la", "et" dans un corpus de texte ?
    - **Réponse :** B) Leur importance est diminuée.
    - **Analyse :** TF-IDF réduit l'importance des mots très fréquents dans le corpus car leur fréquence inverse des documents (IDF) est faible.

13. **N-grams :** Dans l'analyse des sentiments, pourquoi les bi-grams ou tri-grams peuvent être plus informatifs que les unigrams ?
    - **Réponse :** A) Ils capturent mieux les expressions idiomatiques.
    - **Analyse :** Les bi-grams et tri-grams peuvent capturer des phrases ou des expressions idiomatiques importantes pour l'analyse des sentiments, comme "pas bon" ou "très heureux".

14. **Word2Vec :** Quel est l'effet de l'augmentation de la taille de la fenêtre contextuelle dans le modèle Skip-gram de Word2Vec ?
    - **Réponse :** A) Augmentation de la précision des relations sémantiques et D) Réduction de la vitesse de convergence.
    - **Analyse :** Une fenêtre contextuelle plus large capture plus de contexte, augmentant la précision des relations sémantiques mais ralentissant la convergence en raison du traitement de plus de combinaisons de mots.

15. **GloVe :** Quelle est la principale différence entre GloVe et Word2Vec en termes de traitement des co-occurrences de mots ?
    - **Réponse :** A) GloVe utilise une matrice de co-occurrence globale, tandis que Word2Vec se concentre sur des contextes locaux et C) GloVe est basé sur la factorisation matricielle, tandis que Word2Vec est basé sur la prédiction de contexte.
    - **Analyse :** GloVe construit une matrice de co-occurrence globale et la factorise pour capturer les relations sémantiques, tandis que Word2Vec utilise des contextes locaux pour entraîner ses modèles de prédiction.

16. **Expressions régulières :** Comment modifieriez-vous l'expression régulière `r'\d{2,4}'` pour qu'elle corresponde uniquement aux nombres de 3 ou 4 chiffres ?
    - **Réponse :** A) `r'\d{3,4}'`
    - **Analyse :** L'expression `r'\d{3,4}'` correspond aux nombres composés de 3 ou 4 chiffres.

17. **TF-IDF :** Dans quel cas le TF-IDF d'un terme serait-il égal à zéro ?
    - **Réponse :** A) Si le terme apparaît dans tous les documents du corpus, B) Si le terme n'apparaît dans aucun document du corpus et D) Si le terme apparaît une fois dans chaque document.
    - **Analyse :** Le TF-IDF est zéro si le terme apparaît dans tous les documents (IDF=0), s'il n'apparaît dans aucun document (TF=0), ou s'il apparaît une fois dans chaque document (IDF=0).

18. **N-grams :** Quel est l'avantage principal de l'utilisation des n-grams dans le traitement du langage naturel ?
    - **Réponse :** C) Ils améliorent la compréhension du contexte et de la structure des phrases.
    - **Analyse :** Les n-grams capturent des séquences de mots qui aident à mieux comprendre le contexte et la structure des phrases.

19. **Word2Vec :** Quelle méthode est généralement utilisée pour réduire la dimensionnalité des vecteurs de mots dans Word2Vec ?
    - **Réponse :** A) Analyse en composantes principales (ACP)
    - **Analyse :** L'Analyse en composantes principales (ACP) est couramment utilisée pour réduire la dimensionnalité des vecteurs de mots tout en conservant le plus d'information possible.

20. **GloVe :** Dans l'algorithme GloVe, comment le poids des co-occurrences est-il généralement déterminé ?
    - **Réponse :** B) Par une fonction logarithmique de la fréquence des co-occurrences.
    - **Analyse :** GloVe utilise une fonction logarithmique pour pondérer les co-occurrences, ce qui permet de capturer efficacement les relations sémantiques entre les mots.
