# Project---1-python-
Inicialização em Python 
# Importando módulos regex - tratamento de caracter
import re

# Declaração de variáveis globais
funcionarios = {}
id_counter = 1
def entrada_str(prompt):
    while True:
        regexp = re.compile('[^a-zA-Z]+') # Expressões regulares (regex)
        entrada = input(prompt).strip()  # Remove espaços em branco no início/fim

        if entrada == '':  # Verifica se a entrada está vazia
            print("Por favor, insira um texto válido (não vazio).")
        elif regexp.search(entrada):
            print("Por favor, insira um texto válido (não caracteres).")
        else:
            try:
                # Tenta converter para número para verificar se é numérico
                float(entrada)
                print("Por favor, insira um texto, não um número.")
            except ValueError:
                # Se não for número, retorna a entrada como válida
                return entrada


