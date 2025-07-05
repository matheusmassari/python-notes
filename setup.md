# 🛠️ Guia de Configuração do Ambiente Virtual

Este guia te ajudará a configurar um ambiente virtual Python específico para o projeto de análise do World Bank.

## Por que usar um ambiente virtual?

- **Isolamento**: Evita conflitos entre diferentes projetos
- **Reprodutibilidade**: Garante que todos usem as mesmas versões das bibliotecas
- **Organização**: Mantém suas dependências organizadas
- **Segurança**: Não altera as bibliotecas do sistema

## Passo a Passo

### 1. Navegue até o diretório do projeto
```bash
cd /caminho/para/seu/projeto/python-notes
```

### 2. Crie o ambiente virtual
```bash
# Criar ambiente virtual chamado 'venv'
python -m venv venv

# Ou use python3 se necessário
python3 -m venv venv
```

### 3. Ative o ambiente virtual

#### No macOS/Linux:
```bash
source venv/bin/activate
```

#### No Windows:
```bash
venv\Scripts\activate
```

### 4. Confirme que o ambiente está ativo
Quando ativo, você verá `(venv)` no início da linha de comando:
```bash
(venv) ~/python-notes $ 
```

### 5. Instale as dependências
```bash
pip install -r requirements.txt
```

### 6. Instale o kernel do Jupyter para este ambiente
```bash
python -m ipykernel install --user --name=world-bank-analysis --display-name="World Bank Analysis"
```

### 7. Inicie o Jupyter Notebook
```bash
jupyter notebook
```

### 8. Configure o kernel no notebook
1. Abra o arquivo `world_bank.ipynb`
2. Clique em "Kernel" → "Change kernel"
3. Selecione "World Bank Analysis"
4. Agora você pode executar as células!

## Comandos Úteis

### Verificar pacotes instalados
```bash
pip list
```

### Atualizar requirements.txt (se adicionar novos pacotes)
```bash
pip freeze > requirements.txt
```

### Desativar o ambiente virtual
```bash
deactivate
```

### Remover o kernel do Jupyter (se necessário)
```bash
jupyter kernelspec remove world-bank-analysis
```

## Troubleshooting

### Erro: "python não encontrado"
Use `python3` em vez de `python`:
```bash
python3 -m venv venv
```

### Erro: "jupyter não encontrado"
Certifique-se de que o ambiente virtual está ativo e execute:
```bash
pip install jupyter notebook
```

### Erro: "kernel não aparece no Jupyter"
Reinstale o kernel:
```bash
python -m ipykernel install --user --name=world-bank-analysis --display-name="World Bank Analysis" --force
```

### Erro: "ModuleNotFoundError" no notebook
1. Confirme que o kernel correto está selecionado
2. Reinstale as dependências:
```bash
pip install -r requirements.txt
```

## Estrutura do Projeto

```
python-notes/
├── venv/                   # Ambiente virtual (criado por você)
├── world_bank.ipynb        # Notebook principal
├── requirements.txt        # Dependências
├── README.md              # Documentação
├── setup.md               # Este guia
└── .gitignore             # Arquivos ignorados pelo Git
```

## Dicas Importantes

1. **Sempre ative o ambiente virtual** antes de trabalhar no projeto
2. **Use o kernel correto** no Jupyter (World Bank Analysis)
3. **Não commite a pasta venv** no Git (já está no .gitignore)
4. **Mantenha o requirements.txt atualizado** se adicionar novos pacotes

---

**Pronto! Agora você tem um ambiente virtual isolado para o projeto! 🎉** 