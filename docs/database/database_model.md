# 📐 Modelagem do Sistema

## 🧩 Descrição das Entidades
- **Usuário:** representa pessoas físicas, protetores/ONGs e administradores.  
- **Gato:** representa os animais cadastrados para adoção.  
- **Solicitação de adoção:** representa o pedido de um tutor para adotar um gato.  

---

## 🔗 Descrição dos Relacionamentos
- Um **usuário protetor/ONG** pode cadastrar vários gatos (**1:N**).  
- Um **tutor** pode enviar várias solicitações de adoção (**1:N**).  
- Cada **solicitação** está vinculada a um único gato e a um único tutor (**N:1**).  

---

## 📊 Diagrama ER (Mermaid)

erDiagram
   
    USUARIO {
        int id PK
        string nome
        string email
        string senha
        string tipo
    }

    GATO {
        int id PK
        string nome
        string sexo
        int idade
        string descricao
        string status
        int id_protetor FK
    }

    SOLICITACAO {
        int id PK
        int id_adotante FK
        int id_gato FK
        string status
    }
    
    USUARIO ||--o{ GATO : "cadastra"
    USUARIO ||--o{ SOLICITACAO : "envia"
    GATO ||--o{ SOLICITACAO : "recebe"


# 📖 Dicionário de Dados  

## 🧑‍💻 Tabela USUARIO  
- **id (PK):** identificador único do usuário.  
- **nome:** nome completo.  
- **email:** endereço de e-mail (único).  
- **senha:** senha criptografada.  
- **tipo:** define se o usuário é **tutor**, **protetor/ONG** ou **administrador**.  

## 🐱 Tabela GATO  
- **id (PK):** identificador único do gato.  
- **nome:** nome do animal.  
- **sexo:** macho ou fêmea.  
- **idade:** idade estimada em anos.  
- **descricao:** breve histórico ou observações.  
- **status:** disponível, em processo ou adotado.  
- **id_protetor (FK):** referência ao usuário **protetor/ONG** que cadastrou o gato.  

## 📩 Tabela SOLICITACAO  
- **id (PK):** identificador único da solicitação.  
- **id_adotante (FK):** referência ao usuário **tutor** que solicita a adoção.  
- **id_gato (FK):** referência ao gato desejado.  
- **status:** pendente, aprovado ou rejeitado.  
