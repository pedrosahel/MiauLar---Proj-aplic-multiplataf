# Endpoints previstos

- POST /auth/login - autenticação de usuários.  
- POST /usuarios - cadastro de novos usuários (tutor, ONG, administrador).  
- GET /usuarios/{id} - retorna informações de um usuário específico.  
- POST /gatos - cadastro de um novo gato (apenas ONG/protetor).  
- GET /gatos - lista todos os gatos disponíveis.  
- GET /gatos/{id} - retorna informações detalhadas de um gato.  
- POST /solicitacoes - cria uma nova solicitação de adoção (apenas tutores).  
- GET /solicitacoes/{id} - retorna os detalhes de uma solicitação.  
- PATCH /solicitacoes/{id} - atualiza o status da solicitação (ONG/admin).  
