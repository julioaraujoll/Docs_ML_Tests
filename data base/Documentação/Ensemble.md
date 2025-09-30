# Ensemble Documentação

- Ensemble combina múltiplos algorítimos de aprendizagem  para obter uma  melhor performance prevista que apenas um único modelo. Não existe um número predefinido a se considerar, e alguns objetivos de negócios podem necessitar mais modelos que outros

## Tipos de métodos de Ensemble

### Bagging:
Também é conhecido como um bootstrap(inicialização) de agregação. É similar ao Random Forest, porém, o Bagging utiliza todos os preditores, enquanto o Random Foreste utiliza apenas um subset de preditores em cada árvore.
É selecionada uma amostra aleatória dos dados do set de treinamento com substituição, a qual permite a duplicação de amosras de instancias em um set
#### Passos:
- Geração de múltiplos bootstrap reamostras.
- Rodando um algoritimo em cada reamostra para fazer previsões
- Combinando as previsões pela média das previsões ou pegando o maior voto(para classificação)
#### Vantagens:
- O modelo de processamento é fraco e  não exige nenhum tipo de conceitos matemáticos, e pode lidar com perda de valores
- Tem um efeito sgnificante na redução de variância na calssificação de alta variância
- Provem um imparcialidade estimada do, a qual corresponde a média de erro/perda que todos esses classificadores rendem
#### Desvantagens:
- É computacionalmente caro devido ao uso de modelos diverificados
- A media desenvolvida entre as  previsões tornam a interpretação do resultado final mais difícil
### Boosting
Boosting utiliza de uma abordagem sequencial, onde as previsões so modelo atual é transferida para o próximo
Cada modelo iterativamente foca na observação que são classificados incorretamente pelos antecessores.
#### Vantagens:
- Semelhante ao Bagging, é de fácil implementação e entendimento. Além disso, não requer nenhum preprocessamento e consegue lidar com perda de valores
- Eficientemente reduz as parciliades/tendências(bias)
- Priorizam amostras que aumentam a precisão geral durante o treinamento. Ess eprocesso reduz a dimensionalidade dos dados, assim reduzindo o tempo computacional
#### Desvantagens:
- A abordagem sequencial faz o próximos modelos corrijam os erros do antecessor. Tornando o modelo geral vunerável a valores discrepantes
- Não é escalável pelo mesmo motivo do aspecto sequencial

