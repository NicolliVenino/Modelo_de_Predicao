# Modelo Preditivo de Classificação Binária Supervisionada

&nbsp;O modelo configura-se como supervionado, haja vista que o dataset contempla dados rotulados, e como de classificação, em razão da demanda de retornar um valor discreto como resuldado final, na variável label. 

&nbsp;A primeira etapa do desenvolvimento do modelo consistiu em rotular os dados manualmente, pois o dataset fornecido continha apenas as amostras de texto. Nesse sentido, foi adicionado a coluna "labels" (variável-alvo), de modo que 0 significa "não possui dados pessoais" e 1 significa "possui dados pessoais". 
&nbsp;A partir desse processo, observou-se um desbalanceamento entre as classes, com predominância de textos classificados como contendo dados pessoais. Esse cenário poderia influenciar negativamente o aprendizado do modelo, levando-o a favorecer a classe majoritária. Diante disso, foram adotadas estratégias para reduzir esse efeito, como o uso de pesos de classe durante o treinamento e a priorização da métrica de recall, considerando a importância de minimizar a ocorrência de falsos negativos.
&nbsp;Além disso, foi aplicada a validação cruzada estratificada, com o objetivo de garantir uma avaliação mais consistente e preservar a proporção entre as classes nos diferentes subconjuntos de treino e validação. Por fim, o modelo foi construído a partir do BERTimbau, um modelo pré-treinado em língua portuguesa, ajustado por meio de fine tuning para a tarefa de identificação de dados pessoais em textos.

### Pré-requisitos e Configuração do Ambiente

#Pré-requisitos

&nbsp;Para a correta execução do projeto, é necessário possuir os seguintes requisitos instalados no ambiente:

- Python 3.9 ou superior;

- pip (gerenciador de pacotes do Python);

- Git (opcional, para clonagem do repositório);

- Sistema operacional compatível: Linux, macOS ou Windows.

*Recomenda-se a utilização de ambiente virtual para evitar conflitos de dependências.*

##Criação e configuração do ambiente

### 1. Clonar o repositório
``
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
``
### 2. Criar ambiente virtual
**Para Linux:**
``
python3 -m venv venv
``
**Para Windowns:**
``
python -m venv venv
``
### 3. Ativar o Ambiente Virtual
**Para Linux:**
``
source venv/bin/activate
``
**Para Windowns:**
``
venv\Scripts\Activate
``
### 4. Instalar as dependências
``
pip install --upgrade pip
pip install -r requirements.txt
``
### 5. Comando de Execução
``
python main.py
``
