<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Painel de Indicadores de Desenvolvimento Sustentável</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body class="bg-slate-50 font-sans text-slate-800 flex h-screen overflow-hidden">
    <aside class="w-64 bg-emerald-900 text-white flex flex-col justify-between hidden md:flex">
        <div>
            <div class="p-5 flex items-center gap-3 border-b border-emerald-800">
                <i class="fa-solid fa-leaf text-2xl text-emerald-400"></i>
                <span class="font-bold text-lg tracking-wide">IDS Dashboard</span>
            </div>
            <nav class="p-4 space-y-2">
                <a href="#" class="flex items-center gap-3 px-4 py-3 bg-emerald-800 rounded-lg text-emerald-300 font-medium transition">
                    <i class="fa-solid fa-chart-line"></i> Visão Geral
                </a>
                <a href="#" class="flex items-center gap-3 px-4 py-3 text-emerald-100 hover:bg-emerald-800/50 rounded-lg transition">
                    <i class="fa-solid fa-bolt"></i> Energia Limpa
                </a>
                <a href="#" class="flex items-center gap-3 px-4 py-3 text-emerald-100 hover:bg-emerald-800/50 rounded-lg transition">
                    <i class="fa-solid fa-faucet-water"></i> Água e Saneamento
                </a>
                <a href="#" class="flex items-center gap-3 px-4 py-3 text-emerald-100 hover:bg-emerald-800/50 rounded-lg transition">
                    <i class="fa-solid fa-hand-holding-heart"></i> Impacto Social
                </a>
                <a href="#" class="flex items-center gap-3 px-4 py-3 text-emerald-100 hover:bg-emerald-800/50 rounded-lg transition">
                    <i class="fa-solid fa-file-export"></i> Relatórios
                </a>
            </nav>
        </div>
        <div class="p-4 border-t border-emerald-800 text-xs text-emerald-400 text-center">
            Data de Atualização: 2026
        </div>
    </aside>

    <main class="flex-1 flex flex-col overflow-y-auto"> 
        <header class="bg-white border-b border-slate-200 px-8 py-4 flex justify-between items-center shrink-0">
            <div>
                <h1 class="text-2xl font-bold text-slate-900">Indicadores de Desenvolvimento Sustentável</h1>
                <p class="text-sm text-slate-500">Acompanhamento em tempo real das metas da Agenda 2030</p>
            </div>
            <div class="flex items-center gap-4">
                <button class="bg-emerald-50 text-emerald-700 font-semibold px-4 py-2 rounded-lg border border-emerald-200 hover:bg-emerald-100 transition flex items-center gap-2">
                    <i class="fa-solid fa-download"></i> Exportar Dados
                </button>
                <div class="w-10 h-10 bg-slate-200 rounded-full flex items-center justify-center font-bold text-slate-600 border border-slate-300">
                    AI
                </div>
            </div>
        </header>

        <div class="p-8 space-y-8 max-w-7xl w-full mx-auto">     
            <section class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-6">        
                <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm flex flex-col justify-between">
                    <div class="flex justify-between items-start">
                        <div>
                            <p class="text-sm font-semibold text-slate-500 uppercase tracking-wider">Emissões de CO₂</p>
                            <h3 class="text-3xl font-bold text-slate-900 mt-1">12.4 t <span class="text-xs text-slate-400 font-normal">/capita</span></h3>
                        </div>
                        <span class="p-3 bg-red-50 text-red-600 rounded-xl"><i class="fa-solid fa-cloud-sun text-xl"></i></span>
                    </div>
                    <div class="mt-4">
                        <div class="flex justify-between text-xs font-medium text-slate-500 mb-1">
                            <span>Meta: -15% até fim do ano</span>
                            <span class="text-red-500 font-bold">+2.4% <i class="fa-solid fa-arrow-trend-up"></i></span>
                        </div>
                        <div class="w-full bg-slate-100 rounded-full h-2">
                            <div class="bg-red-500 h-2 rounded-full" style="width: 78%"></div>
                        </div>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm flex flex-col justify-between">
                    <div class="flex justify-between items-start">
                        <div>
                            <p class="text-sm font-semibold text-slate-500 uppercase tracking-wider">Matriz Renovável</p>
                            <h3 class="text-3xl font-bold text-slate-900 mt-1">64.8%</h3>
                        </div>
                        <span class="p-3 bg-amber-50 text-amber-600 rounded-xl"><i class="fa-solid fa-solar-panel text-xl"></i></span>
                    </div>
                    <div class="mt-4">
                        <div class="flex justify-between text-xs font-medium text-slate-500 mb-1">
                            <span>Meta atingida</span>
                            <span class="text-emerald-500 font-bold">86% da Meta</span>
                        </div>
                        <div class="w-full bg-slate-100 rounded-full h-2">
                            <div class="bg-amber-500 h-2 rounded-full" style="width: 86%"></div>
                        </div>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm flex flex-col justify-between">
                    <div class="flex justify-between items-start">
                        <div>
                            <p class="text-sm font-semibold text-slate-500 uppercase tracking-wider">Acesso à Água Potável</p>
                            <h3 class="text-3xl font-bold text-slate-900 mt-1">91.2%</h3>
                        </div>
                        <span class="p-3 bg-blue-50 text-blue-600 rounded-xl"><i class="fa-solid fa-droplet text-xl"></i></span>
                    </div>
                    <div class="mt-4">
                        <div class="flex justify-between text-xs font-medium text-slate-500 mb-1">
                            <span>População atendida</span>
                            <span class="text-emerald-500 font-bold">+1.2% este mês</span>
                        </div>
                        <div class="w-full bg-slate-100 rounded-full h-2">
                            <div class="bg-blue-600 h-2 rounded-full" style="width: 91%"></div>
                        </div>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm flex flex-col justify-between">
                    <div class="flex justify-between items-start">
                        <div>
                            <p class="text-sm font-semibold text-slate-500 uppercase tracking-wider">Índice Gini Social</p>
                            <h3 class="text-3xl font-bold text-slate-900 mt-1">0.465</h3>
                        </div>
                        <span class="p-3 bg-purple-50 text-purple-600 rounded-xl"><i class="fa-solid fa-users text-xl"></i></span>
                    </div>
                    <div class="mt-4">
                        <div class="flex justify-between text-xs font-medium text-slate-500 mb-1">
                            <span>Meta de redução: 0.420</span>
                            <span class="text-emerald-500 font-bold">-0.008 <i class="fa-solid fa-arrow-trend-down"></i></span>
                        </div>
                        <div class="w-full bg-slate-100 rounded-full h-2">
                            <div class="bg-purple-600 h-2 rounded-full" style="width: 55%"></div>
                        </div>
                    </div>
                </div>
            </section>

            <section class="grid grid-cols-1 lg:grid-cols-3 gap-6">     
                <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm lg:col-span-2">
                    <div class="flex justify-between items-center mb-6">
                        <div>
                            <h4 class="text-lg font-bold text-slate-900">Histórico de Emissões vs. Investimento Verde</h4>
                            <p class="text-xs text-slate-400">Análise comparativa anual</p>
                        </div>
                        <div class="flex items-center gap-2 text-xs font-semibold text-slate-500 bg-slate-100 p-1 rounded-lg">
                            <button class="bg-white px-3 py-1.5 rounded-md shadow-sm text-slate-800">Anual</button>
                            <button class="px-3 py-1.5 rounded-md">Mensal</button>
                        </div>
                    </div>
                    <div class="relative h-80">
                        <canvas id="mixedChart"></canvas>
                    </div>
                </div>

                <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm">
                    <div class="mb-6">
                        <h4 class="text-lg font-bold text-slate-900">Desempenho por ODS</h4>
                        <p class="text-xs text-slate-400">Proximidade da meta ideal (100%)</p>
                    </div>
                    <div class="relative h-80 flex items-center justify-center">
                        <canvas id="radarChart"></canvas>
                    </div>
                </div>
            </section>

            <section class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden">
                <div class="p-6 border-b border-slate-100 flex justify-between items-center">
                    <h4 class="text-lg font-bold text-slate-900">Status de Iniciativas por Região</h4>
                    <span class="text-xs bg-emerald-50 text-emerald-700 px-2.5 py-1 rounded-full font-semibold">4 Projetos Ativos</span>
                </div>
                <div class="overflow-x-auto">
                    <table class="w-full text-left border-collapse">
                        <thead>
                            <tr class="bg-slate-50 border-b border-slate-200 text-xs font-bold text-slate-500 uppercase tracking-wider">
                                <th class="py-4 px-6">Iniciativa / Região</th>
                                <th class="py-4 px-6">ODS Principal</th>
                                <th class="py-4 px-6">Orçamento Alocado</th>
                                <th class="py-4 px-6">Status de Impacto</th>
                            </tr>
                        </thead>
                        <tbody class="text-sm divide-y divide-slate-100 text-slate-600">
                            <tr>
                                <td class="py-4 px-6 font-medium text-slate-900">Complexo Eólico Regional Norte</td>
                                <td class="py-4 px-6"><span class="bg-amber-100 text-amber-800 text-xs font-semibold px-2 py-1 rounded">ODS 7 - Energia Limpa</span></td>
                                <td class="py-4 px-6">R$ 14.2 M</td>
                                <td class="py-4 px-6"><span class="inline-flex items-center gap-1.5 text-xs font-semibold text-emerald-600 bg-emerald-50 px-2.5 py-1 rounded-full"><span class="w-1.5 h-1.5 bg-emerald-500 rounded-full"></span>Excelente</span></td>
                            </tr>
                            <tr>
                                <td class="py-4 px-6 font-medium text-slate-900">Saneamento e Balneabilidade Sul</td>
                                <td class="py-4 px-6"><span class="bg-blue-100 text-blue-800 text-xs font-semibold px-2 py-1 rounded">ODS 6 - Água Potável</span></td>
                                <td class="py-4 px-6">R$ 8.7 M</td>
                                <td class="py-4 px-6"><span class="inline-flex items-center gap-1.5 text-xs font-semibold text-amber-600 bg-amber-50 px-2.5 py-1 rounded-full"><span class="w-1.5 h-1.5 bg-amber-500 rounded-full"></span>Em Atenção</span></td>
                            </tr>
                            <tr>
                                <td class="py-4 px-6 font-medium text-slate-900">Reflorestamento de Biomas Leste</td>
                                <td class="py-4 px-6"><span class="bg-emerald-100 text-emerald-800 text-xs font-semibold px-2 py-1 rounded">ODS 15 - Vida Terrestre</span></td>
                                <td class="py-4 px-6">R$ 3.1 M</td>
                                <td class="py-4 px-6"><span class="inline-flex items-center gap-1.5 text-xs font-semibold text-emerald-600 bg-emerald-50 px-2.5 py-1 rounded-full"><span class="w-1.5 h-1.5 bg-emerald-500 rounded-full"></span>Excelente</span></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </section>
        </div>
    </main>

    <script>
        // Gráfico Combinado: Linhas (Emissões) + Barras (Investimento)
        const ctxMixed = document.getElementById('mixedChart').getContext('2d');
        new Chart(ctxMixed, {
            type: 'bar',
            data: {
                labels: ['2021', '2022', '2023', '2024', '2025', '2026'],
                datasets: [
                    {
                        type: 'line',
                        label: 'Emissões CO₂ (Milhões Ton)',
                        data: [15.2, 14.8, 14.1, 13.5, 12.9, 12.4],
                        borderColor: '#ef4444',
                        backgroundColor: 'transparent',
                        borderWidth: 3,
                        pointBackgroundColor: '#ef4444',
                        yAxisID: 'y-emissions'
                    },
                    {
                        label: 'Investimento em Tecnologia Verde (R$ Milhões)',
                        data: [4.2, 5.5, 6.8, 8.1, 11.0, 14.2],
                        backgroundColor: '#10b981',
                        borderRadius: 6,
                        yAxisID: 'y-investment'
                    }
                ]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { position: 'top', labels: { boxWidth: 12, font: { family: 'sans-serif', size: 12 } } }
                },
                scales: {
                    'y-emissions': {
                        type: 'linear',
                        position: 'left',
                        title: { display: true, text: 'CO₂ (t)' },
                        grid: { drawOnChartArea: false }
                    },
                    'y-investment': {
                        type: 'linear',
                        position: 'right',
                        title: { display: true, text: 'Investimento (R$)' }
                    }
                }
            }
        }); 

        // Gráfico de Radar: Desempenho dos ODS
        const ctxRadar = document.getElementById('radarChart').getContext('2d');
        new Chart(ctxRadar, {
            type: 'radar',
            data: {
                labels: ['ODS 6 (Água)', 'ODS 7 (Energia)', 'ODS 11 (Cidades)', 'ODS 12 (Consumo)', 'ODS 13 (Clima)', 'ODS 15 (Vida)'],
                datasets: [{
                    label: 'Progresso Atual %',
                    data: [91, 64, 55, 72, 48, 80],
                    backgroundColor: 'rgba(16, 185, 129, 0.2)',
                    borderColor: '#10b981',
                    pointBackgroundColor: '#10b981',
                    borderWidth: 2
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { display: false }
                },
                scales: {
                    r: {
                        angleLines: { display: true },
                        suggestedMin: 0,
                        suggestedMax: 100
                    }
                }
            }
        });
    </script>
</body>
</html>
