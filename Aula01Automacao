import pyautogui
import time

#Para rodar o código: usar Jupyter
# pyautogui.click -> clicar como mouse
# pyautogui.write -> escreve um texto
# pyautogui.press -> apertar uma tecla
# pyautogio.hotkey -> aperta uma combinação de teclas
# todos os x e y tem localizações que não funcionarão em seu monitor. Run o print()

pyautogui.PAUSE = 1
#este pede pr entre cada comando, esperar 1 seg

#passo 1: Acessar o sistema da empresa
pyautogui.hotkey(“ctrl”,”t”)
pyautogui.write(“https://pages.hashtagtreinamentos.com/aula1-intensivao-sistema”)
pyautogui.press(”enter”)

time.sleep(5)

#Passo 2> Fazer login no sistema

pyautogui.click(x=983, y=441)
pyautogui.write(“meu login”)
pyautogui.click(x=912, y=529)
pyautoguiwrite(“minha senha”)
pyautogui.click(x=1036 ,y=609)

time.sleep(5)

#Passo 3: Baixar a base de dados

pyautogui.click(x=504, y=440)
pyautogui.click(x=872, y=212)
pyautogui.click(x=990, y=660)

#Passo 4: Calcular os indicadores
import pandas as pd

# importar a base de dados
tabela = pd.read_csv(r“C:\Users\jacke\Downloads\Compras.cvs”, sep=”;”)
display(tabela)

#calculo dos indicadores
#total gasto -> somar a coluna valor final
total_gasto = tabela[“ValorFinal”].sum()

#quantidade -> somar a coluna quantidade
quantidade = tabela[“Quantidade”].sim()

#preço medio -> total gasto / quantidade
preco_medio = total_gasto / quantidade

print(total_gasto)
print(quantidade)
print(preco_medio)

#Passo 5: Enviar o email para a diretoria/destinatario

#entrar no meu email
pyautogui.hotkey(“ctrl”,”t”)
pyautogui.write(“https://mail.google.com/mail/u/0/#inbox”)
pyautogui.press(“enter”)

time.sleep(5)

#clicar em escrever
pyautogui.write(“jackelinekaneko@gmail.com”)
pyautogui.press(“tab”) #seleciona o email

pyautogui.press(“tab”) #passar pro campo assunto
pyautogui.write(Relatorio de Compras”)

pyautogui.press(“tab”) #passar pro campo do corpo do email

texto = “””
Prezados, 

Segue o relatório de compras

Total Gasto: R${total_gasto:,.2f}
Quantidade de Produtos: {quantidade:,}
Preço Médio: R${preco_medio:,.2f}

Qualquer dúvida só me falar.

Att;
Jackeline Kaneko
“””

pyperclip.copy(texto)
pyautogui.hotkey(“ctrl”,”v”)

#enviar
pyautogui.hotkey(“ctrl”,”enter”)
