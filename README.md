# Programa: Pesquisa de Satisfação - TudoWeb
# Lista contendo 10 entrevistas pré-preenchidas para demonstração e testes

# Cada item da lista representa um entrevistado: [Nome, Idade, Opinião (1-Excelente, 2-Bom, 3-Ruim)]
entrevistas = [
    ["Ana Silva", 28, 1],
    ["Carlos Souza", 34, 2],
    ["Mariana Costa", 22, 1],
    ["João Pedro", 45, 3],
    ["Beatriz Lima", 30, 1],
    ["Lucas Mendes", 26, 2],
    ["Fernanda Rocha", 40, 3],
    ["Gabriel Alves", 29, 1],
    ["Juliana Ribeiro", 38, 2],
    ["Rafael Santos", 31, 1]
]

total_entrevistados = len(entrevistas)
qtd_excelente = 0
qtd_ruim = 0

print("=== PESQUISA DE SATISFAÇÃO - TUDOWEB ===")
print(f"Processando dados de {total_entrevistados} entrevistados...\n")

# Estrutura de repetição FOR iterando sobre cada entrevista já cadastrada
for i, dados in enumerate(entrevistas, start=1):
    nome = dados[0]
    idade = dados[1]
    opiniao = dados[2]
    
    # Traduzindo o código da opinião para texto para exibição
    if opiniao == 1:
        texto_opiniao = "EXCELENTE"
        qtd_excelente += 1
    elif opiniao == 2:
        texto_opiniao = "BOM"
    else:
        texto_opiniao = "RUIM"
        qtd_ruim += 1

    print(f"Entrevistado {i}: {nome} | Idade: {idade} | Opinião: {texto_opiniao}")

# Exibição dos resultados finais
print("\n" + "=" * 40)
print("       RESULTADO FINAL DA PESQUISA       ")
print("=" * 40)
print(f"Total de entrevistados: {total_entrevistados}")
print(f"a) Quantidade de respostas 'EXCELENTE': {qtd_excelente}")
print(f"b) Quantidade de respostas 'RUIM': {qtd_ruim}")
print("=" * 40)
