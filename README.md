# Modelling the dynamics of language death
This repository describes the "dynamics of language death modeling" assigment of the EMAP-FGV biological modeling discipline.

#### Link for report
Report in overleaf: [report PDF](https://pt.overleaf.com/read/vqjfqhspnmdb).

#### Main article of reference
Article [Modelling the dynamics of language death](https://www.nature.com/articles/424900a).


### Ideas



### O que é dito no artigo main

Milhares de línguas do mundo estão desaparecendo em um ritmo alarmante, com 90% delas sendo esperado que desapareçam com a geração atual [https://pascal-francis.inist.fr/vibad/index.php?action=getRecordDetail&idt=6143996]. Aqui, desenvolvemos um modelo simples de competição linguística que explica dados históricos sobre o declínio do galês, gaélico escocês, quíchua (a língua indígena sobrevivente mais comum nas Américas) e outras línguas ameaçadas de extinção. Um parâmetro linguístico que quantifica a ameaça de extinção da linguagem pode ser derivado do modelo e pode ser útil no projeto e avaliação de programas de preservação da linguagem.

Modelos anteriores de dinâmica da linguagem focaram na transmissão e evolução da sintaxe, gramática ou outras propriedades estruturais da própria linguagem [vide refecencias 2, 3, 4, 5, 6 e 7]. Em contraste, o modelo que descrevemos aqui idealiza as línguas como fixas e como concorrentes entre si por falantes. Para simplificar, também assumimos uma população altamente conectada, sem estrutura espacial ou social, na qual todos os falantes são monolíngues.

Considere um sistema de duas línguas concorrentes, X e Y, no qual a atratividade de uma língua aumenta tanto com seu número de falantes quanto com seu status percebido [https://scholar.google.com/scholar_lookup?title=Reversing%20Language%20Shift&publication_year=1991&author=Fishman%2CJA] (um parâmetro que reflete as oportunidades sociais ou econômicas oferecidas a seus falantes). Suponha que um indivíduo converta de Y para X com uma probabilidade, por unidade de tempo, de P_{yx} (x, s), onde x é a fração da população falando X e 0 ≤ s ≤ 1 é uma medida do status relativo de X. Um modelo mínimo para mudança de idioma é, portanto,

<img src="http://www.sciweavers.org/tex2img.php?eq=%5Cfrac%7Bdx%7D%7Bdy%7D%20%3D%20y%20P_%7By%20x%7D%20%28x%2C%20s%29%20-%20x%20P_%7Bx%20y%7D%20%28x%2C%20s%29&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0" align="center" border="0" alt="\frac{dx}{dy} = y P_{y x} (x, s) - x P_{x y} (x, s)" width="228" height="47" />

Onde y = 1 - x, é a fração complementar da população que fala Y no tempo t. Por simetria, a troca de línguas deve produzir a mesma probabilidade de transição que uma troca na fração de falantes e status relativo; assim, P_{xy} (x, s) = P_{yx} (1 - x, 1 - s). Também assumimos que ninguém adotará uma linguagem que não tenha falantes (P_{yx} (0, s) = 0) ou nenhum status (P_{yx} (x, 0) = 0), e que P_{yx} é suave e monotonicamente crescente em ambos os argumentos.

Essas suposições suaves implicam que a primeira equação tem genericamente três pontos fixos. Destes, apenas x = 0 e x = 1 são estáveis. O modelo, portanto, prevê que duas línguas não podem coexistir de forma estável - uma acabará por levar a outra à extinção.

Para testar nosso modelo, coletamos dados sobre o número de falantes de línguas ameaçadas de extinção em 42 regiões do Peru, Escócia, País de Gales, Bolívia, Irlanda e Alsácia-Lorena, quatro das quais são mostradas na [figura do artigo]. Ajustamos as soluções do modelo aos dados, assumindo funções de transição das formas P_{yx} (x, s) = s*c*x^a e Pxy (x, s) = (1 - s)*c*(1 - x)^a. Inesperadamente, o expoente a foi considerado aproximadamente constante entre as culturas, com a = 1,31 ± 0,25 (média ± desvio padrão; mais detalhes estão disponíveis com os autores).
