# Requisitos Funcionais - Sistema **Tudo Fresco**

## Visão Geral

O sistema **Tudo Fresco** é uma plataforma digital que conecta produtores de alimentos a compradores, facilitando a negociação direta e permitindo que grandes demandas sejam atendidas por múltiplos pequenos produtores, impulsionando a economia local e promovendo o consumo de alimentos frescos e de qualidade.

---

## Requisitos Funcionais - MVP

### 1. Cadastro de Usuários
- O sistema deve permitir que qualquer usuário crie uma conta na plataforma (sign up).
- O sistema deve permitir que o usuário altere seus dados pessoais posteriormente.
- O sistema deve permitir o upload e alteração da foto de perfil do usuário.

### 2. Cadastro de Empresas
- O sistema deve permitir que usuários cadastrem empresas do tipo **Comprador** ou **Produtor**.
- A validação dos dados empresariais deve ser feita via integração com a **API da Receita Federal**.

### 3. Cadastro de Endereço
- O sistema deve permitir o cadastro de endereços comerciais para cada empresa.
- O preenchimento de endereço deve ser assistido por integração com a **API dos Correios**.

### 4. Geolocalização Aproximada
- Ao cadastrar um endereço, o sistema deve estimar e armazenar automaticamente suas coordenadas geográficas (latitude e longitude), para futura exibição em mapas e também para determinar a relevância de demandas no feed.

### 5. Gestão de Empresas Vinculadas ao Usuário
- O sistema deve permitir que o usuário visualize e acesse suas empresas cadastradas.
- Um mesmo usuário pode estar vinculado a múltiplas empresas com diferentes perfis (comprador ou produtor).

### 6. Gestão de Demandas (Apenas Empresas Compradoras)
- O sistema deve permitir que empresas do tipo **Comprador**:
  - Criem demandas de produtos.
  - Editem demandas abertas anteriormente.
  - Vinculem produtos previamente cadastrados à demanda.
  - Listem demandas por status.

### 7. Cadastro de Produtos para Demandas
- O sistema deve permitir que o usuário cadastre novos produtos durante a criação de uma demanda.

### 8. Busca Inteligente de Produtos
- O sistema deve oferecer uma busca com **autocomplete** para facilitar a seleção de produtos ao criar uma demanda.
- Caso o produto buscado não exista, deve ser possível cadastrá-lo manualmente.

### 9. Feed de Demandas (Apenas Empresas Produtoras)
- O sistema deve disponibilizar um feed de demandas com scroll infinito, similar ao Instagram.
- As demandas exibidas no feed devem:
  - Estar com o status “Em aberto”.
  - Ser de compradores localizados em um raio de até **10 km** da localização do produtor.

### 10. Contato com Compradores
- O sistema deve permitir que produtores interessados entrem em contato com compradores por:
  - WhatsApp (mensagem pré-preenchida).
  - E-mail (mensagem pré-preenchida).
- A mensagem deve conter automaticamente dados da empresa produtora e do produto oferecido.

---

## Requisitos Funcionais Planejados (Pós-MVP)

### 1. Implementação do Mapa de Demandas
- Exibir um mapa interativo com as localizações das demandas abertas, baseado nas coordenadas geográficas estimadas.

### 2. Certificação de Produtos
- Permitir o upload e exibição de selos de certificação (TECPAR, IBD, EcoCert).

### 3. Sistema de Avaliação
- Permitir que compradores avaliem produtos recebidos e produtores avaliados.
- As avaliações devem conter notas, comentários e feedback sobre entrega e atendimento.

### 4. Venda Direta
- Permitir a publicação de produtos por produtores para compra direta (sem passar por demanda).
- Integração com meio de pagamento (Pix, boleto, cartão).

### 5. Divisão de Demandas entre Múltiplos Produtores
- Permitir que uma única demanda seja atendida por múltiplos produtores, com rastreamento individual da contribuição de cada um.

### 6. Sistema de Leilões para Compras em Lote
- Permitir que compradores lancem demandas com possibilidade de leilão inverso.
- Produtores podem disputar o fornecimento com preços e prazos distintos.

### 7. Rede Colaborativa entre Produtores
- Criar um espaço onde produtores compartilhem boas práticas, experiências e colaborem na produção.

### 8. Sugestões Personalizadas para Compradores
- Sugerir produtos com base nas preferências e histórico de compras do comprador, incluindo sazonalidade.

### 9. Blog e Conteúdo Educativo
- Área com artigos, receitas e dicas sobre alimentação saudável e produção orgânica.

### 10. Abertura de Vagas Temporárias
- Permitir que produtores publiquem vagas de trabalho sazonais diretamente na plataforma.

---

## Observações

- Os requisitos planejados têm como objetivo alinhar o crescimento da plataforma com os princípios de sustentabilidade, economia local e alimentação saudável.
- A modularidade do sistema permitirá que essas funcionalidades sejam implementadas em etapas, sem prejuízo ao que já está em operação.

