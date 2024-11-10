# ses---ces
<html lang="fr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercice - Ces vs Ses</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }

        .correct {
            color: green;
        }

        .incorrect {
            color: red;
        }

        .analyse {
            color: blue;
        }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["ces", "ses", "ces", "ses", "ces", "ses", "ces", "ses", "ces", "ses",
                                     "ces", "ses", "ces", "ses", "ces", "ses", "ces", "ses", "ces", "ses"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));
                let analyse = document.getElementById('analyse' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✔️ Correct";
                    feedback.className = "correct";
                    analyse.innerText = "";
                    score++;
                } else {
                    feedback.innerText = "❌ Incorrect";
                    feedback.className = "incorrect";
                    analyse.innerText = `La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "ces" est un déterminant démonstratif utilisé pour montrer quelque chose (ex : ces livres), tandis que "ses" est un déterminant possessif utilisé pour indiquer que quelque chose appartient à quelqu'un (ex : ses affaires).`;
                    analyse.className = "analyse";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>

<body>
    <h2>Règle : "ces" vs "ses"</h2>
    <p>
        - <b>"ces"</b> est un déterminant démonstratif utilisé pour montrer quelque chose au pluriel. Exemple : "Ces livres sont à moi".<br>
        - <b>"ses"</b> est un déterminant possessif utilisé pour indiquer la possession au pluriel. Exemple : "Ses amis sont venus le voir".
    </p>

    <h2>Exercice - Complétez avec "ces" ou "ses"</h2>

    <!-- Génération des 20 questions -->
    <div id="exercices">
        <p>1. ___ chiens sont très bruyants.</p>
        <input type="text" id="reponse1"> <span id="feedback1"></span><br>
        <p id="analyse1"></p><br>

        <p>2. Elle a perdu ___ clés.</p>
        <input type="text" id="reponse2"> <span id="feedback2"></span><br>
        <p id="analyse2"></p><br>

        <p>3. ___ arbres sont magnifiques en automne.</p>
        <input type="text" id="reponse3"> <span id="feedback3"></span><br>
        <p id="analyse3"></p><br>

        <p>4. Il a réparé ___ chaussures.</p>
        <input type="text" id="reponse4"> <span id="feedback4"></span><br>
        <p id="analyse4"></p><br>

        <p>5. ___ fleurs sont très colorées.</p>
        <input type="text" id="reponse5"> <span id="feedback5"></span><br>
        <p id="analyse5"></p><br>

        <p>6. Elle adore ___ vêtements.</p>
        <input type="text" id="reponse6"> <span id="feedback6"></span><br>
        <p id="analyse6"></p><br>

        <p>7. ___ enfants jouent dans le parc.</p>
        <input type="text" id="reponse7"> <span id="feedback7"></span><br>
        <p id="analyse7"></p><br>

        <p>8. Elle a vendu ___ livres à la brocante.</p>
        <input type="text" id="reponse8"> <span id="feedback8"></span><br>
        <p id="analyse8"></p><br>

        <p>9. ___ idées sont vraiment intéressantes.</p>
        <input type="text" id="reponse9"> <span id="feedback9"></span><br>
        <p id="analyse9"></p><br>

        <p>10. Il a lavé ___ assiettes.</p>
        <input type="text" id="reponse10"> <span id="feedback10"></span><br>
        <p id="analyse10"></p><br>

        <p>11. ___ oiseaux chantent le matin.</p>
        <input type="text" id="reponse11"> <span id="feedback11"></span><br>
        <p id="analyse11"></p><br>

        <p>12. Elle a rassemblé ___ affaires.</p>
        <input type="text" id="reponse12"> <span id="feedback12"></span><br>
        <p id="analyse12"></p><br>

        <p>13. ___ chaussures sont à la mode cette année.</p>
        <input type="text" id="reponse13"> <span id="feedback13"></span><br>
        <p id="analyse13"></p><br>

        <p>14. Il a perdu ___ jouets au parc.</p>
        <input type="text" id="reponse14"> <span id="feedback14"></span><br>
        <p id="analyse14"></p><br>

        <p>15. ___ amis sont venus dîner hier soir.</p>
        <input type="text" id="reponse15"> <span id="feedback15"></span><br>
        <p id="analyse15"></p><br>

        <p>16. Elle a oublié ___ devoirs à la maison.</p>
        <input type="text" id="reponse16"> <span id="feedback16"></span><br>
        <p id="analyse16"></p><br>

        <p>17. ___ problèmes doivent être résolus rapidement.</p>
        <input type="text" id="reponse17"> <span id="feedback17"></span><br>
        <p id="analyse17"></p><br>

        <p>18. Il a retrouvé ___ lunettes.</p>
        <input type="text" id="reponse18"> <span id="feedback18"></span><br>
        <p id="analyse18"></p><br>

        <p>19. ___ routes sont bloquées par la neige.</p>
        <input type="text" id="reponse19"> <span id="feedback19"></span><br>
        <p id="analyse19"></p><br>

        <p>20. Elle a lavé ___ vêtements ce matin.</p>
        <input type="text" id="reponse20"> <span id="feedback20"></span><br>
        <p id="analyse20"></p><br>
    </div>

    <button onclick="verifier()">Vérifier</button>
    <p id="score"></p>
</body>

</html>
