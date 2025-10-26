def criarTurma():
    turma=[]
    return turma

def inserirAluno(listat):
    a=input("Digite o nome do aluno:")
    i=int(input("Digite o id do aluno:"))
    n1=int(input("Digite a nota dos TPCs:"))
    n2=int(input("Digite a nota do Projeto:"))
    n3=int(input("Digite a nota do Teste:"))
    notas=[n1,n2,n3]
    al=(a,i,notas)
    listat.append(al)
    print(listat)
    return listat

def listarTurma(listat):
    print(f"Lista de alunos na turma {listat}:")
    for t in listat:
        print(f"O aluno {t[0]}, com o id {t[1]}, teve a nota {t[2][0]} no TPC, {t[2][1]} no projeto e {t[2][2]} no teste.")
    return

def idAluno(listat,i):
    for t in listat:
        if i == t[1]:
            print(f"O aluno cujo id é {i} é o/a {t}.")
        else:
            print("Aluno não encoontrado.")
    return


def guardarTurma(listat, fnome):
    file = open(fnome,"w") # "r", "w"
    res=""
    for a in listat:
        al, i, notas = a
        res += str(al) + ";" + str(i) + ";" + str(notas[0]) + "::" + str (notas[1]) + "::" + str(notas[2]) + "|"
        res+="\n"
    file.write(res)
    file.close()

def recuperarTurma(fnome):
    listat = []
    file = open(fnome,"r")
    text=file.read()
    turma_text=text.split("\n")

    for p_text in turma_text[:-1]:
        t=[]
        t_text=p_text.split("|")

        for t_text in t_text[:-1]:
            al, i, notas = t_text.split(";")

            notas_lista=[]
            for n in notas.split("::"):
                notas_lista.append(float(n))
            alu=(str(al),int(i),list(notas_lista))
            t.append(alu)
        listat.append(t)
    file.close()
    return listat


def menu():
    print("\n========= MENU =========")
    print("1: Criar uma turma")
    print("2: Inserir um aluno na turma")
    print("3: Listar a turma")
    print("4: Consultar um aluno por ID")
    print("5: Guardar a turma em ficheiro")
    print("6: Carregar a turma dum ficheiro")
    print("0: Sair")
    print("========================")

modo=-1
menu()
while modo!=0:
    modo=int(input("O que deseja efetuar?"))
    if modo==0:
        print("Terminou")
    elif modo==1:
        turma=criarTurma()
    elif modo==2:
        inserirAluno(turma)
    elif modo==3:
        listarTurma(turma)
    elif modo==4:
        ident=int(input("Qual id deseja procurar:"))
        idAluno(turma,ident)
    elif modo==5:
        print(f"A sua turma foi guardada no ficheiro: turma")
        guardarTurma(turma,"turma.txt")
    elif modo==6:
        print(recuperarTurma("turma.txt"))
    else:
        print("Tente outro número")
