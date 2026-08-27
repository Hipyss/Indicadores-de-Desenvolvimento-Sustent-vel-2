{
  "name": "meu-blog-tech",
  "displayName": "Meu Blog Tech",
  "description": "Exibe notícias de tecnologia do Meu blog tech no VS Code",
  "version": "1.0.0",
  "engines": {
    "vscode": "^1.80.0"
  },
  "categories": [
    "Other"
  ],
  "main": "./extension.js",
  "activationEvents": [],
  "contributes": {
    "commands": [
      {
        "command": "meuBlogTech.openPost",
        "title": "Meu Blog Tech: Abrir Notícias"
      }
    ]
  }
}
const vscode = require('vscode');

function activate(context) {
    let disposable = vscode.commands.registerCommand('meuBlogTech.openPost', function () {
        // Cria e exibe um painel de Webview no VS Code
        const panel = vscode.window.createWebviewPanel(
            'meuBlogTech',
            'Meu blog tech - Notícias',
            vscode.ViewColumn.One,
            { enableScripts: true }
        );

        // Insere o HTML do post na janela
        panel.webview.html = getWebviewContent();
    });

    context.subscriptions.push(disposable);
}

function getWebviewContent() {
    return `<!DOCTYPE html>
    <html lang="pt-BR">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Meu blog tech</title>
        <style>
            body {
                font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
                padding: 20px;
                background-color: var(--vscode-editor-background);
                color: var(--vscode-editor-foreground);
                line-height: 1.6;
            }
            header {
                border-bottom: 2px solid var(--vscode-activityBar-activeBorder);
                padding-bottom: 10px;
                margin-bottom: 20px;
            }
            .logo {
                font-size: 1.8rem;
                font-weight: bold;
                color: #38bdf8;
                text-decoration: none;
            }
            .category {
                background-color: #0369a1;
                color: #ffffff;
                padding: 3px 8px;
                border-radius: 4px;
                font-size: 0.8rem;
                font-weight: bold;
                text-transform: uppercase;
            }
            h1 {
                font-size: 1.8rem;
                margin: 15px 0 10px 0;
                color: var(--vscode-editor-foreground);
            }
            .meta {
                font-size: 0.85rem;
                opacity: 0.8;
                margin-bottom: 20px;
            }
            img {
                max-width: 100%;
                height: auto;
                border-radius: 6px;
                margin-bottom: 20px;
            }
            p {
                margin-bottom: 15px;
                font-size: 1rem;
            }
            h2 {
                font-size: 1.3rem;
                margin-top: 20px;
            }
        </style>
    </head>
    <body>
        <header>
            <div class="logo">Meu blog tech</div>
        </header>

        <main>
            <span class="category">Inteligência Artificial</span>
            <h1>O Impacto dos Novos Processadores na Evolução da IA Local</h1>
            <div class="meta">Por <strong>Redação Meu blog tech</strong> | 2026</div>

            <img src="https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?auto=format&fit=crop&w=800&q=80" alt="Tecnologia">

            <p>A tecnologia avança a passos largos e o grande foco da indústria está na capacidade de rodar sistemas complexos diretamente nos dispositivos, sem depender exclusivamente da nuvem.</p>
            
            <p>Os novos chips trazem arquiteturas desenhadas especificamente para processar algoritmos de IA de forma local. Isso garante mais velocidade, privacidade e economia de dados.</p>

            <h2>O que muda para o usuário?</h2>
            <p>Tarefas como tradução simultânea e assistentes virtuais avançados funcionam de forma instantânea, mesmo sem conexão com a internet.</p>
        </main>
    </body>
    </html>`;
}

function deactivate() {}

module.exports = {
    activate,
    deactivate
};
