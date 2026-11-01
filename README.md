# Programa: Pesquisa de Satisfação - TudoWeb
# Configurado para 10 entrevistados para testes (conforme requisito da atividade)

total_entrevistados = 10

qtd_excelente = 0
qtd_ruim = 0

print("=== PESQUISA DE SATISFAÇÃO - TUDOWEB ===")
print(f"Iniciando a pesquisa com {total_entrevistados} entrevistados.\n")

for i in range(1, total_entrevistados + 1):
    print(f"--- Entrevistado {i} de {total_entrevistados} ---")
    
    # Coleta de dados básicos
    nome = input("Digite o nome do entrevistado: ")
    
    # Validação simples da idade
    while True:
        try:
            idade = int(input("Digite a idade do entrevistado: "))
            if idade > 0:
                break
            print("Por favor, digite uma idade válida maior que zero.")
        except ValueError:
            print("Entrada inválida. Digite um número inteiro para a idade.")
            
    # Coleta e validação da opinião
    print("Opinião sobre o atendimento:")
    print("  [1] EXCELENTE")
    print("  [2] BOM")
    print("  [3] RUIM")
    
    while True:
        try:
            opiniao = int(input("Digite o código da sua opinião (1, 2 ou 3): "))
            if opiniao in [1, 2, 3]:
                break
            print("Opinião inválida! Escolha 1, 2 ou 3.")
        except ValueError:
            print("Entrada inválida. Digite apenas o número correspondente.")

    # Estrutura de decisão para contabilizar as respostas
    if opiniao == 1:
        qtd_excelente += 1
    elif opiniao == 3:
        qtd_ruim += 1
    # Nota: A opção 2 (BOM) é registrada no fluxo, mas não possui contagem específica exigida no relatório final.

    print("-" * 35 + "\n")

# Exibição dos resultados finais
print("=" * 40)
print("       RESULTADO FINAL DA PESQUISA       ")
print("=" * 40)
print(f"Total de entrevistados: {total_entrevistados}")
print(f"a) Quantidade de respostas 'EXCELENTE': {qtd_excelente}")
print(f"b) Quantidade de respostas 'RUIM': {qtd_ruim}")
print("=" * 40)
