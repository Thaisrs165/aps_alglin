# aps_alglin

1. Carregamento dos Áudios
Para testar seus próprios áudios, basta carregá-los no projeto e inserir o caminho correto do arquivo no comando librosa.load, conforme indicado no Passo 1.

2. Requisitos dos Áudios
Certifique-se de utilizar dois áudios estéreos com mesma duração e mesma taxa de amostragem, pois isso é essencial para a correta aplicação da separação de fontes.

3. Configuração da Matriz de Mistura (Passo 3)
A matriz A representa a mistura dos sinais. Nela, você define a proporção de cada fonte em cada microfone, simulando diferentes cenários de captação.

4. Simulação de Múltiplos Microfones
Para separar dois sinais distintos, é necessário simular pelo menos dois microfones. Isso ocorre porque precisamos de no mínimo o mesmo número de sensores que de fontes para estimar corretamente cada componente. Ou seja, para três fontes, são necessários pelo menos três microfones (três pontos de vista distintos).

5. Número de Componentes (Passo 4)
Caso esteja testando com mais de duas fontes, atualize o parâmetro n_components para refletir a quantidade de fontes utilizadas no seu teste.

6. Reprodução dos Áudios Separados
Se estiver trabalhando com mais de duas fontes, adicione novas linhas de reprodução de áudio como: "Audio(S[:, x], rate=sr_voz)".
Substitua "x" pelo índice do componente que deseja ouvir e "sr_voz" pela taxa de amostragem correspondente.

VÍDEO EXPLICATIVO: https://youtu.be/3rHEfYFcejQ
SLIDES: https://docs.google.com/presentation/d/1oT4eywwc_DdDZ-WOGK3_U9Hok8s3tMnSL4DX3-fK6jg/edit?usp=sharing
