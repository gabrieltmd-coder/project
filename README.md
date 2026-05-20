# Dashboard Financeiro - RUMO

## Descrição
Dashboard interativo para análise consolidada de contratos financeiros com identidade visual moderna em azul royal, inspirado no design Xperia.

## Arquivos

```
VSC - DASH/
├── index.html              # Dashboard interativo (abra no navegador)
├── dashboard_data.json     # Dados financeiros em JSON
├── layout xperia.avif      # Referência de design
└── README.md               # Este arquivo
```

## Como Usar

### Opção 1: Abrir no Navegador
1. Navegue até a pasta: `C:\Users\Admin\Desktop\VSC - DASH`
2. Clique 2x em `index.html`
3. O dashboard abrirá no seu navegador padrão

### Opção 2: Abrir com URL
- Copie o caminho completo do arquivo
- Cole na barra de endereço do navegador: `file:///C:/Users/Admin/Desktop/VSC%20-%20DASH/index.html`

## Funcionalidades

### Visão Macro
- 6 KPIs principais (cards com gradientes)
- Total de Contratos
- Total Planejado
- Total Realizado
- Total Forecast
- Taxa de Execução
- Desvio Total

**Gráficos:**
- Distribuição de Valores (Donut Chart)
- Análise Planejado x Realizado (Bar Chart Horizontal)
- Tabela resumida com percentuais

### Visão por Fornecedor
Análise detalhada de 7 fornecedores:
- AUSENCO
- BUILDERS
- GEODEEP
- GEOFORMA
- GERCON
- TMSA
- VR DEMOLIDORA

**Gráficos:**
- Total por Fornecedor (Bar Chart)
- Taxa de Execução (Bar Chart com cores: verde ≥40%, amarelo ≥20%, vermelho <20%)
- Planejado vs Realizado (Bar Chart comparativo)
- Desvio de Execução (Bar Chart com valores positivos/negativos)

**Tabela:**
- Detalhamento completo com 7 colunas
- Formatação de valores monetários
- Badges coloridas por taxa de execução

## Design

### Paleta de Cores
- **Primária:** Azul Royal (#4169E1)
- **Secundária:** Roxo (#8B7EFF)
- **Destaque:** Cyan (#00D9FF)
- **Fundo:** Gradiente roxo/azul escuro
- **Success:** Verde (#10B981)
- **Danger:** Vermelho (#EF4444)

### Características de Design
- Fundo gradiente com efeitos radiais animados
- Cards com blur effect (frosted glass)
- Borders com transparência
- Animações suaves (slideDown, slideUp, cardBounce, fadeIn)
- Tipografia moderna com gradientes
- Responsivo para mobile, tablet e desktop

## Dados

O arquivo `dashboard_data.json` contém:

### Análise Macro
```json
{
  "total_contratos": 371449722.61,
  "total_planejado": 26973040.84,
  "total_realizado": 10365133.64,
  "total_forecast": 18016039.56,
  "taxa_execucao": 38.43,
  "desvio_planejado": -16607907.20
}
```

### Dados por Fornecedor
- Total de Contratos
- Planejado
- Realizado
- Forecast
- Taxa de Execução (calculada)
- Desvio (calculado)

## Tecnologias

- **HTML5** - Estrutura
- **CSS3** - Styling com gradientes, animações e backdrop-filter
- **JavaScript** - Lógica interativa
- **Chart.js** - Gráficos dinâmicos
- **Fetch API** - Carregamento de dados JSON

## Navegadores Suportados

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Resolução de Problemas

### O dashboard está em branco
- Verifique se o arquivo `dashboard_data.json` está na mesma pasta que `index.html`
- Abra o console do navegador (F12) para ver mensagens de erro
- Verifique a conexão com a internet (para CDN do Chart.js)

### Os gráficos não aparecem
- Reload da página (F5)
- Limpe o cache do navegador
- Verifique se JavaScript está habilitado

### Dados não carregam
- Certifique-se que `dashboard_data.json` é um JSON válido
- Abra o arquivo JSON diretamente para verificar a formatação
- Verifique as permissões do arquivo

## Atualizar Dados

Para atualizar o dashboard com novos dados:

1. Atualize o arquivo `Base Consolidada Contratadas - v1.xlsx` no Desktop
2. Execute o script Python que extrai os dados
3. O novo `dashboard_data.json` será gerado automaticamente
4. Recarregue o dashboard no navegador

## Performance

O dashboard carrega em:
- **Primeira carga:** ~2-3 segundos
- **Mudança de abas:** Instantânea
- **Tamanho total:** ~38KB (HTML) + ~1.4KB (JSON) + Assets CDN

## Autor
Gerado automaticamente com análise de dados consolidados da RUMO

## Data de Atualização
07 de Maio de 2026
