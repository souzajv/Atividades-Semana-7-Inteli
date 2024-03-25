Algoritmo Simulador_Carro_Elétrico
    // Entradas
    velocidade_inicial = Ler_Velocidade_Inicial()
    taxa_aceleracao = Ler_Taxa_Aceleracao()
    distancia = Ler_Distancia()
    velocidade_maxima = Ler_Velocidade_Maxima()
    tempo_maximo = Ler_Tempo_Maximo()

    // Variáveis
    velocidade_atual = velocidade_inicial
    tempo = 0
    distancia_percorrida = 0

    Enquanto (distancia_percorrida < distancia) E (tempo <= tempo_maximo) E (velocidade_atual < velocidade_maxima) faça
        // Calcular nova velocidade e distância percorrida
        velocidade_atual = velocidade_atual + taxa_aceleracao * tempo
        distancia_percorrida = distancia_percorrida + velocidade_atual * tempo
        tempo = tempo + 1 // Incrementar tempo em minutos
    Fim Enquanto

    Se (distancia_percorrida >= distancia) Então
        Escrever "O carro completou a corrida em ", tempo, " minutos."
    Senão
        Se (tempo > tempo_maximo) Então
            Escrever "O carro não completou a corrida dentro do tempo máximo permitido."
        Senão
            Escrever "O carro atingiu a velocidade máxima permitida."
        Fim Se
    Fim Se

FimAlgoritmo