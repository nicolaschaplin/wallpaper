<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NCR_7 // Terminal Portfolio</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;700&display=swap');

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        /* Fundo simulando um data center escurecido/desfocado */
        /* Fundo com a imagem na cor normal original */
        body {
            background-color: #050505;
            background-image: url('https://images.unsplash.com/photo-1558494949-ef010cbdcc31?q=80&w=2000&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: #d3d3d3; /* Cinza claro para texto padrão */
            font-family: 'Fira Code', monospace;
            padding: 40px 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        /* A janela do terminal */
        .terminal-window {
            background-color: rgba(15, 15, 15, 0.95);
            width: 100%;
            max-width: 1100px;
            border-radius: 10px;
            border: 1px solid #333;
            box-shadow: 0 20px 50px rgba(0,0,0,0.8);
            overflow: hidden;
            backdrop-filter: blur(5px);
        }

        /* Conteúdo interno do terminal */
        .terminal-content {
            padding: 30px;
            font-size: 15px;
            line-height: 1.5;
        }

        /* Cores Base */
        .green { color: #50fa7b; } /* Verde neon */
        .cyan { color: #8be9fd; } /* Ciano para links/destaques */
        .white { color: #f8f8f2; }
        .comment { color: #6272a4; } /* Cinza azulado para menus/comentários */
        
        .bold { font-weight: bold; }

        /* Estrutura do Header e Menu */
        .top-bar {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 20px;
            flex-wrap: wrap;
            gap: 15px;
        }

        .logo-area {
            font-size: 24px;
        }

        .menu-area {
            color: #8be9fd;
            font-size: 14px;
        }

        .subtitle {
            color: #50fa7b;
            margin-bottom: 30px;
            border-bottom: 1px dashed #333;
            padding-bottom: 15px;
        }

        /* Sessões de Comandos */
        .command-block {
            margin-bottom: 25px;
        }

        .prompt { color: #f8f8f2; }
        .cmd-text { color: #8be9fd; }

        /* Output do systemctl */
        .sys-status {
            margin-left: 15px;
        }
        
        .sys-status .dot {
            color: #50fa7b;
            font-size: 20px;
            line-height: 0;
            vertical-align: middle;
        }

        .sys-content {
            margin-left: 20px;
            color: #d3d3d3;
            white-space: pre-wrap;
        }

        /* Output das Habilidades */
        .skills-list {
            margin-left: 20px;
            list-style-type: none;
        }

        .skills-list li {
            margin-bottom: 5px;
        }

        /* Footer / Status Bar */
        .status-bar {
            border-top: 1px solid #333;
            padding-top: 15px;
            margin-top: 30px;
            display: flex;
            justify-content: space-between;
            color: #f8f8f2;
            font-size: 14px;
        }

        /* Cursor */
        .cursor {
            display: inline-block;
            width: 10px;
            height: 20px;
            background-color: #50fa7b;
            vertical-align: middle;
            animation: blink 1s step-end infinite;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

        @media (max-width: 768px) {
            .terminal-content { padding: 15px; font-size: 13px; }
            .top-bar { flex-direction: column; }
        }
        /* Container para alinhar o boneco e a lista lado a lado */
        .skills-container {
            display: flex;
            align-items: center; /* Alinha pelo centro verticalmente */
            gap: 30px; /* Espaço entre o boneco e a lista */
            margin-top: 15px;
        }
        
        .ascii-boneco {
            color: #00FF00; /* Verde para destacar do texto verde */
            font-weight: bold;
            line-height: 1.2;
            white-space: pre; /* Garante que o desenho ASCII não quebre */
        }

        /* Ajuste para o celular: coloca o boneco em cima da lista em telas pequenas */
        @media (max-width: 768px) {
            .skills-container {
                flex-direction: column;
                align-items: flex-start;
                gap: 15px;
            }
        }
    </style>
</head>
<body>

<div class="terminal-window">
    <div class="terminal-content">
        <pre class="ascii-logo">
            <span class="green bold">
 _   _  _____  ______ ______ 
| \ | |/  __ \| ___ \___  / 
|  \| || /  \/| |_/ /  / /  
| . ` || |    |    /  / /   
| |\  || \__/\| |\ \ / /    
\_| \_/ \____/\_| \_|\_/      
            </span>                         
</pre></span>
        <!-- Header & Menu -->
        <div class="subtitle">
            NCR7 | Infraestrutura de Rede e Segurança Cibernética | [ Conectividade Total ]
        </div>

        <!-- Comando 1: systemctl status -->
        <div class="command-block">
            <div><span class="prompt">root@ncr7:~# </span><span class="cmd-text">systemctl status ncr7-stack</span></div>
            <div class="sys-status">
                <span class="dot">•</span> <span class="white">ncr7-stack.service - Nicolas Chaplin Rodrigues Profile</span><br>
                <div class="sys-content">Loaded: loaded (/etc/systemd/system/ncr7-stack.service; enabled)
Active: <span class="green">active (running)</span> since Mon 2026-06-12 08:00:00 UTC
Main PID: 1999 (ncr7-core)

<span class="white">Profile:</span> Profissional de Infraestrutura de TI e Redes, formado em Gestão da Tecnologia da Informação, com experiência no 1º Ofício de Registro de Imóveis de Florianópolis. Minha atuação abrange suporte técnico, administração de servidores, configuração de firewalls e equipamentos de rede, além do monitoramento de sistemas e gestão de rotinas de backup alinhadas à LGPD.

<span class="white">Focus:</span> Com forte foco em segurança e modernização de ambientes corporativos, dedico meus estudos atuais ao aprofundamento em Microsoft 365, Entra ID e Intune para a gestão de identidades e endpoints. Complemento essa especialização com estudos contínuos em Cybersecurity e mitigação de riscos.</div>
            </div>
        </div>

        <!-- Comando 2: habilidades_view.sh -->
        <div class="command-block">
            <div><span class="prompt">root@ncr7:~# </span><span class="cmd-text">./habilidades_view.sh --verbose</span></div>
            <div class="green">[OK] Carregando Habilidades Técnicas da NCR7...</div>
            
            <div class="skills-container">
                <!-- O Bonequinho ASCII -->
                <div class="ascii-boneco">
   .---.
  /     \
  \     /
   `---'
  /|   |\
 / |   | \
   |===|
   |   |
   |   |
                </div>
                
                <!-- A Lista de Habilidades -->
                <ul class="skills-list">
                    <li><span class="white">1. ECOSSISTEMA MICROSOFT & IDENTIDADE:</span>
  - Microsoft 365, Microsoft Entra, Microsoft Intune, Active Directory</li>
                    <li><span class="white">2. INFRAESTRUTURA, REDES & HARDWARE:</span>
  - Arquitetura de Rede, LAN, Cabeamento Estruturado, Switches
  - Telefonia, Manutenção e Conhecimento Avançado em Hardware</li>
                    <li><span class="white">3. SERVIDORES & VIRTUALIZAÇÃO:</span>
  - Servidores Windows e Linux, Proxmox VE, Hyper-V
  - Soluções de Containers (Docker/LXC)</li>
                    <li><span class="white">4. SEGURANÇA DA INFORMAÇÃO & FIREWALLS:</span>
  - FortiGate, Unifi Controller, Políticas de Segurança e Mitigação de Riscos</li>
                    <li><span class="white">5. MONITORAMENTO, SUPORTE & ANÁLISE:</span>
  - Zabbix, Zammad, Habilidades Analíticas e Resolução Rápida de Incidentes</li>
                    <li><span class="white">6. DESENVOLVIMENTO, CLOUD & IA:</span>
  - Lógica de Programação, Front-End (HTML/CSS), PaaS (Coolify)
  - Conhecimento Avançado em Inteligência Artificial Local e Generativa</li>
                </ul>
            </div>
        </div>

        <!-- Comando 3: cat projetos -->
        <div class="command-block">
            <div><span class="prompt">root@ncr7:~# </span><span class="cmd-text">cat projetos_NCR7.txt</span></div>
            <div class="white">-- Projetos Recentes NCR7 --</div>
            <div>> Participação ativa na implementação do Provimento 213/2026 na área da Tecnologia da Informação (Fevereiro 2026)</div>
            <div>> Implementação Microsoft Intune (Março 2026)</div>
            <div>> Setup de IA Local (Stable Diffusion) para geração de imagens via RTX 2070 Super (Maio 2026)</div>
            <div>> Autohospedagem e Deploy Contínuo (CI/CD) via Coolify com integração GitHub Apps/Webhooks (Junho 2026)</div>
            <div>> Implantação e gestão de servidores dedicados de jogos e alta disponibilidade (Junho 2026)</div>
        </div>

        <!-- Contato e Cursor Final -->
        <div class="command-block">
            <div><span class="prompt">root@ncr7:~# > </span><span class="cyan">Contate-nos: root@ncr7.com.br / ncr7.com.br</span><span class="cursor"></span></div>
        </div>

        <!-- Footer Bar -->
        <div class="status-bar">
            <div>NCR7 CLI | Uptime: 24/7/365 | Status: <span class="green">ONLINE</span></div>
            <div>logged as root</div>
        </div>

    </div>
</div>

</body>
</html>
