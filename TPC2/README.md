print("Bem vindo ao jogo dos fósforos!")

n = 21
jogador = int(input("Pretende jogar em primeiro ou em segundo? Jogador 1 ou 2?"))
while n > 1:
    if jogador == 1:
        jogada = int(input("De 1 a 4, quantos fósforos queres retirar?"))
        if jogada >= 1 and jogada <= 4:
            n = n - jogada
            print("Restam" , n , "fósforos!")
            if jogada == 1:
                        n = n - 4
                        print("A jogada do computador é retirar 4 fósforos.")
                        print("Restam" , n , "fósforos!")
            if jogada==2:
                        n = n - 3
                        print("A jogada do computador é retirar 3 fósforos.")
                        print("Restam", n , "fósforos")
            if jogada==3:
                        n = n - 2
                        print("A jogada do computador é retirar 2 fósforos.")
                        print("Restam", n , "fósforos")
            if jogada==4:
                        n = n - 1
                        print("A jogada do computador é retirar 1 fósforos.")
                        print("Restam", n , "fósforos")
        else:
            print("Erro! Tenta de novo")
        print("Fim de jogo. Jogador perde! :(")
    elif jogador == 2:
            resto = n % 5 
            if resto == 0:
                    jogada_computador = 1
            else:
                jogada_computador = resto
            n -= jogada_computador
            print("O computador retira" , jogada_computador , "fósforos")
            print("Restam" , n , "fósforos")
            if n == 1:
                print("Fim de jogo. Jogador perde! :(")
                break
    jogada = int(input("De 1 a 4, quantos fósforos queres retirar?"))
    if jogada < 1 or jogada > 4:
           print("Erro! Tenta de novo!")
           continue
    n -= jogada
    print("Restam" , n , "fósforos")
    if n == 1:
          print("Fim do jogo! Ganhaste! :)")
          break
       )")
           break
