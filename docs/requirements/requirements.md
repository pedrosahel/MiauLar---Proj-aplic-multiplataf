# 📋 Requisitos do Sistema

## ✅ Requisitos Funcionais (RF)
1. **Cadastro de usuários** (ONGs, protetores independentes e tutores).  
2. **Cadastro de gatos** disponíveis para adoção.  
4. **Painel de gestão para ONGs**, permitindo aprovar/rejeitar solicitações de adoção.  
5. **Notificação de usuários** sobre novos gatos cadastrados ou mudança de status.  

---

## ⚙️ Requisitos Não-Funcionais (RNF)
1. **Sistema responsivo**, acessível tanto em navegadores web quanto em dispositivos móveis.  
2. **Proteção de dados** através de criptografia.  
3. **Tempo de resposta rápido**, garantindo boa usabilidade.  

---

## 📏 Regras de Negócio
1. Todo gato **só poderá ser cadastrado** se houver registro de vacinação.  
2. Apenas **ONGs e protetores validados** podem cadastrar gatos no sistema.  

---

## 👥 Perfis de Usuários
- **Tutor (adotante):** usuário interessado em adotar gatos, pode criar conta, buscar animais, enviar solicitações e acompanhar status.  
- **Protetor Independente:** usuário autorizado a cadastrar gatos disponíveis, mas com número limitado de cadastros.  
- **ONG:** organização com acesso ao painel administrativo, podendo cadastrar animais, gerenciar solicitações e validar protetores.  
- **Administrador do Sistema:** responsável pela gestão geral, manutenção e configuração da plataforma.  

---

## 📚 Casos de Uso
1. **Cadastro de Usuário**  
   - Ator: Tutor, Protetor, ONG  
   - Fluxo principal: Usuário preenche formulário de cadastro → Sistema valida dados → Conta criada.  

2. **Cadastro de Gato**  
   - Ator: ONG ou Protetor validado  
   - Fluxo principal: Preencher dados do gato (nome, idade, vacinação, etc.) → Sistema valida informações → Animal fica disponível na plataforma.  

3. **Solicitação de Adoção**  
   - Ator: Tutor  
   - Fluxo principal: Tutor seleciona um gato → Envia solicitação → ONG recebe notificação → Aprova ou rejeita → Tutor é notificado da decisão.  
