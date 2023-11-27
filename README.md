# Banco-de-dados-II.I
Exercicio prático.



Uma loja tem um banco de dados que contém todo o controle de vendas de produtos e de cadastro de clientes. Pensando nisso, crie uma função para somar todos os clientes que foram cadastrados na loja durante um dia.

def somar_clientes_cadastrados(dados_vendas):
    # Inicializa o contador de clientes
    total_clientes = 0
    
    # Percorre os dados de vendas
    for venda in dados_vendas:
        # Verifica se o cliente já foi cadastrado
        if venda['cliente'] not in dados_vendas[:dados_vendas.index(venda)]:
            total_clientes += 1
    
    return total_clientes
