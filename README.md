## MidiaLink - IP Logger Avançado

📡 Sobre o Projeto

MidiaLink é uma solução composta por uma API Node.js poderosa e um cliente Python avançado para monitoramento em tempo real. A ferramenta permite gerar links de rastreamento e coletar informações detalhadas sobre quem os acessa.

🏗️ Arquitetura do Sistema

API (Backend - Node.js)

· Tecnologia: Express.js + Axios
· Hospedagem: Vercel (https://medialink-uploads.vercel.app)
· Funcionalidades:
  · Geração de links únicos de rastreamento
  · Coleta automática de dados de IP
  · Geolocalização com múltiplas fontes
  · Análise de User-Agent
  · Coleta de hardware via WebGL
  · Painel web em tempo real

Cliente (Frontend - Python)

· Tecnologia: Python + Requests + Colorama
· Funcionalidades:
  · Interface CLI colorida e intuitiva
  · Monitoramento em tempo real
  · Coleta avançada de informações de rede
  · Análise de segurança automática
  · Salvamento de logs em múltiplos formatos

🔧 Funcionalidades Técnicas

Coleta de Dados (API)

· IP Detection: Suporte a IPv4/IPv6 com múltiplos headers
· Geolocation: Integração com ip-api.com e ipinfo.io
· DNS Reverse Lookup: Resolução de nomes de domínio
· User-Agent Analysis: Detecção de navegador, SO e dispositivo
· Hardware Fingerprinting: Coleta via WebGL e Navigator API

Monitoramento (Cliente Python)

· Port Scanning: Verificação de portas abertas
· WHOIS Lookup: Informações de registro de IP
· DNS Analysis: Resolução completa de DNS
· Risk Assessment: Análise automática de risco
· Real-time Updates: Atualização automática a cada 3 segundos

📊 Dados Coletados

Informações de Rede

· Endereço IP completo
· Localização geográfica (cidade, país, coordenadas)
· Provedor de internet (ISP)
· Tipo de conexão (IPv4/IPv6)
· DNS reverso
· Informações AS (Autonomous System)

Informações do Cliente

· Navegador e versão
· Sistema operacional
· Tipo de dispositivo (Desktop/Mobile/Tablet)
· Resolução de tela
· Informações de GPU via WebGL
· Hardware (núcleos CPU, memória RAM)
· Fuso horário e idioma

Detecções de Segurança

· Proxy/VPN detection
· Data center/hosting detection
· Conexão móvel detection
· Análise de risco automática

🚀 Como Funciona

1. Geração de Link: A API gera um link único com ID específico
2. Coleta de Dados: Quando acessado, coleta automaticamente todas as informações
3. Monitoramento: O cliente Python se conecta à API e exibe dados em tempo real
4. Persistência: Dados são salvos em arquivos TXT e JSON para análise posterior

🔒 Segurança e Privacidade

· Links temporários: Expiração automática após 7 dias
· Senha de administração: Proteção para endpoints sensíveis
· Validação de IP: Filtragem de IPs locais e inválidos
· Coleta ética: Apenas dados disponíveis publicamente

💻 Tecnologias Utilizadas

Backend

· Node.js 18+
· Express.js
· Axios para requisições HTTP
· DNS promises para resolução
· CORS para segurança

Cliente

· Python 3.7+
· Requests para HTTP
· Colorama para interface
· dnspython para DNS
· python-whois para WHOIS
· geoip2 para geolocalização local

📁 Estrutura de Arquivos

```
midialink/
├── /
│   └── index.js          # Código da API Node.js
├── ferramenta_cli/
│   └── main.py  # Cliente Python
└── README.md           # Tutorial
```

🌐 API Endpoints

```
GET  /gerar/:senha         # Gerar novo link
GET  /file/:id            # Página de rastreamento
GET  /painel/:id          # Painel web
GET  /api/status/:id      # Status do endpoint
GET  /api/dados/:id/:senha # Dados completos
POST /api/coleta-extra/:id/:visitanteId # Hardware data
```

🔄 Fluxo de Dados

```
Usuário → Link Gerado → API MidiaLink → Coleta Dados → Banco em Memória
                                                          ↓
Cliente Python ←─ API Status ←─── Monitoramento ←─── Dados Disponíveis
```

⚡ Características Únicas

1. Multi-fonte Geolocation: Combina dados de ip-api.com e ipinfo.io
2. Hardware Fingerprinting: Detecção avançada via WebGL
3. Real-time Monitoring: Atualização automática a cada 3 segundos
4. Risk Analysis: Pontuação automática de risco baseada em múltiplos fatores
5. Cross-platform: Funciona em Windows, Linux e Termux (Android)

🎯 Casos de Uso

· Pentesting: Testes de segurança e reconhecimento
· Network Monitoring: Monitoramento de acessos
· Geolocation Testing: Verificação de localização por IP
· Educational: Estudo de técnicas de coleta de dados
· Security Analysis: Detecção de proxies e VPNs

📝 Licença e Uso

O código é aberto e público, disponível para quem quiser utilizar, modificar ou hospedar em sua própria infraestrutura.

Aviso Legal: Esta ferramenta deve ser usada apenas para fins legítimos, educacionais ou de segurança autorizada. Respeite a privacidade alheia e as leis locais.

🔗 Links

· API Ativa: https://medialink-uploads.vercel.app
· Repositório: GitHub - MidiaLink
MidiaLink - Ferramenta profissional para coleta e monitoramento de informações de rede em tempo real.
