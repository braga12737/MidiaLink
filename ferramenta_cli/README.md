
**🔧 Instalação Rápida**

📱 Termux (Android)

```bash
# 1. Atualizar e instalar Python
pkg update && pkg upgrade
pkg install python git

# 2. Clonar e entrar na pasta
git clone https://github.com/braga12737/medialink-uploadfiles.git
cd medialink-uploadfiles

# 3. Instalar dependências
pip install requests colorama
pip install python-whois dnspython

# 4. Executar
python main.py
```

💻 Windows

```bash
# 1. Instalar Python (se não tiver)
#    Baixe em: python.org/downloads
#    Marque "Add Python to PATH"

# 2. Abrir CMD como Administrador

# 3. Instalar dependências
pip install requests colorama python-whois dnspython

# 4. Baixar o código
#    Opção A: Baixar ZIP e extrair

# 5. Entrar na pasta e executar
cd medialink-uploadfiles
python main.py
```

🚀 Como Usar

Passo 1: Executar a Ferramenta

```bash
python main.py
```

Passo 2: Escolher Opção 1

```
[1] GERAR NOVO LINK E MONITORAR
```

· A ferramenta gera automaticamente 3 links:
  1. Link de rastreamento (envie para a pessoa)
  2. Link do painel web (monitore no navegador)
  3. Link da API (dados em JSON)

Passo 3: Compartilhar o Link

· Copie o primeiro link (aparece em amarelo)
· Envie para quem você quer rastrear

Passo 4: Monitorar em Tempo Real

· A ferramenta começa automaticamente a monitorar
· Quando alguém acessar o link, aparecerá:
  · IP completo da pessoa
  · Localização (cidade, país, coordenadas)
  · Provedor de internet (ISP)
  · Informações do dispositivo (navegador, sistema)
  · Detecção de VPN/Proxy
  · Análise de risco

📊 O que é Coletado

Informações Básicas

· Endereço IP completo
· Tipo (IPv4/IPv6)
· Data e hora do acesso
· ID único da visita

Localização

· Cidade, estado, país
· Coordenadas geográficas
· Fuso horário
· Provedor de internet (ISP)
· Número AS (Autonomous System)

Dispositivo

· Navegador utilizado
· Sistema operacional
· Tipo de dispositivo (Desktop/Mobile/Tablet)
· Resolução de tela
· Informações de GPU
· Número de núcleos da CPU
· Quantidade de memória RAM

Segurança

· Detecção de VPN/Proxy
· Detecção de Data Center
· Verificação de portas abertas
· Análise de risco automática

💾 Salvamento de Dados

A ferramenta salva automaticamente tudo em:

· logs_detalhados_ID_DATA.txt - Logs formatados em texto
· dados_completos_ID_DATA.json - Dados completos em JSON

⚡ Dicas Importantes

1. Só compartilhe o primeiro link (aparece em amarelo)
2. Use o segundo link para ver o painel no navegador
3. Os dados aparecem automaticamente no terminal
4. Pressione CTRL+C para voltar ao menu
5. Tudo é salvo automaticamente nos arquivos

❓ Problemas Comuns

Erro "Módulo não encontrado"

```bash
# Instalar manualmente as dependências
pip install requests colorama python-whois dnspython geoip2
```

Erro de Conexão

· Verifique sua internet
· Confira se o servidor está online
· Aguarde alguns segundos e tente novamente

Termux Travando

```bash
# Fechar e abrir novamente
exit
# Reabrir Termux
cd medialink-uploadfiles
python main.py
```

📞 Suporte
· GitHub Issues: Reportar problemas
---

Nota: Use esta ferramenta apenas para fins legítimos e educacionais. Respeite a privacidade alheia e as leis locais.
