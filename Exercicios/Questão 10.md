Função MultiplicaçãoDeMatrizes(matrizA, matrizB):
    # Verifica se o número de colunas em matrizA é igual ao número de linhas em matrizB
    Se tamanho(matrizA[0]) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser multiplicadas. Dimensões incompatíveis."
    Senão:
        linhasA <- tamanho(matrizA)
        colunasA <- tamanho(matrizA[0])
        colunasB <- tamanho(matrizB[0])
        matrizResultado <- novaMatriz(linhasA, colunasB)

        # Loop para percorrer cada elemento da matriz resultado
        Para i de 0 até linhasA-1 faça:
            Para j de 0 até colunasB-1 faça:
                # Inicializa o elemento da matriz resultado como 0
                matrizResultado[i][j] <- 0
                Para k de 0 até colunasA-1 faça:
                    # Calcula o produto da linha i de matrizA com a coluna j de matrizB
                    matrizResultado[i][j] <- matrizResultado[i][j] + (matrizA[i][k] * matrizB[k][j])

        Retornar matrizResultado
