# 📋 Exemplo de Uso Prático

Este documento mostra como usar o projeto de análise do World Bank na prática.

## 1. Configuração Inicial

### Passo 1: Clone/Download do projeto
```bash
git clone <seu-repositorio> 
cd python-notes
```

### Passo 2: Configuração automática
```bash
# No macOS/Linux
bash setup.sh

# No Windows
powershell -ExecutionPolicy Bypass -File setup.ps1
```

## 2. Iniciando a Análise

### Passo 1: Ativar ambiente virtual
```bash
# macOS/Linux
source venv/bin/activate

# Windows
venv\Scripts\activate
```

### Passo 2: Iniciar Jupyter
```bash
jupyter notebook
```

### Passo 3: Abrir o notebook
1. No navegador, abra `world_bank.ipynb`
2. Selecione o kernel "World Bank Analysis"
3. Execute as células sequencialmente

## 3. Exemplos de Uso

### Análise Básica
```python
# Após executar todas as células, você pode:

# 1. Ver estatísticas resumidas
summary_statistics()

# 2. Criar perfil de um país específico
create_country_profile('Brasil')
create_country_profile('Estados Unidos')

# 3. Exportar dados para análise externa
export_data_to_csv()
```

### Análise Personalizada
```python
# Modificar lista de países
custom_countries = {
    'ARG': 'Argentina',
    'CHL': 'Chile',
    'COL': 'Colômbia',
    'PER': 'Peru',
    'URY': 'Uruguai'
}

# Executar análise customizada
custom_data = get_world_bank_data(
    list(custom_countries.keys()), 
    indicators, 
    start_year=2015, 
    end_year=2023
)
```

## 4. Interpretando os Resultados

### Gráficos Principais
1. **Box Plot PIB per capita**: Mostra diferenças entre grupos
2. **Correlação GINI vs PIB**: Revela padrões de desigualdade
3. **Análise PCA**: Identifica componentes principais
4. **Heatmap**: Correlações entre indicadores

### Estatísticas Importantes
- **Gap PIB**: Diferença absoluta entre grupos
- **Correlações**: Relações entre variáveis
- **Tendências**: Evolução temporal dos indicadores

## 5. Casos de Uso Específicos

### Pesquisa Acadêmica
```python
# Focar em indicadores específicos
education_indicators = [
    'SE.XPD.TOTL.GD.ZS',  # Gastos com educação
    'SE.ADT.LITR.ZS',     # Taxa de alfabetização
    'SE.TER.ENRR'         # Matrícula ensino superior
]

# Análise específica de educação
education_data = get_world_bank_data(
    list(all_countries.keys()), 
    education_indicators
)
```

### Análise de Política Pública
```python
# Comparar países similares
similar_countries = ['BRA', 'ARG', 'CHL', 'COL', 'PER']

# Focar em indicadores de desenvolvimento
development_indicators = [
    'NY.GDP.PCAP.CD',     # PIB per capita
    'FX.OWN.TOTL.ZS',     # Acesso financeiro
    'IT.NET.USER.ZS',     # Internet
    'SH.XPD.CHEX.PC.CD'   # Gastos saúde
]
```

### Análise de Mercado
```python
# Países emergentes
emerging_markets = ['BRA', 'IND', 'CHN', 'RUS', 'ZAF']

# Indicadores de investimento
investment_indicators = [
    'IC.CRD.PRVT.ZS',     # Crédito privado
    'FB.CBK.BRCH.P5',     # Agências bancárias
    'FS.AST.DOMS.GD.ZS'   # Ativos financeiros
]
```

## 6. Personalização Avançada

### Adicionar Novos Indicadores
```python
# Consultar indicadores disponíveis
wb.series.info()

# Adicionar novo indicador
new_indicators = {
    'SL.UEM.TOTL.ZS': 'Taxa de Desemprego (%)',
    'FP.CPI.TOTL.ZG': 'Inflação (%)',
    'BX.KLT.DINV.WD.GD.ZS': 'Investimento Estrangeiro (% PIB)'
}
```

### Modificar Visualizações
```python
# Customizar gráficos
plt.figure(figsize=(12, 8))
sns.scatterplot(data=analysis_df, x='PIB per capita (USD)', y='Índice GINI', 
                hue='Categoria', size='População Total')
plt.title('Relação PIB per capita vs Desigualdade')
plt.show()
```

## 7. Exportação e Compartilhamento

### Salvar Resultados
```python
# Exportar dados
export_data_to_csv()

# Salvar gráficos
plt.savefig('analise_disparidades.png', dpi=300, bbox_inches='tight')
```

### Relatório Automático
```python
# Gerar relatório para múltiplos países
countries_to_analyze = ['Brasil', 'Argentina', 'Chile', 'Colômbia']

for country in countries_to_analyze:
    print(f"\n{'='*50}")
    create_country_profile(country)
    print(f"{'='*50}")
```

## 8. Troubleshooting

### Problemas Comuns
1. **Kernel não encontrado**: Reinstale o kernel
2. **Dados não carregam**: Verifique conexão com internet
3. **Erro de dependência**: Reinstale requirements.txt
4. **Gráficos não aparecem**: Verifique versão do matplotlib

### Soluções
```bash
# Reinstalar kernel
python -m ipykernel install --user --name=world-bank-analysis --display-name="World Bank Analysis" --force

# Atualizar dependências
pip install -r requirements.txt --upgrade

# Verificar instalação
pip list | grep -E "(pandas|matplotlib|seaborn)"
```

## 9. Próximos Passos

### Expandir Análise
1. Adicionar mais países
2. Incluir indicadores setoriais
3. Análise temporal mais detalhada
4. Modelos preditivos

### Melhorar Visualizações
1. Gráficos interativos com Plotly
2. Dashboards com Streamlit
3. Mapas geográficos
4. Animações temporais

---

**Agora você está pronto para usar o projeto! 🚀** 