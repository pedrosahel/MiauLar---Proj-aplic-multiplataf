# 🐾 Arquitetura do Sistema

# Escopo do Projeto

 A ideia é o desenvolvimento de um sistema voltado para facilitar a adoção responsável de gatos e reduzir o abandono desses animais em áreas urbanas. O sistema permitirá o cadastro de usuários, diferenciando tutores e organizações de proteção animal.
  
  A plataforma oferecerá recursos de busca para facilitar a localização de animais, além de possibilitar a solicitação de adoção por parte dos interessados. As solicitações serão gerenciadas pelas organizações, que poderão aprová-las ou rejeitá-las, com atualização automática do status de cada animal.
    
  Estão fora do escopo desta primeira versão funcionalidades avançadas, como integração com sistemas de pagamento, acompanhamento pós-adoção e recursos de busca e filtragem.
 

### Funcionalidades contempladas
- Cadastro de usuários, com diferenciação entre **tutores**, **organizações de proteção animal** e **protetores independentes**.  
- Cadastro de gatos disponíveis para adoção.  
- Possibilidade de **solicitação de adoção** por parte dos tutores interessados.  
- **Gestão de solicitações** pelas organizações (aprovação ou rejeição).  

### Fora do escopo (versão inicial)
- Integração com sistemas de pagamento.  
- Recursos de **busca e filtragem** de animais.  
- Acompanhamento pós-adoção.  
- Design gráfico avançado.  


## 🖥️ Arquitetura do Sistema
A arquitetura proposta segue o padrão **Cliente-Servidor** dividido em três camadas principais:

### 1. Frontend
- Web: Desenvolvida com **HTML, CSS, JavaScript e Bootstrap**, garantindo leveza, responsividade e baixo nível de complexidade.  
- Mobile: Implementada como PWA, possibilitando que o site responsivo seja utilizado também em dispositivos móveis, sem necessidade de app nativo.  

### 2. Backend
- Construída em PHP com o framework CodeIgniter 4, responsável por:  
  - Gerenciar autenticação e perfis de usuário (ONGs, tutores).  
  - Processar solicitações de adoção.  
  - Controlar o fluxo de aprovação/rejeição.  
  - Atualizar o status dos animais no banco de dados.  
- Implementação de **APIs REST**, que conectam o frontend ao backend.  

### 3. Banco de dados
- Banco de dados relacional MySQL, responsável por armazenar:  
  - Informações de usuários.  
  - Perfis de ONGs e tutores.  
  - Cadastro de gatos disponíveis.  
  - Solicitações de adoção e seus status.  

### Componentes do Sistema
- Autenticação e autorização de usuários.  
- Cadastro e gerenciamento de usuários (ONGs, protetores e tutores).  
- Cadastro e gerenciamento de gatos disponíveis para adoção.  
- Painel administrativo para controle de solicitações e status dos animais.  

### Decisões Técnicas
1. Frontend Web com Bootstrap  
   - Escolhido pela **leveza**, baixo nível de complexidade e urva de aprendizado reduzida.  
   - Oferece componentes prontos e responsivos, facilitando a criação de telas de cadastro, listagens e formulários.  
   - Permite que o desenvolvimento se concentre mais na lógica do sistema do que no design visual.  

2. PWAs para Mobile  
   - Optou-se por PWA pela facilidade de portar um site responsivo para dispositivos móveis.  
   - Evita custos e complexidade do desenvolvimento de apps nativos.  
   - Garante instalação no celular, acesso offline básico e notificações push no futuro.  

3. Backend em PHP CodeIgniter 4 
   - PHP foi escolhido por sua ampla documentação, baixo custo de hospedagem e familiaridade da equipe.  
   - O framework CodeIgniter 4 traz organização em MVC, facilitando manutenção e escalabilidade.  
   - Suporte integrado a rotas, middlewares e APIs REST simplifica a comunicação entre frontend e backend.  

4. Banco de Dados MySQL 
   - Selecionado pela consistência, estabilidade e amplo suporte em comunidades.  
   - A equipe já possui conhecimento prévio em sua modelagem e utilização.  
   - Permite fácil integração com o CodeIgniter e suporte a consultas relacionais para gerenciar usuários, animais e adoções.  

5. APIs REST 
   - Definidas como padrão de comunicação entre frontend e backend.  
   - Facilitam integração futura com outros sistemas como abrigos parceiros, plataformas governamentais.  
   - Seguem boas práticas de modularidade e desacoplamento.  

6. Controle de Versão
   - Utilização do GitHub para versionamento, colaboração em equipe.  
   - Permite registro histórico do projeto e facilita revisões de código.  

## Fluxo Simplificado
1. Usuário acessa a plataforma.  
2. Faz login ou cria cadastro.  
3. ONG cadastra gatos disponíveis.  
4. Tutor busca animais e envia uma solicitação de adoção.  
5. ONG recebe e analisa a solicitação.  
6. Sistema atualiza automaticamente o status do animal.  

## Tecnologias Propostas
- Frontend Web: HTML, CSS, JavaScript, Bootstrap  
- Frontend Mobile: PWA 
- Backend: PHP 
- Banco de Dados: MySQL  
- APIs: REST  
- Controle de Versão: Git/GitHub  

