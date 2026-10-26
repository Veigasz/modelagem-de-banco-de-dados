# **Entrega 2: Modelagem de Banco de Dados**

**Sistema de Gestão de Informações – Mont Ararat Burger House**


** Integrantes do Grupo (Nomes e RGMs):**   
* – Gustavo Almeida de Lima, RGM: 48157899  
* – Mariana Brito Farias, RGM: 48134767   
* – Ynaê Ribeiro da Silva, RGM: 47987111

-------------------------------------------------------------------------
# **1\. Caracterização da Organização**

### **Nome e Natureza da Organização:**

* Razão Social: MONT ARARAT BURGER HOUSE LTDA  
* Nome Fantasia: Mont Ararat Burger House  
* CNPJ: 46.336.364/0001-48  
* Natureza Jurídica: Sociedade Empresária Limitada (LTDA) / Organização Privada com Fins Lucrativos.  
* Atividade Econômica Principal (CNAE): Lanchonetes

-------------------------------------------------------------------------

  **Evidências da organização:**

* **Logradouro:** Rua Vercínio Pereira de Souza, 1199, São Paulo, São Paulo,   
* **Bairro:** São Mateus  
* **CEP:** 03945-000  
* **Município:** São Paulo  
* **Estado:** [São Paulo](https://cnpj.biz/empresas/estado/SP)  
* **Google Maps:** [Mont Ararat Hamburgueria] (https://maps.app.goo.gl/tbeaWRYgZ4ftwdSMA)  
* **Instagram:** [https://www.instagram.com/montararatburger/](https://www.instagram.com/montararatburger/)   
* **Contato (telefone):** (11)2015-5871  
* **Pesquisa de Campo:** Entrevista direta realizada com a gerência local e observação de campo, acompanhada de registros fotográficos do cardápio, fita de fechamento de caixa e planilhas operacionais. 

-------------------------------------------------------------------------

# **Contexto e Porte:**

A Mont Ararat Burger House é uma rede regional de hamburguerias artesanais. Classifica-se formalmente como Microempresa (ME) / Empresa de Pequeno Porte (EPP). Fundada originalmente em 2016, a marca conta com unidades em São Paulo (unidade de estudo em São Mateus), Suzano e Mogi das Cruzes.
# **Tamanho da Operação:**

* **Infraestrutura Física:** Salão com capacidade para 30 mesas presenciais, com gestão dinâmica de ocupação e comandas.  
* **Terminais de Atendimento:** 2 Terminais de caixa físicos operando simultaneamente (Caixa 01: Salão / Caixa 02: Delivery e Balcão).  
* **Arquitetura de Atendimento:** Operação híbrida de alta rotatividade em tempo real, integrando lançamentos presenciais e pedidos concorrentes via Delivery/Balcão com impressão na cozinha.  
* **Equipe e Turnos:** Operação de terça a domingo e feriados (18h às 23h em dias úteis; 18h às 00h aos fins de semana). A equipe é composta por 13 funcionários fixos (CLT) e cerca de 15 freelancers ativados aos finais de semana, divididos entre turnos de pré-preparo (manhã) e operação/atendimento (tarde/noite).

-------------------------------------------------------------------------

# **Volume de Atividades:**

* **Fluxo de Atendimentos: (Salão)**  
  * Média Diária (Dias úteis): 30 a 90 comandas/atendimentos.  
  * Média Diária (Finais de semana / Pico): 70 a 140 comandas/atendimentos.  
  * Projeção Mensal: 1000 a 1500 comandas processadas no salão.  
  Movimentação Financeira: 
  * Dia de Baixo Movimento: \~R$3.500,00/dia (com taxa de serviço).  
  * Dia de Pico (Fim de semana): \~R$10.000,00 a R$14.000,00/dia (com taxa de serviço).
* **Fluxo de Atendimentos: (Delivery / Balcão)**
  * Obs: Pelo balcão não possui taxa de serviço e entrega.  
  * Média Diária (Dias úteis): 30 a 90 comandas/atendimentos (Números Parecidos ao do salão). 
  * Média Diária (Finais de semana / Pico): 150 a 250 comandas/atendimentos.  
  * Projeção Mensal: 2000 a 3000 comandas processadas no salão.  
  Movimentação Financeira:
  * Dia de Baixo Movimento: \~R$3.500,00/dia (com taxa de entrega).  
  * Dia de Pico (Fim de semana): \~R$20.000,00 a R$25.000,00/dia (com taxa de entrega). 
 
-------------------------------------------------------------------------

# **Problemas e Necessidades Identificados (Crise Operacional):**

* **1. Gestão Descentralizada de Compras e Estoque:** O controle de insumos e compras é realizado manualmente por planilhas avulsas e não integradas. A ausência de cálculo automatizado de Ficha Técnica resulta em compras imprecisas e custos operacionais não contabilizados em tempo real.
* **2. Ausência de Cadastro Centralizado de Pessoas:** Inexistência de registros formais de clientes para ações de fidelização/aniversariantes e ausência de vinculação formal de colaboradores/freelancers aos lançamentos de vendas.
* **3. Falta de padronização e Rastreabilidade do Caixa:** Necessidade de vincular as vendas fracionadas (divisão de contas) e sangrias aos terminais e operadores responsáveis.

-------------------------------------------------------------------------

# **Escopo do Sistema**


# **Justificativa da Escolha**

A escolha da unidade São Mateus da Mont Ararat Burger House justifica-se pelo acesso direto e irrestrito do grupo às rotinas operacionais (um dos integrantes é colaborador do local). O ambiente apresenta complexidade ideal para modelagem de dados: possui volumetria rica (30 mesas, 2 caixas, múltiplos turnos e ficha técnica artesanal) sem exceder o escopo da disciplina.

-------------------------------------------------------------------------
# **2. Processos de Negócio**

### **Principais Processos Mapeados**
* **Pré-preparo e Produção de Insumos (Turno da Manhã)**: Manipulação de insumos artesanais (moagem de carnes de 180g e 120g, preparo de molhos da casa, corte de vegetais, porcionamento).
* **Abertura e Operação de Caixa:** Abertura de sessões por terminal (Salão/Delivery) com registro de fundo de reserva (R$150,00) e atribuição de operador.
* **Atendimento de Salão e Gestão de Comandas**: Abertura de comanda associada à mesa, lançamento progressivo de itens por garçom e controle de transferência entre mesas.
* **Pedido de Delivery e Balcão:** Processo voltado para o atendimento de clientes que compram para retirada no balcão, via 99 (Aplicativo de Delivery) ou  por WhatsApp. Envolve o registro dos dados do cliente (no caso de delivery), escolha de produtos, cálculo automático da taxa de entrega baseada no endereço ou seleção de retirada, escolha da forma de pagamento online ou na entrega, e o direcionamento imediato do pedido para a fila de produção da cozinha, integrando-se ao controle de expedição e entrega.
* **Cancelamento de Item ou de Pedido:** Fluxo de exceção que rege o cancelamento de itens já lançados em comandas ou de pedidos completos. Exige a identificação do operador responsável e justificativa obrigatória para a administradora do caixa do dia respectivo. O sistema deve registrar o evento para fins de auditoria de estoque (estornando os insumos utilizados se aplicável) e controle gerencial de perdas.
* **Gestão do Cardápio e Preços:** Processo administrativo responsável pela criação, alteração e descontinuação de produtos, categorias (lanches, bebidas, acompanhamentos) e ingredientes adicionais. Permite a definição de preços vigentes, controle de disponibilidade de itens em tempo real (esgotar produto) e parametrização de combos ou promoções aplicáveis aos canais de venda (salão, balcão e delivery).
* **Cardapio**:
<img width="300" height="400" alt="WhatsApp Image 2026-10-26 at 09 47 25" src="https://github.com/user-attachments/assets/582071cb-4771-4d7c-82e3-d9c1afa14fab" />
<img width="300" height="400" alt="WhatsApp Image 2026-10-26 at 09 47 25 (1)" src="https://github.com/user-attachments/assets/b4d9b61c-e444-4abe-a445-68658e29cfaf" />

* **Cadastro de fornecedores**: Atualmente o Cadastro de fornecedores é ausente na Empresa entretanto possui seus fornecedores fixos para certos produtos (Carne, pães, hortifrúti e bebidas). Deve-se Armazena dados cadastrais, CNPJ, prazos de entrega negociados, formas de pagamento e os insumos específicos fornecidos por cada parceiro comercial.
* **Compra de Insumos (Geração de Pedidos de Compra:)** Processo periódico de análise de estoque mínimo e projeção de demanda para a geração de listas de compras. Com base nas baixas operacionais e no saldo atual de insumos, o sistema auxilia na criação de ordens de compra a serem enviadas aos fornecedores cadastrados, prevenindo rupturas na produção.
* **Recebimento e Conferência da Mercadoria:** Processo físico e lógico de entrada de insumos no estabelecimento. No momento da entrega pelo fornecedor, os produtos são conferidos quantitativa e qualitativamente em relação à nota fiscal e ao pedido de compra original, registrando-se a entrada oficial dos lotes no estoque e atualizando os custos unitários dos insumos.
* **Controle de Estoque:** Gestão contínua das entradas, saídas e saldos de insumos e produtos acabados. O sistema realiza a baixa automática de estoque com base na ficha técnica dos itens vendidos (ex: a venda de um hambúrguer desconta pão, carne, queijo e embalagem), além de permitir ajustes manuais para perdas, desperdícios, quebras e contagens periódicas de inventário físico.
* **Escala de Funcionários e Freelancers:** Processo de organização e planejamento da jornada de trabalho da equipe da hamburgueria (chapa, atendimento, caixa). Permite o registro de turnos fixos dos colaboradores CLT e o cadastro/alocação de freelancers para dias de maior movimento, controlando horários de entrada, saída e custos operacionais de mão de obra. Freelancers que trabalham no Turno matutino Entram as 8, e são liberados as 15 e30, Freelancers que Trabalham no turno Integral/Noturno, Entram a partir das 16 e 30 (Ou 15 e 3 com direito a 1 hora de almoço) São liberados as 23:30 em dias úteis e 00:30 em Finais de semana.
* **Produção na Cozinha (Chapa/Montagem)**: Recebimento dos itens de pedidos fracionados por comanda, controle de observações (ponto de carne, remoção de itens)
* **Fechamento de Conta e Recebimento Fracionado**: Consolidação do consumo, aplicação/isenção opcional da taxa de serviço de 10%, registros de pagamentos fracionados (N formas de pagamento) e encerramento da comanda com liberação da mesa.
* **Controle Financeiro e Fechamento de Turno**: Apuração das entradas por meio de pagamento, registro de sangrias/suprimentos, conferência de divergências de caixa e fechamento do turno.
