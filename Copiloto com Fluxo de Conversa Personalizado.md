### **Criando um Copiloto com Fluxo de Conversa Personalizado no Microsoft Copilot Studio**

O **Microsoft Copilot Studio** é uma plataforma poderosa para criar assistentes virtuais inteligentes e personalizados, capazes de interagir com os usuários de forma dinâmica e contextualizada. Neste artigo, vamos explorar como criar um **copiloto com fluxo de conversa personalizado**, desde a criação de um agente em branco até a customização de tópicos e mensagens de erro, além de ajustar a qualidade das respostas generativas usando **Inteligência Artificial Generativa (GenAI)**. O objetivo é fornecer um guia prático e detalhado para desenvolver copilotos eficientes e adaptados às necessidades do seu negócio.

---

### **Criando um Copiloto em Branco**

O primeiro passo para criar um copiloto personalizado é configurar um **agente em branco** no Microsoft Copilot Studio. Aqui está um guia passo a passo:

1. **Acessar o Microsoft Copilot Studio**:  
   - Entre ou inscreva-se no [Microsoft Copilot Studio](https://powerplatform.microsoft.com/).  
   - Na página inicial, selecione **Criar** na navegação à esquerda.

2. **Selecionar Novo Agente**:  
   - Na página **Criar**, selecione **Novo agente**. Isso abrirá o assistente de criação de agentes.

3. **Definir a Linguagem**:  
   - Escolha a linguagem que o agente usará para interagir com os usuários. Essa configuração é crucial para garantir que o copiloto se comunique de forma eficaz.

4. **Nome e Descrição**:  
   - **Nome**: Dê um nome descritivo ao seu agente, como "Tutor de Agente Amigável".  
   - **Descrição**: Escreva uma descrição clara sobre o propósito do agente. Por exemplo, "Ajuda os usuários a aprender a criar agentes no Microsoft Copilot Studio".

5. **Instruções**:  
   - Defina as instruções que orientam o comportamento do agente. Inclua detalhes sobre o estilo de conversa e os objetivos. Por exemplo, "Fale com os usuários como um professor gentil e paciente".

6. **Adicionar Conhecimento**:  
   - Configure as **fontes de conhecimento** que o agente usará, como URLs de sites públicos, documentos no SharePoint ou arquivos carregados no Dataverse.

7. **Configurações Avançadas**:  
   - **Solução**: Defina a solução onde o agente será implementado.  
   - **Nome do Esquema**: Especifique o nome do esquema para a base de dados do agente.

8. **Salvar e Testar**:  
   - Após configurar todas as opções, salve as configurações e teste o agente para garantir que ele está funcionando conforme esperado.

---

### **Customizando um Tópico**

Uma vez criado o agente, o próximo passo é **customizar tópicos** para definir como o copiloto responderá a perguntas específicas. Aqui está como fazer isso:

1. **Acessar a Página de Tópicos**:  
   - No Copilot Studio, vá para a página do seu agente e selecione a aba **Tópicos**.

2. **Adicionar um Novo Tópico**:  
   - Clique em **Adicionar um tópico** e selecione **Criar a partir da descrição com o Copilot**.  
   - Insira um nome e uma descrição clara para o tópico. Por exemplo, "Informações de Contato".

3. **Adicionar Frases de Gatilho**:  
   - No editor de tópicos, adicione frases que o usuário provavelmente usará para acionar o tópico. Por exemplo, "Quais são as informações de contato?".

4. **Adicionar Respostas Generativas**:  
   - No nó de resposta, selecione **Adicionar resposta generativa**.  
   - Configure as fontes de dados que o agente usará, como URLs de sites públicos ou documentos no SharePoint.

5. **Adicionar a Variável de Sistema `activity.text`**:  
   - Adicione um nó de ação para capturar o texto da atividade do usuário. Por exemplo:  
     ```
     activity.text = "Texto da atividade do usuário"
     ```

6. **Adicionar Mensagem de Finalização**:  
   - Inclua uma mensagem para encerrar a conversa. Por exemplo, "Obrigado por entrar em contato! Se precisar de mais alguma coisa, estou aqui para ajudar.".

7. **Testar o Tópico**:  
   - Use o painel **Testar seu agente** para simular conversas e verificar se o tópico está funcionando conforme esperado.

---

### **Personalizando uma Mensagem de Erro**

Para garantir uma experiência de usuário fluida, é importante **personalizar mensagens de erro** que orientem o usuário quando algo der errado. Aqui está como fazer isso:

1. **Acessar o Editor de Tópicos**:  
   - No Copilot Studio, vá para a página do seu agente e selecione a aba **Tópicos**.  
   - Escolha o tópico que deseja editar ou crie um novo.

2. **Adicionar Conversational Boosting**:  
   - Inclua mensagens que orientem o usuário a reformular a pergunta. Por exemplo, "Desculpe, não consegui entender. Você pode reformular?".

3. **Configurar Fallback**:  
   - Adicione um nó de fallback para lidar com situações em que o agente não consegue processar a solicitação. Por exemplo, "Vou transferir você para um agente humano.".

4. **Adicionar Mensagem de Erro Personalizada**:  
   - Configure uma mensagem de erro detalhada. Por exemplo, "Ocorreu um erro. Verifique as informações e tente novamente.".

5. **Testar o Tópico**:  
   - Simule conversas para garantir que as mensagens de erro estejam funcionando corretamente.

---

### **Ajustando a Qualidade das Respostas com GenAI**

A **Inteligência Artificial Generativa (GenAI)** permite ajustar a qualidade das respostas do copiloto. Aqui está como configurar:

1. **Acessar o Editor de Tópicos**:  
   - No Copilot Studio, vá para a página do seu agente e selecione a aba **Tópicos**.  
   - Escolha o tópico que deseja editar.

2. **Adicionar um Nó de Respostas Generativas**:  
   - No editor de tópicos, selecione **Adicionar resposta generativa**.

3. **Configurar Propriedades do Nó**:  
   - **Content**: Defina o conteúdo usado para gerar respostas.  
   - **ContentLocation**: Especifique a URL da fonte de conteúdo.  
   - **Title**: Adicione um título para a citação do conteúdo.

4. **Ajustar Instruções Personalizadas**:  
   - Adicione instruções para orientar o formato e o estilo das respostas. Por exemplo, "Responda de forma concisa e direta.".

5. **Configurar Fontes de Conhecimento**:  
   - Adicione URLs de sites ou documentos para garantir respostas precisas.

6. **Salvar Configurações**:  
   - Após ajustar as propriedades, salve as configurações e teste o agente.

---

### **Exemplo Prático: Agente de Suporte Técnico**

Imagine que você está criando um agente de suporte técnico. Aqui está um exemplo de como configurar:

1. **Tópico de Erro Personalizado**:  
   - **Conversational Boosting**: "Desculpe, não entendi. Reformule, por favor."  
   - **Fallback**: "Transferindo para um agente humano."  
   - **Mensagem de Erro**: "Ocorreu um erro. Verifique as informações e tente novamente."

2. **Respostas Generativas**:  
   - **Content**: "Solução para problemas comuns de conexão."  
   - **ContentLocation**: "https://suporte.com/conexao"  
   - **Title**: "Guia de Conexão"

---

### **Resumindo**

Criar um **copiloto com fluxo de conversa personalizado** no **Microsoft Copilot Studio** é um processo intuitivo e poderoso. Você pode desenvolver assistentes virtuais altamente adaptados às necessidades do seu negócio, oferecendo respostas precisas, contextualizadas e personalizadas. Seja para atendimento ao cliente, suporte técnico ou agendamentos, o Copilot Studio é a ferramenta ideal para transformar ideias em realidade.
