# Análise de Disparidades Econômicas - World Bank Data

Este projeto realiza uma análise abrangente das disparidades de renda entre países desenvolvidos e em desenvolvimento utilizando dados do World Bank.

## Objetivos

- **Comparar indicadores econômicos** entre países de primeiro mundo e terceiro mundo
- **Analisar desigualdade de renda** através do Índice GINI
- **Examinar acesso a serviços financeiros** e sua correlação com desenvolvimento
- **Investigar o impacto de corporações financeiras** na situação econômica
- **Criar visualizações informativas** para demonstrar disparidades

## Indicadores Analisados

### Indicadores Principais
- **PIB per capita (USD)** - Renda média por habitante
- **Índice GINI** - Medida de desigualdade de renda
- **Taxa de Pobreza** - Porcentagem abaixo da linha de pobreza
- **Acesso a Conta Financeira** - Inclusão financeira
- **Infraestrutura Bancária** - Agências e ATMs per capita

### Indicadores Complementares
- Gastos com Saúde per capita
- Gastos com Educação (% PIB)
- Penetração de Internet
- Acesso à Eletricidade
- Emissões de CO2 per capita

## Países Analisados

### Países Desenvolvidos (10)
Estados Unidos, Alemanha, Japão, França, Reino Unido, Canadá, Austrália, Suécia, Suíça, Dinamarca

### Países em Desenvolvimento (10)
Brasil, Índia, Nigéria, Bangladesh, Paquistão, Etiópia, Madagascar, Haiti, Afeganistão, Mali

## Tecnologias Utilizadas

- **Python 3.7+**
- **wbgapi** - API oficial do World Bank
- **pandas** - Manipulação de dados
- **matplotlib & seaborn** - Visualizações
- **plotly** - Gráficos interativos
- **scikit-learn** - Análise multivariada
- **scipy** - Testes estatísticos

## Principais Análises

### 1. Disparidades de Renda
- Comparação de PIB per capita
- Análise de gaps econômicos
- Tendências temporais

### 2. Desigualdade Interna
- Análise do Índice GINI
- Correlação com renda nacional
- Padrões por região

### 3. Inclusão Financeira
- Acesso a serviços bancários
- Infraestrutura financeira
- Barreiras ao desenvolvimento

### 4. Análise Temporal
- Evolução dos indicadores (2010-2022)
- Convergência ou divergência
- Impacto de eventos globais

### 5. Correlações Multivariadas
- Análise de Componentes Principais (PCA)
- Matriz de correlações
- Fatores explicativos

## Como Executar

### Pré-requisitos
- Python 3.7+
- Jupyter Notebook ou JupyterLab
- Conexão com a internet

### Instalação

#### Opção 1: Configuração Automática (Recomendada)

**No macOS/Linux:**
```bash
# Execute o script de configuração
bash setup.sh
```

**No Windows:**
```powershell
# Execute o script PowerShell
powershell -ExecutionPolicy Bypass -File setup.ps1
```

#### Opção 2: Configuração Manual

##### 1. Criar e ativar ambiente virtual
```bash
# Criar ambiente virtual
python -m venv venv

# Ativar ambiente virtual
# No macOS/Linux:
source venv/bin/activate

# No Windows:
venv\Scripts\activate
```

##### 2. Instalar dependências
```bash
pip install -r requirements.txt
```

##### 3. Instalar kernel do Jupyter para o ambiente virtual
```bash
python -m ipykernel install --user --name=world-bank-analysis --display-name="World Bank Analysis"
```

### Execução

#### 1. Ativar o ambiente virtual (se não estiver ativo)
```bash
# No macOS/Linux:
source venv/bin/activate

# No Windows:
venv\Scripts\activate
```

#### 2. Iniciar Jupyter Notebook
```bash
jupyter notebook
```

#### 3. Executar o notebook
1. Abra o arquivo `world_bank.ipynb`
2. **Importante**: Certifique-se de que o kernel "World Bank Analysis" está selecionado (canto superior direito)
3. Execute as células sequencialmente (Shift + Enter)
4. A primeira célula instalará automaticamente as bibliotecas necessárias
5. Aguarde o carregamento dos dados do World Bank (pode demorar alguns minutos)

### Desativar ambiente virtual
```bash
deactivate
```

### Exportação
```python
# Exportar dados para CSV
export_data_to_csv()

# Criar perfil de país específico
create_country_profile('Brasil')

# Mostrar estatísticas resumidas
summary_statistics()
```

## Principais Descobertas

### Disparidades Extremas
- Países desenvolvidos têm PIB per capita **10-15x maior** que países em desenvolvimento
- O gap absoluto **continua crescendo** ao longo do tempo
- Concentração de riqueza nos países desenvolvidos

### Desigualdade Interna
- Países em desenvolvimento frequentemente têm **maior desigualdade interna**
- Correlação negativa entre PIB per capita e Índice GINI
- Grande heterogeneidade dentro dos grupos

### Exclusão Financeira
- Países pobres têm **muito menor acesso** a serviços financeiros
- Forte correlação entre desenvolvimento e inclusão financeira
- Infraestrutura bancária concentrada em países ricos

### Círculo Vicioso
- Falta de acesso financeiro perpetua o subdesenvolvimento
- Corporações financeiras concentram-se em mercados lucrativos
- Custos de serviços financeiros são maiores em países pobres

## Recomendações

### Para Países em Desenvolvimento
- Expandir inclusão financeira
- Investir em fintech e tecnologia
- Programas de educação financeira
- Melhorar ambiente regulatório

### Para Organismos Internacionais
- Facilitar transferência de tecnologia
- Aumentar financiamento concessionário
- Assistência técnica para reformas
- Monitoramento contínuo das disparidades

## Limitações

- eDisponibilidade limitada de dados para alguns países
- Heterogeneidade dentro dos grupos
- Correlações não implicam causalidade
- Foco em período específico (2010-2022)

## Próximos Passos

1. **Análise setorial** - Examinar setores específicos
2. **Estudos de caso** - Análises detalhadas por país
3. **Impacto de políticas** - Avaliar efetividade de intervenções
4. **Modelos preditivos** - Previsões de tendências futuras

## Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

## Contribuições

Contribuições são bem-vindas! Por favor, abra uma issue ou envie um pull request.

---

**Desenvolvido para análise de disparidades econômicas globais**
*Utilizando dados oficiais do World Bank*