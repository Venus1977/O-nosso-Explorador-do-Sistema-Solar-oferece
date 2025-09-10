<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>📖 README - Explorador do Sistema Solar</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f0f23 100%);
            color: white;
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #667eea, #764ba2);
            padding: 40px;
            text-align: center;
        }

        .header h1 {
            font-size: 3em;
            margin-bottom: 10px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }

        .header p {
            font-size: 1.2em;
            opacity: 0.9;
        }

        .content {
            padding: 40px;
        }

        .section {
            margin: 40px 0;
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .section h2 {
            color: #667eea;
            font-size: 2em;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .section h3 {
            color: #4ecdc4;
            font-size: 1.4em;
            margin: 25px 0 15px 0;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .feature-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 10px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            text-align: center;
        }

        .feature-card .emoji {
            font-size: 3em;
            margin-bottom: 10px;
            display: block;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 20px 0;
        }

        .tech-badge {
            background: linear-gradient(45deg, #667eea, #764ba2);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9em;
            font-weight: bold;
        }

        .code-block {
            background: #2d3748;
            color: #e2e8f0;
            padding: 20px;
            border-radius: 10px;
            font-family: 'Courier New', monospace;
            margin: 15px 0;
            overflow-x: auto;
            border: 1px solid #4a5568;
        }

        .btn {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            font-size: 1.1em;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
            margin: 10px 5px;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .btn.success {
            background: linear-gradient(45deg, #4CAF50, #45a049);
        }

        .btn.warning {
            background: linear-gradient(45deg, #ff9800, #f57c00);
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            color: #4ecdc4;
            margin-bottom: 5px;
        }

        .highlight {
            background: rgba(255, 235, 59, 0.2);
            border: 1px solid rgba(255, 235, 59, 0.5);
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
        }

        .warning {
            background: rgba(244, 67, 54, 0.2);
            border: 1px solid rgba(244, 67, 54, 0.5);
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
        }

        .success {
            background: rgba(76, 175, 80, 0.2);
            border: 1px solid rgba(76, 175, 80, 0.5);
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
        }

        ul, ol {
            margin: 15px 0;
            padding-left: 30px;
        }

        li {
            margin: 8px 0;
        }

        .screenshot-placeholder {
            background: rgba(255, 255, 255, 0.1);
            border: 2px dashed rgba(255, 255, 255, 0.3);
            padding: 40px;
            text-align: center;
            border-radius: 10px;
            margin: 20px 0;
            color: #ccc;
        }

        .footer {
            background: rgba(0, 0, 0, 0.3);
            padding: 30px;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        @media (max-width: 768px) {
            .container {
                margin: 10px;
                border-radius: 15px;
            }
            
            .header {
                padding: 30px 20px;
            }
            
            .header h1 {
                font-size: 2.2em;
            }
            
            .content {
                padding: 30px 20px;
            }
            
            .section {
                padding: 20px;
            }
            
            .feature-grid {
                grid-template-columns: 1fr;
            }
            
            .stats {
                grid-template-columns: repeat(2, 1fr);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🚀 Explorador do Sistema Solar</h1>
            <p>Jogo educativo interativo para descobrir os segredos do nosso sistema solar</p>
        </div>

        <div class="content">
            <!-- Visão Geral -->
            <div class="section">
                <h2>🌟 Visão Geral</h2>
                <p>O <strong>Explorador do Sistema Solar</strong> é um jogo educativo interativo desenvolvido especialmente para jovens exploradores entre os 8 e 16 anos. Combina diversão com aprendizagem, permitindo descobrir os planetas, completar missões espaciais e usar ferramentas científicas.</p>
                
                <div class="stats">
                    <div class="stat-card">
                        <div class="stat-number">8</div>
                        <div>Planetas</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">5</div>
                        <div>Missões</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">3</div>
                        <div>Ferramentas</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">8</div>
                        <div>Conquistas</div>
                    </div>
                </div>
            </div>

            <!-- Funcionalidades -->
            <div class="section">
                <h2>✨ Funcionalidades Principais</h2>
                
                <div class="feature-grid">
                    <div class="feature-card">
                        <span class="emoji">🪐</span>
                        <h3>Sistema Solar 3D</h3>
                        <p>Órbitas animadas e planetas interativos com informações detalhadas</p>
                    </div>
                    
                    <div class="feature-card">
                        <span class="emoji">🚀</span>
                        <h3>Missões Espaciais</h3>
                        <p>5 missões baseadas em explorações reais da NASA</p>
                    </div>
                    
                    <div class="feature-card">
                        <span class="emoji">📏</span>
                        <h3>Ferramentas Científicas</h3>
                        <p>Medição, comparação e calculadora espacial</p>
                    </div>
                    
                    <div class="feature-card">
                        <span class="emoji">🏆</span>
                        <h3>Sistema de Conquistas</h3>
                        <p>8 conquistas para motivar a exploração</p>
                    </div>
                    
                    <div class="feature-card">
                        <span class="emoji">📱</span>
                        <h3>Design Responsivo</h3>
                        <p>Funciona perfeitamente em todos os dispositivos</p>
                    </div>
                    
                    <div class="feature-card">
                        <span class="emoji">🌐</span>
                        <h3>Funciona Offline</h3>
                        <p>Não precisa de internet após ser guardado</p>
                    </div>
                </div>
            </div>

            <!-- Como Usar -->
            <div class="section">
                <h2>🎮 Como Usar</h2>
                
                <h3>🚀 Início Rápido</h3>
                <ol>
                    <li><strong>Guarda o ficheiro:</strong> Copia o código HTML e guarda como <code>explorador-sistema-solar.html</code></li>
                    <li><strong>Abre o jogo:</strong> Faz duplo-clique no ficheiro para abrir no navegador</li>
                    <li><strong>Explora:</strong> Clica nos planetas, inicia missões e usa as ferramentas!</li>
                </ol>

                <h3>🎯 Objetivos do Jogo</h3>
                <ul>
                    <li>Visitar todos os 8 planetas do sistema solar</li>
                    <li>Completar as 5 missões espaciais disponíveis</li>
                    <li>Usar as 3 ferramentas científicas</li>
                    <li>Desbloquear todas as 8 conquistas</li>
                </ul>

                <div class="highlight">
                    <strong>💡 Dica:</strong> Clica em tudo! O jogo foi desenhado para ser explorado livremente. Cada clique pode revelar informações interessantes sobre o espaço.
                </div>
            </div>

            <!-- Tecnologias -->
            <div class="section">
                <h2>⚙️ Tecnologias Utilizadas</h2>
                
                <div class="tech-stack">
                    <span class="tech-badge">HTML5</span>
                    <span class="tech-badge">CSS3</span>
                    <span class="tech-badge">JavaScript ES6+</span>
                    <span class="tech-badge">Tailwind CSS</span>
                    <span class="tech-badge">CSS Animations</span>
                    <span class="tech-badge">Responsive Design</span>
                    <span class="tech-badge">Local Storage</span>
                </div>

                <h3>🏗️ Arquitetura</h3>
                <ul>
                    <li><strong>Frontend:</strong> HTML5 semântico com CSS3 moderno</li>
                    <li><strong>Interatividade:</strong> JavaScript vanilla (sem dependências)</li>
                    <li><strong>Dados:</strong> Objetos JavaScript com informações científicas precisas</li>
                    <li><strong>Animações:</strong> CSS keyframes e transitions</li>
                    <li><strong>Responsividade:</strong> CSS Grid e Flexbox</li>
                </ul>
            </div>

            <!-- Instalação -->
            <div class="section">
                <h2>💾 Instalação e Configuração</h2>
                
                <h3>📋 Pré-requisitos</h3>
                <ul>
                    <li>Qualquer navegador moderno (Chrome, Firefox, Safari, Edge)</li>
                    <li>Não precisa de servidor web ou instalação especial</li>
                    <li>Funciona offline após ser guardado</li>
                </ul>

                <h3>🔧 Passos de Instalação</h3>
                <div class="code-block">
# 1. Copia o código HTML completo
# 2. Cria um novo ficheiro de texto
# 3. Cola o código no ficheiro
# 4. Guarda como "explorador-sistema-solar.html"
# 5. Abre o ficheiro no navegador
                </div>

                <div class="success">
                    <strong>✅ Pronto!</strong> O jogo está instalado e pronto a usar. Não são necessárias configurações adicionais.
                </div>
            </div>

            <!-- Estrutura do Projeto -->
            <div class="section">
                <h2>📁 Estrutura do Projeto</h2>
                
                <div class="code-block">
explorador-sistema-solar.html
├── HTML Structure
│   ├── Header (título e estatísticas)
│   ├── Navigation (tabs)
│   ├── Planets Tab (sistema solar 3D)
│   ├── Missions Tab (5 missões espaciais)
│   ├── Tools Tab (ferramentas científicas)
│   └── Achievements Tab (conquistas)
├── CSS Styling
│   ├── Responsive Design
│   ├── Animations & Transitions
│   ├── Dark Space Theme
│   └── Interactive Elements
└── JavaScript Logic
    ├── Game State Management
    ├── Planet Data & Information
    ├── Mission System
    ├── Scientific Tools
    └── Achievement System
                </div>
            </div>

            <!-- Funcionalidades Detalhadas -->
            <div class="section">
                <h2>🔍 Funcionalidades Detalhadas</h2>
                
                <h3>🪐 Sistema de Planetas</h3>
                <ul>
                    <li><strong>Visualização 3D:</strong> Sistema solar animado com órbitas realistas</li>
                    <li><strong>Informações Científicas:</strong> Dados precisos sobre cada planeta</li>
                    <li><strong>Interatividade:</strong> Clique para explorar cada planeta</li>
                    <li><strong>Progresso:</strong> Acompanha planetas visitados</li>
                </ul>

                <h3>🚀 Sistema de Missões</h3>
                <ul>
                    <li><strong>Missão Apollo:</strong> Revive a ida à Lua</li>
                    <li><strong>Exploração de Marte:</strong> Procura vida no planeta vermelho</li>
                    <li><strong>Missão Voyager:</strong> Viaja pelos planetas exteriores</li>
                    <li><strong>Missão Júpiter:</strong> Estuda o maior planeta</li>
                    <li><strong>Exploração de Saturno:</strong> Descobre os anéis misteriosos</li>
                </ul>

                <h3>📏 Ferramentas Científicas</h3>
                <ul>
                    <li><strong>Medição de Distâncias:</strong> Calcula distâncias entre planetas</li>
                    <li><strong>Comparação de Tamanhos:</strong> Visualiza diferenças de escala</li>
                    <li><strong>Calculadora Espacial:</strong> Para cálculos científicos</li>
                </ul>

                <h3>🏆 Sistema de Conquistas</h3>
                <ul>
                    <li>Primeiro Explorador (visitar 1 planeta)</li>
                    <li>Meio Sistema (visitar 4 planetas)</li>
                    <li>Mestre do Sistema Solar (visitar todos os planetas)</li>
                    <li>Astronauta Iniciante (completar 1 missão)</li>
                    <li>Astronauta Experiente (completar 3 missões)</li>
                    <li>Mestre das Missões (completar todas as missões)</li>
                    <li>Cientista Iniciante (usar 1 ferramenta)</li>
                    <li>Mestre da Ciência (usar todas as ferramentas)</li>
                </ul>
            </div>

            <!-- Personalização -->
            <div class="section">
                <h2>🎨 Personalização</h2>
                
                <h3>🌈 Modificar Cores</h3>
                <p>Para alterar o esquema de cores, edita as variáveis CSS no início do ficheiro:</p>
                <div class="code-block">
/* Cores principais */
--primary-color: #667eea;
--secondary-color: #764ba2;
--accent-color: #4ecdc4;
--success-color: #4caf50;
                </div>

                <h3>📝 Adicionar Conteúdo</h3>
                <p>Para adicionar novos planetas ou missões, edita os objetos JavaScript:</p>
                <div class="code-block">
// Adicionar novo planeta
const planetsData = {
    'NovoPlaneta': {
        name: 'Novo Planeta',
        emoji: '🌍',
        description: 'Descrição do planeta...',
        facts: ['Facto 1', 'Facto 2'],
        color: '#cor-hex'
    }
};
                </div>

                <h3>🔧 Modificar Funcionalidades</h3>
                <ul>
                    <li>Adicionar novas ferramentas científicas</li>
                    <li>Criar missões personalizadas</li>
                    <li>Implementar novos tipos de conquistas</li>
                    <li>Modificar animações e efeitos visuais</li>
                </ul>
            </div>

            <!-- Compatibilidade -->
            <div class="section">
                <h2>🌐 Compatibilidade</h2>
                
                <h3>💻 Navegadores Suportados</h3>
                <div class="feature-grid">
                    <div class="feature-card">
                        <span class="emoji">🌐</span>
                        <h4>Chrome</h4>
                        <p>Versão 80+</p>
                    </div>
                    <div class="feature-card">
                        <span class="emoji">🦊</span>
                        <h4>Firefox</h4>
                        <p>Versão 75+</p>
                    </div>
                    <div class="feature-card">
                        <span class="emoji">🧭</span>
                        <h4>Safari</h4>
                        <p>Versão 13+</p>
                    </div>
                    <div class="feature-card">
                        <span class="emoji">🔷</span>
                        <h4>Edge</h4>
                        <p>Versão 80+</p>
                    </div>
                </div>

                <h3>📱 Dispositivos</h3>
                <ul>
                    <li><strong>Desktop:</strong> Windows, macOS, Linux</li>
                    <li><strong>Tablet:</strong> iPad, Android tablets</li>
                    <li><strong>Mobile:</strong> iPhone, Android phones</li>
                    <li><strong>Resolução:</strong> Otimizado para 16:9, mas responsivo</li>
                </ul>
            </div>

            <!-- Resolução de Problemas -->
            <div class="section">
                <h2>🔧 Resolução de Problemas</h2>
                
                <h3>❌ Problemas Comuns</h3>
                
                <div class="warning">
                    <strong>Problema:</strong> O jogo não carrega ou aparece em branco
                    <br><strong>Solução:</strong>
                    <ul>
                        <li>Verifica se o ficheiro termina em .html</li>
                        <li>Certifica-te que copiaste todo o código</li>
                        <li>Tenta noutro navegador</li>
                        <li>Recarrega a página (F5)</li>
                    </ul>
                </div>

                <div class="warning">
                    <strong>Problema:</strong> As animações não funcionam
                    <br><strong>Solução:</strong>
                    <ul>
                        <li>Atualiza o navegador para a versão mais recente</li>
                        <li>Verifica se o JavaScript está ativado</li>
                        <li>Desativa extensões que possam interferir</li>
                    </ul>
                </div>

                <div class="warning">
                    <strong>Problema:</strong> O jogo não responde no telemóvel
                    <br><strong>Solução:</strong>
                    <ul>
                        <li>Usa o jogo na orientação horizontal</li>
                        <li>Fecha outras aplicações para libertar memória</li>
                        <li>Atualiza o navegador móvel</li>
                    </ul>
                </div>
            </div>

            <!-- Contribuição -->
            <div class="section">
                <h2>🤝 Contribuição</h2>
                
                <p>Este projeto foi criado com fins educativos. Se quiseres contribuir ou melhorar o jogo:</p>
                
                <h3>💡 Ideias para Melhorias</h3>
                <ul>
                    <li>Adicionar mais planetas (planetas anões, exoplanetas)</li>
                    <li>Implementar quiz sobre astronomia</li>
                    <li>Criar modo multijogador</li>
                    <li>Adicionar sons e música espacial</li>
                    <li>Implementar realidade aumentada</li>
                    <li>Criar versão em outras línguas</li>
                </ul>

                <h3>🔄 Como Contribuir</h3>
                <ol>
                    <li>Faz uma cópia do código</li>
                    <li>Implementa as tuas melhorias</li>
                    <li>Testa em diferentes dispositivos</li>
                    <li>Partilha as tuas modificações</li>
                </ol>
            </div>

            <!-- Licença -->
            <div class="section">
                <h2>📄 Licença e Créditos</h2>
                
                <h3>📜 Licença</h3>
                <p>Este projeto é de código aberto e pode ser usado livremente para fins educativos. Podes modificar, distribuir e usar o código como quiseres.</p>

                <h3>🙏 Créditos</h3>
                <ul>
                    <li><strong>Dados Científicos:</strong> NASA, ESA</li>
                    <li><strong>Inspiração:</strong> Missões espaciais reais</li>
                    <li><strong>Design:</strong> Inspirado no cosmos</li>
                    <li><strong>Emojis:</strong> Unicode Consortium</li>
                </ul>

                <h3>⚖️ Disclaimer</h3>
                <p>As informações científicas foram simplificadas para fins educativos. Para dados precisos e atualizados, consulta fontes oficiais como NASA e ESA.</p>
            </div>

            <!-- FAQ -->
            <div class="section">
                <h2>❓ Perguntas Frequentes</h2>
                
                <h3>🤔 O jogo precisa de internet?</h3>
                <p>Não! Após guardares o ficheiro HTML no teu computador, o jogo funciona completamente offline.</p>

                <h3>🎯 Para que idades é adequado?</h3>
                <p>O jogo foi desenhado para idades entre 8-16 anos, mas pode ser divertido para toda a família!</p>

                <h3>💾 Como guardo o meu progresso?</h3>
                <p>O progresso é guardado automaticamente no navegador. Se limpares os dados do navegador, o progresso será perdido.</p>

                <h3>🔄 Posso modificar o jogo?</h3>
                <p>Sim! O código é aberto e podes modificar tudo o que quiseres. É uma ótima forma de aprender programação!</p>

                <h3>📱 Funciona no telemóvel?</h3>
                <p>Sim! O jogo é totalmente responsivo e funciona em todos os dispositivos.</p>

                <h3>🌍 Está disponível noutras línguas?</h3>
                <p>Atualmente só está em português, mas podes traduzir o código facilmente.</p>
            </div>
        </div>

        <div class="footer">
            <h3>🚀 Explorador do Sistema Solar</h3>
            <p>Criado com ❤️ para jovens exploradores do espaço</p>
            <p style="margin-top: 15px; opacity: 0.7;">
                Versão 1.0 | Última atualização: 2024
            </p>
        </div>
    </div>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'97ce375ce72d2186',t:'MTc1NzQ5OTg3Mi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
