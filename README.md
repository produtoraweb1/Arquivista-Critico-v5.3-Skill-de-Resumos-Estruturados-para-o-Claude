# 📚 Arquivista Crítico (v5.3) — Engenharia de Resumos Estruturados via Claude Projects

> **Sugestões de Títulos para o seu Repositório:**
> * `claude-project-arquivista-critico`
> * `knowledge-archivist-project`
> * `prompt-rag-resumo-critico`

## 🎯 Descrição do Projeto

O **Arquivista Crítico** é uma especificação técnica de engenharia de prompt desenhada para transformar a área de **Projetos (Projects)** do Claude (Anthropic) numa central automatizada de **Análise Crítica, Ancoragem Factual e Mapeamento Extensivo de Livros em PDF**.

Ao configurar esta Skill nas diretrizes estruturais do seu Claude Project, você elimina a necessidade de copiar e colar prompts manuais a cada conversa. Toda vez que iniciar um chat novo e anexar um livro dentro desse projeto, o Claude aplicará automaticamente um processo interno de auditoria (`<thinking>`) com ancoragem factual extrema. O sistema varre a totalidade do arquivo anexado para mapear de forma cirúrgica o perfil cognitivo do autor (idiossincrasias, tom, vieses) e extrair de 5 a 10 frameworks práticos mais importantes, sem resumir por brevidade. O resultado é um arquivo detalhado em Markdown (`.md`), blindado contra alucinações e otimizado para servir como uma **Base de Conhecimento Pessoal (Segunda Mente)** para consultas futuras de humanos ou de outras instâncias de IA, economizando milhares de tokens.

---

## 🧠 Benefícios Técnicos e Arquitetura Cognitiva

Ao utilizar o **Arquivista Crítico**, você cria um pipeline de dados otimizado para Large Language Models (LLMs):
* **Automação via Infraestrutura (No-Paste):** O prompt mestre fica fixado na memória raiz do projeto do Claude. Você só precisa arrastar e soltar o livro.
* **Máxima Extensão e Cobertura:** A versão v5.3 elimina vícios de parada e comandos de brevidade ("conciso", "denso"), forçando o Claude a varrer o miolo do livro e entregar respostas de longo fôlego.
* **Eficiência de Contexto (Token Saving):** Reduz um livro inteiro de ~400 páginas para uma estrutura altamente descritiva de 3 a 5 páginas. Isso diminui o consumo de tokens em mais de 90% nas consultas subsequentes.
* **Sandbox Baseado em Fatos:** Evita que o Claude misture o conteúdo do livro com alucinações geradas pelo senso comum da internet, restringindo a IA estritamente à lógica do autor.
* **Rastreabilidade Factual:** As exigências de citação por nome de capítulo ou seção previnem erros de OCR comuns no mapeamento de numeração de páginas rígidas.

---

## 📖 Instruções de Configuração e Uso (Workflow de Produção)

### Passo 1: Criar o Projeto no Claude
1. Acesse o Claude.ai (necessário plano Pro ou Team).
2. No menu lateral ou na página inicial, clique em **Projects** e selecione **Create Project**.
3. Escolha um nome para o seu projeto (ex: *Arquivista Crítico de Livros*).

### Passo 2: Definir as Instruções Coletivas (Instanciação da Skill)
1. Dentro do seu novo projeto, clique em **Set Custom Instructions** (Definir Instruções Personalizadas) no painel direito.
2. Copie e cole todo o conteúdo do arquivo `instrucoes.md` (versão v5.3-Production) deste repositório dentro da caixa de texto de instruções.
3. Clique em **Save**. Pronto! A inteligência de auditoria agora está congelada na raiz de todos os chats que você abrir aqui dentro.

### Passo 3: Geração Automatizada do Resumo
1. Com o projeto configurado, abra um novo chat **dentro dele**.
2. Faça o upload do arquivo PDF do livro.
3. Escreva o prompt de disparo para forçar o limite de resposta da IA:
   > *"Aplique a Skill do Arquivista Crítico neste livro. Faça uma análise exaustiva e de máxima extensão permitida pela sua janela de resposta, detalhando todos os pilares factuais do livro sem resumir ideias essenciais."*
4. O Claude processará a tag `<thinking>` em segundo plano e entregará a saída oficial rigorosamente estruturada.

### Passo 4: Armazenamento Estruturado (Segunda Mente)
Copie a saída gerada e salve localmente num arquivo de texto usando a extensão `.md` (Markdown). Adote o seguinte padrão de nome de arquivo para organização:
`sobrenome-autor_titulo-do-livro.md` (Exemplo: `kahneman_rapido-e-devagar.md`).

---

## 🚀 Exemplos Práticos de Uso para Consultas Avançadas

Depois de mapear seus livros técnicos, doutrinas ou manuais e alimentar o seu ecossistema, você poderá cruzar os dados ou aplicar os resumos gerados em cenários do seu dia a dia profissional. Veja estes seis exemplos de prompts avançados para usar no Claude:

### 🌟 Exemplo 1: Psicologia e Saúde Mental (Formulações Clínicas e Abordagens)
> **Contexto:** Você gerou o resumo crítico de um manual clássico sobre Terapia Cognitivo-Comportamental (TCC) ou um tratado de psicopatologia de referência.
>
> **Prompt para o Claude:**
> *"Claude, estou estruturando a formulação de caso de um paciente fictício que apresenta sintomas acentuados de ansiedade generalizada e padrões repetitivos de catastrofização. Estou anexando o **Resumo de Referência Futura** do livro de TCC que consolidamos no projeto. Com base estritamente nos frameworks de 'Identificação de Pensamentos Automáticos' e 'Questionamento Socrático' mapeados na Seção 3 e herdando as lentes metodológicas do autor detalhadas na Seção 2, crie uma estratégia de intervenção contendo 3 perguntas reflexivas para a próxima sessão. Não utilize abordagens fora do escopo deste resumo."*

### 🌟 Exemplo 2: Advocacia e Direito (Análise de Casos com base em Livros de Leis/Doutrinas)
> **Contexto:** Você gerou o resumo crítico de um livro de doutrina jurídica robusta ou comentários estruturados a códigos legais.
>
> **Prompt para o Claude:**
> *"Claude, estou analisando um caso complexo de quebra de contrato comercial devido a um evento de força maior imprevisto. Anexei aqui o **Resumo de Referência Futura** do livro de Doutrina de Direito Civil sobre Responsabilidade Contratual que mapeamos anteriormente. Utilizando exclusivamente a interpretação do autor sobre o nexo de causalidade e as excludentes de responsabilidade civil documentadas na Seção 3, faça um parecer preliminar apontando os pontos fortes e os pontos fracos do argumento da nossa defesa. Cite os termos originais e jargões do autor mapeados na Seção 4 (Glossário)."*

### 🌟 Exemplo 3: Engenharia de Produto, Inovação e Growth (Cenário Técnico)
> **Contexto:** Você gerou o resumo crítico do livro *"O Dilema da Inovação"* de Clayton Christensen.
>
> **Prompt para o Claude:**
> *"Claude, atuamos no mercado de SaaS para logística e um concorrente menor começou a oferecer uma ferramenta gratuita, simplificada, mas muito veloz, ameaçando nossa base de clientes de entrada. Anexei aqui o **Resumo de Referência Futura** do livro 'O Dilema da Inovação' (Clayton Christensen). Utilizando exclusivamente o concept de 'Inovação Disruptiva vs. Sustentável' e as limitações de mercado documentadas nas seções 3 e 5 deste resumo, faça um diagnóstico do nosso cenário estratégico e sugira duas linhas de defesa que a nossa engenharia de produto pode adotar."*

### 🌟 Exemplo 4: Estratégia de Negócios e Finanças (Valuation e Análise Competitiva)
> **Contexto:** Você mapeou um livro avançado sobre Value Investing ou Análise de Demonstrações Financeiras.
>
> **Prompt para o Claude:**
> *"Claude, estamos avaliando a tese de investimento de uma empresa do setor de varejo que possui margens operacionais historicamente espremidas, mas apresenta alto giro de estoques. Estou anexando o **Resumo de Referência Futura** da obra clássica sobre Valuation que extraímos. Utilizando as premissas e métricas de eficiência descritas nas Seções 3 e 4, avalie se esse modelo de negócios é considerado resiliente segundo a ótica estrita do autor. Aponte também os riscos de fragilidade contábil que ele alerta na Seção 5 (Lacunas/Limitações)."*

### 🌟 Exemplo 5: Liderança, Cultura e Gestão de Pessoas (Diagnóstico Organizacional)
> **Contexto:** Você consolidou o resumo de um livro sobre Alta Performance, Gestão de Cultura ou Segurança Psicológica nas Empresas.
>
> **Prompt para o Claude:**
> *"Claude, nossa equipe de engenharia de software apresentou uma queda abrupta no volume de deploys e os líderes estão apontando medo de punições por falhas em produção como a causa principal. Anexei o **Resumo de Referência Futura** sobre Segurança Psicológica Corporativa. Extraia a definição exata de 'Clima de Confiança' e os 'Mecanismos de Resposta a Erros' da Seção 3 e estruture um roteiro rápido de 4 passos para o Diretor de Tecnologia aplicar na próxima reunião, neutralizando a ansiedade operacional de acordo com as premissas estruturais do autor."*

### 🌟 Exemplo 6: Marketing Digital e Persuasão (Copywriting e Funis de Conversão)
> **Contexto:** Você gerou o resumo analítico de um livro de psicologia da persuasão, neuromarketing ou copy.
>
> **Prompt para o Claude:**
> *"Claude, preciso desenhar a página de vendas de um novo infoproduto voltado para gestão de tempo para executivos seniores. Anexei o **Resumo de Referência Futura** do livro sobre Gatilhos Mentais e Comportamento Humano. Varra a Seção 3 (Arquitetura do Pensamento) e selecione os 3 frameworks de influência mais indicados para o público B-Level. Em seguida, utilize o Glossário da Seção 4 para escrever duas variações de chamadas (H1) que utilizem rigorosamente a ressignificação conceitual proposta pelo autor para capturar a atenção imediata."*

---

## 🤝 Apoio ao projeto

Se esta ferramenta ajudou você, é possível apoiar voluntariamente a manutenção e evolução do projeto.

```txt
Pix: doacoes@produtoraweb.com
Cripto: 0xEd46dADa43cb7b4e4D753D631B4E99002530D780
```

---

## 🛡️ Aviso legal

Use com responsabilidade, revise os prompts antes de enviar e valide alterações importantes antes de publicar qualquer projeto.

---

## 📄 Licença

Este projeto é distribuído sob a licença **GNU General Public License v3.0 (GPL-3.0)**.

Você pode usar, estudar, modificar e redistribuir este projeto, desde que qualquer versão modificada ou redistribuída também mantenha o código aberto sob os termos da GPL-3.0.

Consulte o arquivo `LICENSE` para mais detalhes.

---
Desenvolvido por ProdutoraWeb.com para revolucionar estratégias de busca orgânica e visibilidade digital. 🚀
