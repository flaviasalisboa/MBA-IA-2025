Modelando Grafos com LOGS de Acesso Web Apache - MBA-IA-BIGDATA 2025 (TURMA 4)

LISBOA, F.O.S.S. Experimentação TCC do MBA em Inteligência Artificial e Big Data: Modelando grafos com logs de acesso web Apache.
São Carlos: IFSC/USP, 2025. Disponível em: https://www.ifsc.usp.br/~flavia/mba-ia.

Os experimentos foram realizados utilizando-se de quatro modelos de grafos detalhados a seguir:

1) Grafos de similaridade entre arquivos de log.
•	Utilizam-se as técnicas TF-IDF + similaridade cosseno e TF-IDF + similaridade k-NN.
•	Comparar cada log diário com o log de invasão do caso concreto do ataque de injeção de SQL e detectar se algum dia apresenta padrão semelhante ao log do dia de ataque.

2) Grafos bipartidos e tripartidos.
•	Construção de grafos bipartidos de arquivos de log suspeitos, em que os nós são dois atributos extraídos dos registros de log com o objetivo de comparação das relações entre esses atributos com os mesmos atributos do log de invasão.
o	URL x Códigos de Resposta HTTP: relaciona URLs acessadas com os códigos de resposta HTTP (por exemplo, 200, 404, 403, 500).
•	Construção de grafos tripartidos de arquivos de log suspeitos em que os nós são os três atributos extraídos dos registros de log.
  o	IP × URL × Códigos de Resposta HTTP: grafo com três tipos de nós, mostrando o caminho completo de acesso, de quem acessou (IP), o que acessou (URL) e com qual resultado (código de resposta HTTP – erro ou sucesso no acesso).

3) Grafos temporais por minuto e por hora com animação.
•	Temporal x Código de Resposta de Erro 404: considera o tempo como dimensão (em minutos) e relaciona aos códigos de resposta de erro 404 registrados no período os IPs ou URLs.
•	Temporal com Janelas por Hora (interativo e animado): variações com relações entre URL x Código de Resposta HTTP, IP x URL e bipartido URL x Código de Resposta HTTP (filtro por 404 e 200).

4) Grafos de detecção de comunidades usando o algoritmo Louvain.
•	Detectar comunidades de endereços IP com comportamentos similares, a fim de identificar grupos de endereços IP possivelmente maliciosos, por exemplo, aqueles endereços que geram muitos registros de log com erro de acesso com os códigos de resposta de erro mais comuns como 404, 403 e 500.
  o	Nós do grafo: endereços IP.
  o	Arestas do grafo: conectam endereços IP que receberam o mesmo código de resposta HTTP.
