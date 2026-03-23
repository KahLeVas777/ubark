UBARK | Plataforma de Conhecimento e Inteligência Estratégica  Organize, Expanda e Transforme o Conhecimento em Vantagem Competitiva.Acessar Plataforma1. Visão GeralA UBARK é uma plataforma web robusta e centralizada, desenvolvida para a organização inteligente do conhecimento e a gestão eficiente de recursos digitais. Com foco em estrategistas e equipes de alta performance, a plataforma integra funcionalidades essenciais como um catálogo de produtos, uma biblioteca de arquivos com controle de acesso granular e um fórum comunitário dinâmico. Nosso objetivo é proporcionar um ambiente coeso e intuitivo para que usuários possam acessar, compartilhar e expandir seu capital intelectual de forma segura e eficaz.2. FuncionalidadesA plataforma UBARK oferece um conjunto abrangente de recursos para otimizar a gestão e o acesso ao conhecimento:
Autenticação Segura com Firebase: Sistema de login e registro robusto, garantindo a segurança dos dados do usuário e a integração com os serviços Google.
Gestão de Usuários e Perfis: Controle de acesso baseado em papéis (e.g., admin, user, e papéis personalizados como alfa e omega), permitindo a definição de permissões específicas para cada tipo de usuário.
Catálogo de Produtos Dinâmico: Uma seção dedicada à exibição e gestão de produtos, com detalhes, preços e controle de estoque, facilitando a organização de ofertas ou recursos.
Biblioteca de Arquivos com Níveis de Acesso: Armazenamento e organização de documentos, mídias e outros ativos digitais, com permissões de visualização e download configuráveis (e.g., VIP, General, Temp).
Fórum Comunitário Interativo: Um espaço para discussões, troca de ideias e colaboração entre os membros da comunidade, com funcionalidades de criação de posts, comentários e likes.
Base para Automações e IA: Arquitetura preparada para futuras integrações com inteligência artificial e automação de processos, visando otimizar a curadoria de conteúdo e a experiência do usuário.
3. TecnologiasO projeto UBARK é construído sobre uma stack tecnológica moderna e escalável, garantindo alta performance e manutenibilidade:
Frontend:

React: Biblioteca JavaScript para construção de interfaces de usuário reativas e componentizadas.
Vite: Ferramenta de build de nova geração, proporcionando um ambiente de desenvolvimento rápido e otimizações para produção.
TypeScript: Superset do JavaScript que adiciona tipagem estática, melhorando a robustez e a legibilidade do código.
Tailwind CSS: Framework CSS utilitário para estilização rápida e consistente da interface.
Lucide React: Biblioteca de ícones leves e personalizáveis para aprimorar a experiência visual.
Motion: Biblioteca de animação para React, adicionando fluidez e interatividade à interface.
Recharts: Biblioteca de gráficos para visualização de dados, ideal para dashboards e análises.


Backend e Banco de Dados:

Firebase: Plataforma de desenvolvimento de aplicativos do Google, oferecendo serviços de autenticação, banco de dados e armazenamento.
Firestore: Banco de dados NoSQL flexível e escalável do Firebase, utilizado para persistência de dados em tempo real.


Inteligência Artificial:

@google/genai: Integração com as APIs de IA generativa do Google, permitindo funcionalidades inteligentes na plataforma.


4. Estrutura de DadosA arquitetura de dados do UBARK é projetada para ser clara, eficiente e escalável, utilizando coleções no Firestore para organizar as informações:
User: Armazena perfis de usuário, incluindo informações de contato, papéis de acesso (admin, user, alfa, omega), status de bloqueio e metadados de criação/atualização.
Product: Contém os detalhes dos produtos disponíveis no catálogo, como nome, preço, descrição, categoria, estoque e URLs de imagem.
LibraryFile: Gerencia os metadados dos arquivos da biblioteca, incluindo ID, nome, tipo de acesso (VIP, General, Temp), URL de download, descrição, autor, categoria e nível de aprendizado.
ForumPost: Armazena as publicações do fórum, com título, conteúdo, autor, categoria, data de criação, contagem de likes e comentários, e status de moderação.
5. Coleções do FirestoreAs principais coleções do Firestore que estruturam o UBARK são:
/users/{uid}: Perfis de usuário e papéis de acesso.
/products/{productId}: Catálogo de itens disponíveis.
/library_files/{fileId}: Arquivos da biblioteca com controle de permissão.
/forum_posts/{postId}: Publicações e interações da comunidade.
6. Como Executar o ProjetoPara configurar e rodar o projeto UBARK localmente, siga os passos abaixo:
Instalar Dependências:
bash12345678910111213141516171819202122    npm install
    # ou yarn install
    # ou pnpm install
    

2.  **Configurar Variáveis de Ambiente**:
    Crie um arquivo `.env` na raiz do projeto com as credenciais do Firebase. **Não commite este arquivo para o controle de versão.**
```env
    VITE_FIREBASE_API_KEY="SUA_API_KEY_DO_FIREBASE"
    VITE_FIREBASE_AUTH_DOMAIN="SEU_AUTH_DOMAIN_DO_FIREBASE"
    VITE_FIREBASE_PROJECT_ID="SEU_PROJECT_ID_DO_FIREBASE"
    VITE_FIREBASE_STORAGE_BUCKET="SEU_STORAGE_BUCKET_DO_FIREBASE"
    VITE_FIREBASE_MESSAGING_SENDER_ID="SEU_MESSAGING_SENDER_ID_DO_FIREBASE"
    VITE_FIREBASE_APP_ID="SEU_APP_ID_DO_FIREBASE"
    VITE_FIREBASE_FIRESTORE_DATABASE_ID="SEU_FIRESTORE_DATABASE_ID_OPCIONAL"
    

3.  **Rodar o Projeto**:
```bash
    npm run dev
    # ou yarn dev
    # ou pnpm dev    npm install
    # ou yarn install
    # ou pnpm install
    

2.  **Configurar Variáveis de Ambiente**:
    Crie um arquivo `.env` na raiz do projeto com as credenciais do Firebase. **Não commite este arquivo para o controle de versão.**
```env
    VITE_FIREBASE_API_KEY="SUA_API_KEY_DO_FIREBASE"
    VITE_FIREBASE_AUTH_DOMAIN="SEU_AUTH_DOMAIN_DO_FIREBASE"
    VITE_FIREBASE_PROJECT_ID="SEU_PROJECT_ID_DO_FIREBASE"
    VITE_FIREBASE_STORAGE_BUCKET="SEU_STORAGE_BUCKET_DO_FIREBASE"
    VITE_FIREBASE_MESSAGING_SENDER_ID="SEU_MESSAGING_SENDER_ID_DO_FIREBASE"
    VITE_FIREBASE_APP_ID="SEU_APP_ID_DO_FIREBASE"
    VITE_FIREBASE_FIRESTORE_DATABASE_ID="SEU_FIRESTORE_DATABASE_ID_OPCIONAL"
    

3.  **Rodar o Projeto**:
```bash
    npm run dev
    # ou yarn dev
    # ou pnpm devO aplicativo estará disponível em `http://localhost:3000`.7. Variáveis de AmbienteAs variáveis de ambiente são essenciais para a configuração do Firebase e devem ser mantidas em sigilo. Utilize o prefixo VITE_ para que o Vite as exponha corretamente no ambiente do navegador.Exemplo de .env:envConfigurações do FirebaseVITE_FIREBASE_API_KEY="AIzaSyAggOqUP6afQpxG-US-Pt6wpZE15eJMk2c"
VITE_FIREBASE_AUTH_DOMAIN="ai-studio-applet-webapp-6d6f0.firebaseapp.com"
VITE_FIREBASE_PROJECT_ID="ai-studio-applet-webapp-6d6f0"
VITE_FIREBASE_STORAGE_BUCKET="ai-studio-applet-webapp-6d6f0.firebasestorage.app"
VITE_FIREBASE_MESSAGING_SENDER_ID="763332903057"
VITE_FIREBASE_APP_ID="1:763332903057:web:d197b84c5d591519673f30"
VITE_FIREBASE_FIRESTORE_DATABASE_ID="ai-studio-f74141c8-1cfd-48fc-8c10-23d3c48d3ff1"Outras variáveis de ambiente (se houver)VITE_ALGUMA_OUTRA_CHAVE="valor"
Atenção: Nunca commite seu arquivo .env diretamente para o controle de versão (Git). Adicione-o ao seu .gitignore para proteger suas credenciais.
8. Boas Práticas e ArquiteturaPara garantir a segurança, escalabilidade e manutenibilidade do projeto UBARK, algumas boas práticas arquiteturais são seguidas:
Controle de Acesso Granular: As regras de segurança do Firestore são configuradas para permitir acesso apenas aos dados e funcionalidades que cada usuário tem permissão, baseando-se em seus papéis e UID.
Padronização de Papéis (Roles): A definição clara de papéis (admin, user, alfa, omega) garante uma gestão de permissões consistente em toda a aplicação.
Timestamps para Auditoria: Campos como createdAt e updatedAt são utilizados em todas as entidades principais para rastreamento e auditoria de dados.
Separação de Responsabilidades: O código é organizado em módulos e componentes, promovendo a reutilização e facilitando a manutenção e o desenvolvimento de novas funcionalidades.
Validação de Dados no Frontend e Backend: A validação de dados é implementada tanto na interface do usuário quanto nas regras de segurança do Firestore, garantindo a integridade dos dados.
