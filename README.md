# pedra-papel-tesoura-lagarto-spock;
Jogo feito no PyCharm usando referências da série Big Bang Theory;
Fiz esse jogo quando estava iniciando meus estudos de Python (provavelmente há uma forma mais simples de faze-lo), porém é só um desafio que eu me propus a fazer;
O código que escrevi está logo abaixo.

        import random
        from tkinter import *

        #Randomiza as escolhas da máquina
        lista = 'Pedra Papel Tesoura Lagarto Spock'
        listas = lista.split()
        r = random.choice(listas)

        #janela
        janela = Tk()
        janela.title('Pedra-Papel-Tesoura-Lagarto-Spock')
        janela.geometry('850x425+350+150')
        janela.iconbitmap(default='icon.ico')
        janela.wm_resizable(width=False, height=False)
        back = PhotoImage(file='backgame.png')
        lbbackground = Label(janela, image=back)
        lbbackground.place(x=0, y=0)

        #imagens
        shit = PhotoImage(file='empate.png')
        lp = PhotoImage(file='Lagarto come o papel.png')
        ls = PhotoImage(file='Lagarto envenena o spock.png')
        pp = PhotoImage(file='Papel cobre a pedra.png')
        ps = PhotoImage(file='Papel refuta spock.png')
        pl = PhotoImage(file='Pedra esmaga o lagarto.png')
        pt = PhotoImage(file='Pedra quebra tesoura.png')
        st = PhotoImage(file='Spock esmaga a tesoura.png')
        sp = PhotoImage(file='Spock vaporiza a pedra.png')
        tp = PhotoImage(file='Tesoura corta o papel.png')
        tl = PhotoImage(file='Tesoura decapita o lagarto.png')
        emp = PhotoImage(file='spockspock.png')

        def cmd1_click():
            global e1
            print('cmd1 click')
            r = random.choice(listas)
            lb22['text'] = r
            if(str(ed1.get())).isalpha():
                e1 = str(ed1.get()).capitalize()

            if r == 'Pedra' and e1 == 'Tesoura':
                lb33['text'] = 'Pedra amassa a Tesoura. Eu ganhei!'
                lbbackground['image'] = pt
            elif r == 'Pedra' and e1 == 'Papel':
                lb33['text'] = 'Papel cobre a Pedra. Você ganhou!'
                lbbackground['image'] = pp
            elif r == 'Pedra' and e1 == 'Lagarto':
                lb33['text'] = 'Pedra esmaga o Lagarto. Eu ganhei!'
                lbbackground['image'] = pl
            elif r == 'Pedra' and e1 == 'Spock':
                lb33['text'] = 'Spock vaporiza a Pedra. Você ganhou!'
                lbbackground['image'] = sp
            elif r == 'Pedra' and e1 == 'Pedra':
                lb33['text'] = 'Empate. Vamos de novo!'
                lbbackground['image'] = emp
            elif r == 'Papel' and e1 == 'Pedra':
                lb33['text'] = 'Papel cobre a Pedra. Eu ganhei!'
                lbbackground['image'] = pp
            elif r == 'Papel' and e1 == 'Tesoura':
                lb33['text'] = 'Tesoura corta o Papel. Você ganhou!'
                lbbackground['image'] = tp
            elif r == 'Papel' and e1 == 'Lagarto':
                lb33['text'] = 'Lagarto come o Papel. Você ganhou!'
                lbbackground['image'] = lp
            elif r == 'Papel' and e1 == 'Spock':
                lb33['text'] = 'Papel refuta o Spock. Eu ganhei!'
                lbbackground['image'] = ps
            elif r == 'Papel' and e1 == 'Papel':
                lb33['text'] = 'Empate. Vamos de novo!'
                lbbackground['image'] = emp
            elif r == 'Tesoura' and e1 == 'Pedra':
                lb33['text'] = 'Pedra amassa a Tesoura. Você ganhou!'
                lbbackground['image'] = pt
            elif r == 'Tesoura' and e1 == 'Papel':
                lb33['text'] = 'Tesoura corta o Papel. Eu ganhei!'
                lbbackground['image'] = tp
            elif r == 'Tesoura' and e1 == 'Lagarto':
                lb33['text'] = 'Tesoura decapita o Lagarto. Eu ganhei!'
                lbbackground['image'] = tl
            elif r == 'Tesoura' and e1 == 'Spock':
                lb33['text'] = 'Spock esmaga a Tesoura. Você ganhou!'
                lbbackground['image'] = st
            elif r == 'Tesoura' and e1 == 'Tesoura':
                lb33['text'] = 'Empate. Vamos de novo!'
                lbbackground['image'] = emp
            elif r == 'Lagarto' and e1 == 'Pedra':
                lb33['text'] = 'Pedra esmaga o Lagarto. Você ganhou!'
                lbbackground['image'] = pl
            elif r == 'Lagarto' and e1 == 'Papel':
                lb33['text'] = 'Lagarto come o Papel. Eu ganhei!'
                lbbackground['image'] = lp
            elif r == 'Lagarto' and e1 == 'Tesoura':
                lb33['text'] = 'Tesoura decapita o Lagarto. Você ganhou!'
                lbbackground['image'] = tl
            elif r == 'Lagarto' and e1 == 'Spock':
                lb33['text'] = 'Lagarto envenena o Spock. Eu ganhei!'
                lbbackground['image'] = ls
            elif r == 'Lagarto' and e1 == 'Lagarto':
                lb33['text'] = 'Empate. Vamos de novo!'
                lbbackground['image'] = emp
            elif r == 'Spock' and e1 == 'Pedra':
                lb33['text'] = 'Spock vaporiza a Pedra. Eu ganhei!'
                lbbackground['image'] = sp
            elif r == 'Spock' and e1 == 'Papel':
                lb33['text'] = 'Papel refuta o Spock. Você ganhou!'
                lbbackground['image'] = ps
            elif r == 'Spock' and e1 == 'Tesoura':
                lb33['text'] = 'Spock esmaga a Tesoura. Eu ganhei!'
                lbbackground['image'] = st
            elif r == 'Spock' and e1 == 'Lagarto':
                lb33['text'] = 'Lagarto envenena o Spock. Você ganhou!'
                lbbackground['image'] = ls
            elif r == 'Spock' and e1 == 'Spock':
                lb33['text'] = 'Empate. Vamos de novo!'
                lbbackground['image'] = emp
            else:
                lb33['text'] = 'Escreve direito!'
                lbbackground['image'] = shit

        #entradas
        ed1 = Entry(janela, font='Arial 15')
        ed1.place(x=160, y=5)

        #botão

        cmd1 = Button(janela, text='Start', command=cmd1_click, font='Arial 15', bg='Purple', fg='White')
        cmd1.place(x=400, y=5)

        #label
        lb1 = Label(janela, text='Sua escolha: ', font='Arial 15', bg='Purple', fg='White')
        lb1.place(x=20, y=5)
        lb2 = Label(janela, text='Escolha da máquina: ', font='Arial 15', bg='Purple', fg='White')
        lb2.place(x=20, y=35)
        lb3 = Label(janela, text='Resultado: ', font='Arial 15', bg='Purple', fg='White')
        lb3.place(x=150, y=380)
        lb22 = Label(janela, text='', font='Arial 15', bg='Purple', fg='White')
        lb22.place(x=210, y=35)
        lb33 = Label(janela, text='', font='Arial 15', bg='Purple', fg='White')
        lb33.place(x=255, y=380)
        lbLF = Label(janela, text='Developed by Lucas Franco', font='Arial 8')
        lbLF.place(x=690, y=400)

        janela.mainloop()
