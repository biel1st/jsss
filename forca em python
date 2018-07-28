import random
print("Jogo da forca de cidades")
steps = ['Cabeça','Pescoco','bracos','pernas']
palavras = 'canada parana goias gama brasilia newyork filadelfia luziania westbrook'.split()
def main():
    print('='*50)
    print("Instrucoes:")
    instrucoes()
    print('='*50)
    geraword()
    jogo()

    while True:
        again = int(input("Deseja jogar novamente? ? (1)Sim (2)Não"))
        if again==1:
            print("Jogo da forca de cidades")
            geraword()
            jogo()
        if again==2:
            break

def geraword():
    global palavras , sort , caralho , copia
    sort = random.choice(palavras)
    caralho = [str(d) for d in str(sort)]
    copia = [str(d) for d in str(sort)]

def jogo():
    global caralho , copia
    forgame = []
    parajogo=[]
    wrong =[]
    contacerto = 0
    conterro=0

    for y in range(len(sort)):
        parajogo.append('--')

    while parajogo!=copia:
        for c in parajogo:
            print(c, end=' ')
        print('letras erradas:',end='')
        for word in forgame:
            print(word,end=' ')
        print('')
        palavra = str(input("digite uma letra"))

        if palavra in caralho:
            contacerto+=1
            medir = caralho.count(palavra)
            for i in range(medir):
                parajogo[caralho.index(palavra)] = palavra
                caralho[caralho.index(palavra)] = ''
        win = ("Você ganhou!")

        if palavra not in sort:
            forgame.append(palavra)
            print(steps[conterro])
            conterro+=1

            if conterro ==4:
                win = ("Você perdeu , mais de 4 erros!")
                break
    print(win)
    print("A palavra era:")
    for run in copia:
        print(run , end='')
    print('')


def instrucoes():
    print("Você terá 4 chances para acertar o nome da cidades")
    print('Exemplo "Gama"')
    print("Molelo: -- -- -- --")
    print("Resposta: Gama")
    print("Chute a letra e veja se você acertou")
    print("As letras erradas estão do lado do jogo")
    print("Boa sorte :)")

main()
print("Muito Obrigado :)")




