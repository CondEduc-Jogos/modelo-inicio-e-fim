#Sistema de pontos
init python:
 pontos = 0

# O script do jogo fica nesse arquivo

label start:

    ChP "Olá, sejam bem-vindos ao nosso exercício prático em formato de história interativa."
    ChP "Aqui veremos exemplos reais de coisas que podem acontecer na vida profissional de um porteiro."
    ChP "Seu papel será tomar as decisões certas de acordo com cada situação apresentada,"
    ChP "desse modo, poderemos entender como o porteiro influencia no funcionamento de um condomínio."
    ChP "Esse jogo fala sobre." # colocar o tema de vocês
    ChP "Está preparado?"

    menu:
     "Sim":
      #show screen noframe_pontos
      ChP "Que da hora!{p}Consegue ver essa barra de pontos ali em cima da tela?"
      ChP "Cada resposta certa faz a barra aumentar."
      ChP "Você só vai ganhar o jogo quando conseguir a pontuação máxima."
      ChP "Mas sem pressão.{p}Eu vou estar aqui o tempo todo para te ajudar."
      ChP "Hora de pôr a mão na massa."
      #hide screen noframe_pontos
      #jump cena_00 # Esse comando pula para outra label
      return

     "Não":
      ChP "Não se preocupe, reveja o material se precisar."
      ChP "Respire fundo e vamos um passo de cada vez."
      ChP "Lembre-se, você sempre poderá recomeçar quando quiser."

      #show screen noframe_pontos

      ChP "Falando nisso...{p}Consegue ver essa barra de pontos ali em cima da tela?"
      ChP "Cada resposta certa faz a barra aumentar."
      ChP "Você só vai ganhar o jogo quando conseguir a pontuação máxima."
      ChP "Mas sem pressão.{p}Eu vou estar aqui o tempo todo para te ajudar."
      ChP "Hora de pôr a mão na massa."
      menu:
       "Sim!":
        #hide screen noframe_pontos
        #jump cena_00
        return

#colocar as labels aqui

label cena_final:

 "E aí? O que achou dessa aventura?"
 "Essa é uma forma que a CondEduc pensou para ajudar você, futuro porteiro de qualidade, a se divertir enquanto aprende."
 "Viu só quanta coisa aprendemos nos divertindo?"
 "Agora que você já está fera na parte de prevenção de combate e incêndio," #modificar de acordo com o tema do jogo
 "vamos seguir em frente com os próximos assuntos."
 "Te vejo em breve."

 return #esse comando termina o jogo
