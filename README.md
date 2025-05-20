<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tarxetas de Bioloxía: As Plantas</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts: Montserrat -->
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <!-- React y ReactDOM -->
  <script src="https://unpkg.com/react@18.2.0/umd/react.production.min.js"></script>
  <script src="https://unpkg.com/react-dom@18.2.0/umd/react-dom.production.min.js"></script>
  <!-- Babel para transformar JSX -->
  <script src="https://unpkg.com/@babel/standalone@7.24.7/babel.min.js"></script>
  <style>
    body { 
      font-family: 'Montserrat', sans-serif; 
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .animate-fadeIn {
      animation: fadeIn 0.3s ease-in-out;
    }
  </style>
</head>
<body class="bg-black text-white">
  <div id="root"></div>
  <script type="text/babel">
    try {
      const mainFlashcards = [
        {
          question: "Cal é a función principal das raíces nunha planta?",
          options: ["Realizar a fotosíntese", "Absorber auga e nutrientes", "Producir flores", "Soster as follas"],
          correct: 1
        },
        {
          question: "Que parte da planta realiza a fotosíntese?",
          options: ["Raíz", "Talo", "Folla", "Flor"],
          correct: 2
        },
        {
          question: "Como se chama o proceso polo que as plantas producen o seu propio alimento?",
          options: ["Respiración", "Fotosíntese", "Transpiración", "Xerminación"],
          correct: 1
        },
        {
          question: "Que precisan as plantas para realizar a fotosíntese?",
          options: ["Osíxeno e glicosa", "Luz solar, auga e dióxido de carbono", "Só auga", "Só luz solar"],
          correct: 1
        },
        {
          question: "Que tipo de planta non ten flores nin sementes?",
          options: ["Árbores", "Fentos", "Roseiras", "Cactus"],
          correct: 1
        },
        {
          question: "Que parte da flor contén os óvulos?",
          options: ["Pétalos", "Sépalos", "Pistilo", "Estames"],
          correct: 2
        },
        {
          question: "Como se chama a reprodución que implica pole e óvulos?",
          options: ["Asexual", "Sexual", "Por esporas", "Por estacas"],
          correct: 1
        },
        {
          question: "Que tipo de planta ten sementes protexidas dentro de froitos?",
          options: ["Ximnospermas", "Anxiospermas", "Fentos", "Musgos"],
          correct: 1
        },
        {
          question: "Cal é a función do talo?",
          options: ["Absorber auga", "Soster a planta e transportar nutrientes", "Producir sementes", "Realizar a fotosíntese"],
          correct: 1
        },
        {
          question: "Que son os estames nunha flor?",
          options: ["Partes femininas", "Partes masculinas", "Follas modificadas", "Raíces aéreas"],
          correct: 1
        },
        {
          question: "Que tipo de planta é un piñeiro?",
          options: ["Anxiosperma", "Ximnosperma", "Fento", "Musgo"],
          correct: 1
        },
        {
          question: "Que precisan as sementes para xerminar?",
          options: ["Só luz", "Auga, osíxeno e temperatura adecuada", "Só osíxeno", "Só terra"],
          correct: 1
        },
        {
          question: "Que son os musgos?",
          options: ["Plantas con flores", "Plantas sen raíces verdadeiras", "Árbores grandes", "Plantas acuáticas"],
          correct: 1
        },
        {
          question: "Que gas liberan as plantas durante a fotosíntese?",
          options: ["Dióxido de carbono", "Osíxeno", "Nitróxeno", "Hidróxeno"],
          correct: 1
        },
        {
          question: "Que parte da planta protexe a flor antes de que se abra?",
          options: ["Pétalos", "Sépalos", "Pistilo", "Estames"],
          correct: 1
        },
        {
          question: "Que é a clorofila?",
          options: ["Un tipo de raíz", "Un pigmento verde", "Unha semente", "Un tipo de flor"],
          correct: 1
        },
        {
          question: "Que tipo de reprodución NON require polinización?",
          options: ["Sexual", "Asexual", "Por esporas", "Por sementes"],
          correct: 1
        },
        {
          question: "Que son as anxiospermas?",
          options: ["Plantas sen sementes", "Plantas con flores e froitos", "Plantas con esporas", "Plantas sen raíces"],
          correct: 1
        },
        {
          question: "Cal é a función dos pétalos nunha flor?",
          options: ["Protexer a flor", "Atraer insectos", "Producir pole", "Absorber auga"],
          correct: 1
        },
        {
          question: "Que tipo de planta é un fento?",
          options: ["Anxiosperma", "Ximnosperma", "Planta sen sementes", "Planta con flores"],
          correct: 2
        },
        {
          question: "Que transporta o talo desde as raíces ás follas?",
          options: ["Só osíxeno", "Auga e nutrientes", "Só glicosa", "Dióxido de carbono"],
          correct: 1
        },
        {
          question: "Como se chama o proceso polo que as plantas perden auga?",
          options: ["Fotosíntese", "Transpiración", "Respiración", "Polinización"],
          correct: 1
        },
        {
          question: "Que son as ximnospermas?",
          options: ["Plantas con flores", "Plantas con sementes espidas", "Plantas sen raíces", "Plantas acuáticas"],
          correct: 1
        },
        {
          question: "Que parte da planta contén clorofila?",
          options: ["Raíz", "Folla", "Talo", "Flor"],
          correct: 1
        },
        {
          question: "Que precisan as plantas para crecer sans?",
          options: ["Só auga", "Luz, auga, nutrientes e aire", "Só luz", "Só terra"],
          correct: 1
        },
        {
          question: "Que é a polinización?",
          options: ["Produción de follas", "Transferencia de pole", "Absorción de auga", "Crecemento de raíces"],
          correct: 1
        },
        {
          question: "Que tipo de planta é unha roseira?",
          options: ["Ximnosperma", "Anxiosperma", "Fento", "Musgo"],
          correct: 1
        },
        {
          question: "Que producen as plantas durante a fotosíntese?",
          options: ["Dióxido de carbono", "Glicosa e osíxeno", "Só glicosa", "Só osíxeno"],
          correct: 1
        },
        {
          question: "Que son as esporas?",
          options: ["Sementes grandes", "Células reprodutivas dalgunhas plantas", "Follas pequenas", "Raíces aéreas"],
          correct: 1
        },
        {
          question: "Que parte da planta crece baixo terra?",
          options: ["Talo", "Folla", "Raíz", "Flor"],
          correct: 2
        }
      ];

      const secretFlashcards = [
        {
          question: "Que estrutura da planta axuda a fixala ao chan?",
          options: ["Follas", "Raíces", "Flores", "Talo"],
          correct: 1
        },
        {
          question: "Que parte da folla contén os estomas?",
          options: ["Epiderme", "Cloroplastos", "Vainas", "Pétalos"],
          correct: 0
        },
        {
          question: "Que é a savia nas plantas?",
          options: ["Un tipo de flor", "Líquido que transporta nutrientes", "Unha semente", "Un pigmento"],
          correct: 1
        },
        {
          question: "Que tipo de planta ten conos en lugar de froitos?",
          options: ["Anxiospermas", "Ximnospermas", "Fentos", "Musgos"],
          correct: 1
        },
        {
          question: "Que axudan a facer os insectos na polinización?",
          options: ["Producir sementes", "Transportar pole", "Absorber auga", "Realizar fotosíntese"],
          correct: 1
        },
        {
          question: "Que parte da semente se converte na nova planta?",
          options: ["Cotiledóns", "Embrión", "Testa", "Endosperma"],
          correct: 1
        },
        {
          question: "Como se chama a reprodución por estacas ou tubérculos?",
          options: ["Sexual", "Asexual", "Por esporas", "Por polinización"],
          correct: 1
        },
        {
          question: "Que tipo de planta é un carballo?",
          options: ["Fento", "Musgo", "Anxiosperma", "Ximnosperma"],
          correct: 2
        },
        {
          question: "Que función teñen os estomas nas follas?",
          options: ["Absorber luz", "Intercambio de gases", "Producir sementes", "Transportar auga"],
          correct: 1
        },
        {
          question: "Que é o xilema nas plantas?",
          options: ["Un pigmento", "Un tecido que transporta auga", "Unha flor", "Unha semente"],
          correct: 1
        },
        {
          question: "Que tipo de planta necesita moita humidade para vivir?",
          options: ["Cactus", "Fentos", "Piñeiros", "Roseiras"],
          correct: 1
        },
        {
          question: "Que produce o pistilo nunha flor?",
          options: ["Pole", "Óvulos", "Sementes", "Pétalos"],
          correct: 1
        },
        {
          question: "Que é a transpiración nas plantas?",
          options: ["Produción de froitos", "Perda de auga por evaporación", "Absorción de luz", "Crecemento de raíces"],
          correct: 1
        },
        {
          question: "Que tipo de planta é un tomateiro?",
          options: ["Ximnosperma", "Fento", "Anxiosperma", "Musgo"],
          correct: 2
        },
        {
          question: "Que axuda a planta a captar a luz solar?",
          options: ["Raíces", "Follas", "Sépalos", "Estames"],
          correct: 1
        },
        {
          question: "Que son os cloroplastos?",
          options: ["Células que almacenan auga", "Estruturas con clorofila", "Raíces pequenas", "Flores modificadas"],
          correct: 1
        },
        {
          question: "Que tipo de reprodución usan os fentos?",
          options: ["Sementes", "Esporas", "Flores", "Estacas"],
          correct: 1
        },
        {
          question: "Que transporta o floema nas plantas?",
          options: ["Auga", "Osíxeno", "Nutrientes elaborados", "Dióxido de carbono"],
          correct: 2
        },
        {
          question: "Que tipo de planta é un musgo?",
          options: ["Planta con froitos", "Planta sen vasos condutores", "Planta con flores", "Planta con sementes"],
          correct: 1
        },
        {
          question: "Que axuda a dispersar as sementes das anxiospermas?",
          options: ["Raíces", "Follas", "Froitos", "Estomas"],
          correct: 2
        }
      ];

      const FlashcardApp = () => {
        const [currentCard, setCurrentCard] = React.useState(0);
        const [score, setScore] = React.useState(0);
        const [selectedOption, setSelectedOption] = React.useState(null);
        const [isCorrect, setIsCorrect] = React.useState(null);
        const [quizFinished, setQuizFinished] = React.useState(false);
        const [isSecretMode, setIsSecretMode] = React.useState(false);

        const currentFlashcards = isSecretMode ? secretFlashcards : mainFlashcards;

        const handleAnswer = (index) => {
          setSelectedOption(index);
          if (index === currentFlashcards[currentCard].correct) {
            setIsCorrect(true);
            setScore(score + 1);
          } else {
            setIsCorrect(false);
          }
        };

        const nextCard = () => {
          if (currentCard + 1 < currentFlashcards.length) {
            setCurrentCard(currentCard + 1);
            setSelectedOption(null);
            setIsCorrect(null);
          } else {
            setQuizFinished(true);
          }
        };

        const calculateGrade = () => {
          const percentage = (score / currentFlashcards.length) * 10;
          return percentage.toFixed(1);
        };

        const restartQuiz = () => {
          setCurrentCard(0);
          setScore(0);
          setSelectedOption(null);
          setIsCorrect(null);
          setQuizFinished(false);
          setIsSecretMode(false);
        };

        const goToSecretMode = () => {
          setCurrentCard(0);
          setScore(0);
          setSelectedOption(null);
          setIsCorrect(null);
          setQuizFinished(false);
          setIsSecretMode(true);
        };

        return (
          <div className="flex flex-col items-center justify-center min-h-screen bg-black p-4">
            {!quizFinished ? (
              <div className="bg-gray-900 p-6 rounded-lg shadow-lg w-full max-w-md animate-fadeIn">
                <h1 className="text-2xl font-bold text-green-500 mb-4">
                  {isSecretMode ? 'Tarxetas Secretas: As Plantas' : 'Tarxetas: As Plantas'}
                </h1>
                <p className="text-lg text-white mb-4">Pregunta {currentCard + 1} de {currentFlashcards.length}</p>
                <p className="text-xl text-white mb-6">{currentFlashcards[currentCard].question}</p>
                <div className="space-y-4">
                  {currentFlashcards[currentCard].options.map((option, index) => (
                    <button
                      key={index}
                      className={`w-full p-3 rounded-lg text-left transition-all duration-200 ease-in-out ${
                        selectedOption === index
                          ? isCorrect
                            ? 'bg-green-500 text-white'
                            : 'bg-red-500 text-white'
                          : 'bg-gray-700 text-white hover:brightness-110 hover:-translate-y-1'
                      }`}
                      onClick={() => handleAnswer(index)}
                      disabled={selectedOption !== null}
                    >
                      {option}
                    </button>
                  ))}
                </div>
                {selectedOption !== null && (
                  <div className="mt-4 animate-fadeIn">
                    <p className={isCorrect ? 'text-green-500' : 'text-red-500'}>
                      {isCorrect ? 'Correcto!' : 'Incorrecto. A resposta correcta é: ' + currentFlashcards[currentCard].options[currentFlashcards[currentCard].correct]}
                    </p>
                    <button
                      className="mt-4 bg-green-500 text-white p-3 rounded-lg hover:brightness-110 hover:-translate-y-1 transition-all duration-200 ease-in-out"
                      onClick={nextCard}
                    >
                      Seguinte
                    </button>
                  </div>
                )}
              </div>
            ) : (
              <div className="bg-gray-900 p-6 rounded-lg shadow-lg w-full max-w-md text-center animate-fadeIn">
                <h1 className="text-2xl font-bold text-green-500 mb-4">
                  {isSecretMode && calculateGrade() >= 9.0 ? 'Gañaches o xogo!' : 'Cuestionario Completado!'}
                </h1>
                {!isSecretMode && calculateGrade() >= 9.0 && (
                  <h2 className="text-4xl font-bold text-green-500 mb-4">Eres un crack!</h2>
                )}
                <p className="text-lg text-white mb-4">
                  Acertaches {score} de {currentFlashcards.length} preguntas.
                </p>
                <p className="text-xl font-bold text-green-500 mb-6">Nota: {calculateGrade()}/10</p>
                {isSecretMode && calculateGrade() >= 9.0 ? (
                  <button
                    className="bg-green-500 text-white p-3 rounded-lg hover:brightness-110 hover:-translate-y-1 transition-all duration-200 ease-in-out"
                    onClick={restartQuiz}
                  >
                    Reiniciar
                  </button>
                ) : !isSecretMode && calculateGrade() >= 9.0 ? (
                  <button
                    className="bg-green-500 text-white p-3 rounded-lg hover:brightness-110 hover:-translate-y-1 transition-all duration-200 ease-in-out"
                    onClick={goToSecretMode}
                  >
                    Estudar máis
                  </button>
                ) : (
                  <button
                    className="bg-green-500 text-white p-3 rounded-lg hover:brightness-110 hover:-translate-y-1 transition-all duration-200 ease-in-out"
                    onClick={restartQuiz}
                  >
                    Volver comezar
                  </button>
                )}
              </div>
            )}
          </div>
        );
      };

      const root = ReactDOM.createRoot(document.getElementById('root'));
      root.render(<FlashcardApp />);
    } catch (error) {
      console.error('Erro na execución do script:', error);
    }
  </script>
</body>
</html># plantas
