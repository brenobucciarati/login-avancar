# Sistema de Ordens de Serviço (OSM)

Este projeto é um sistema web para controle de Ordens de Serviço (OSM), com três interfaces principais:

- **Execução da OSM (`osm.html`)**
- **Reincidências (`reincidencias.html`)**
- **Componentes Substituídos (`componentes.html`)**

Cada página tem uma funcionalidade específica dentro do processo de manutenção.

---

## 📄 1. `osm.html` - Execução da OSM

### Objetivo:
Registrar e acompanhar a execução de uma Ordem de Serviço.

### Funcionalidades:
- Exibição dos dados da OSM (patrimônio, veículo, tipo, defeito).
- Seleção de demanda associada ao defeito.
- Inserção de até 7 tarefas com observações individuais.
- Campos para:
  - Informações adicionais (obrigatório)
  - Medidor horário
  - Número do lacre
- Botões de ação:
  - **Concluir OSM**: Salva e marca a OSM como finalizada.
  - **Salvar**: Armazena localmente o progresso da OSM.

### Armazenamento:
- Usa `localStorage` para manter os dados da OSM selecionada e tarefas.
- Ao concluir, remove a OSM atual do conjunto de OSMs em andamento.

---

## 🔁 2. `reincidencias.html` - Registro de Reincidências

### Objetivo:
Registrar se houve reincidência de problemas após a execução da OSM.

### Funcionalidades:
- Exibe os mesmos dados da OSM.
- Campo para descrever a reincidência detectada.
- Campos adicionais:
  - Responsável
  - Data
- Botão:
  - **Salvar**: Armazena os dados no `localStorage`.

### Observação:
- Ainda pode ser estendido para gerar relatórios de reincidência.

---

## ⚙️ 3. `componentes.html` - Componentes Substituídos

### Objetivo:
Registrar os componentes que foram trocados ou substituídos durante a OSM.

### Funcionalidades:
- Lista dinâmica de componentes substituídos.
- Campos por componente:
  - Nome do componente
  - Quantidade
  - Código ou número de série
- Botão:
  - **Adicionar Componente**: Adiciona novo item à lista.
  - **Salvar**: Armazena os dados no `localStorage`.

---

## 📁 Estrutura de Armazenamento

- `osSelecionada`: Objeto com dados da OSM em execução.
- `osmsConcluidas`: Lista de OSMs finalizadas.
- Outros dados como tarefas, reincidências e componentes podem ser armazenados em chaves específicas.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5**
- **CSS3**
- **JavaScript (ES6)**
- `localStorage` para persistência temporária

---

## 📌 Possíveis Melhorias Futuras

- Backend para persistência definitiva dos dados.
- Login/autenticação.
- Geração de relatórios em PDF.
- Dashboard para monitoramento das OSMs.

---

## 📧 Contato

Para dúvidas ou sugestões, entre em contato com o desenvolvedor do sistema.

