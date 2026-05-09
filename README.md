<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>S.A.F.A.L. Predictive Systems Dashboard</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .glass { background: rgba(255, 255, 255, 0.9); backdrop-filter: blur(10px); }
        .gradient-bg { background: linear-gradient(135deg, #1e293b 0%, #334155 100%); }
        .pulse { animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite; }
        @keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: .5; } }
        .img-container { position: relative; overflow: hidden; border-radius: 0.75rem; background: #f8fafc; display: flex; align-items: center; justify-content: center; }
        img { width: 100%; height: 100%; object-fit: contain; }
    </style>
</head>
<body class="bg-gray-50 text-slate-900 font-sans">

    <!-- Navigation Header -->
    <nav class="gradient-bg text-white p-4 shadow-lg">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <div class="flex items-center gap-3">
                <div class="bg-blue-500 p-2 rounded-lg">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z" />
                    </svg>
                </div>
                <h1 class="text-xl font-bold tracking-tight">S.A.F.A.L. <span class="font-light text-blue-300">Command Center</span></h1>
            </div>
            <div class="flex items-center gap-6 text-sm font-medium">
                <span class="flex items-center gap-2"><span class="w-2 h-2 bg-blue-400 rounded-full"></span> Research Simulation</span>
                <span class="bg-slate-700 px-3 py-1 rounded">Region: Safdarjung, Delhi</span>
            </div>
        </div>
    </nav>

    <main class="max-w-7xl mx-auto p-6 grid grid-cols-1 lg:grid-cols-3 gap-6">
        
        <!-- Left Column: Metrics & Analysis -->
        <div class="lg:col-span-1 space-y-6">
            <!-- Risk Level Card -->
            <div class="bg-white p-6 rounded-2xl shadow-sm border border-gray-100">
                <h2 class="text-gray-500 text-xs font-bold uppercase tracking-widest mb-4">Current Prediction Risk</h2>
                <div class="flex items-end justify-between">
                    <div>
                        <p class="text-4xl font-black text-orange-500">MODERATE</p>
                        <p class="text-sm text-gray-500 mt-1">Based on 7-day soil saturation proxy</p>
                    </div>
                    <div class="text-right">
                        <p class="text-2xl font-bold">0.64</p>
                        <p class="text-xs text-gray-400">Risk Score</p>
                    </div>
                </div>
                <div class="w-full bg-gray-100 h-2 rounded-full mt-4">
                    <div class="bg-orange-500 h-2 rounded-full" style="width: 64%"></div>
                </div>
            </div>

            <!-- Architecture Snapshot -->
            <div class="bg-white p-4 rounded-2xl shadow-sm border border-gray-100">
                <h2 class="text-gray-500 text-xs font-bold uppercase tracking-widest mb-3">Pipeline Architecture</h2>
                <div class="img-container h-48 bg-slate-900">
                    <img src="architecture_diagram.png" alt="S.A.F.A.L Architecture" onerror="this.src='https://placehold.co/400x300/1e293b/white?text=Architecture+Diagram'">
                </div>
                <p class="text-[10px] text-gray-400 mt-3 italic">Sequential data flow: IMD Ingestion to Model Logic.</p>
            </div>

            <!-- Engineering Takeaway -->
            <div class="bg-blue-50 p-6 rounded-2xl border border-blue-100">
                <h3 class="text-blue-800 font-bold text-sm mb-2">Systems Insight</h3>
                <p class="text-blue-700 text-xs leading-relaxed">
                    The "Saturation Tipping Point" in Delhi was observed at ~150mm/week. Beyond this, response logic shifts from drainage management to automated pumping activation (Conceptual).
                </p>
            </div>
        </div>

        <!-- Center/Right: Data Visualizations -->
        <div class="lg:col-span-2 space-y-6">
            <!-- Main Graph Area: Prediction vs Actual -->
            <div class="bg-white p-6 rounded-2xl shadow-sm border border-gray-100">
                <div class="flex justify-between items-center mb-4">
                    <h2 class="font-bold text-lg text-slate-800">Model Verification: Sequential vs. Actual</h2>
                    <div class="flex gap-2">
                        <span class="text-xs px-2 py-1 bg-blue-100 text-blue-700 rounded">Validation Set</span>
                    </div>
                </div>
                
                <div class="img-container h-72">
                    <img src="prediction_vs_actual.png" alt="Prediction vs Actual Rainfall" onerror="this.src='https://placehold.co/800x400/f8fafc/64748b?text=Prediction+vs+Actual+Graph'">
                </div>
                <p class="text-[10px] text-gray-400 mt-4 text-center italic">Observing the model's tracking accuracy during hydrological outliers in the test window.</p>
            </div>

            <!-- Bottom Grid: Historical Trend and Loss Curve -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <!-- Rainfall Trend Analysis -->
                <div class="bg-white p-4 rounded-xl border border-gray-100">
                    <h3 class="text-xs font-bold text-gray-400 uppercase mb-3">Historical Trend (Safdarjung)</h3>
                    <div class="img-container h-48">
                        <img src="rainfall_trend_analysis.png" alt="Rainfall Trends" onerror="this.src='https://placehold.co/400x300/f8fafc/64748b?text=Trend+Analysis'">
                    </div>
                    <p class="text-[9px] text-gray-500 mt-2">32-year precipitation longitudinal study identifying monsoon variability.</p>
                </div>
                
                <!-- Training Loss Curve -->
                <div class="bg-white p-4 rounded-xl border border-gray-100">
                    <h3 class="text-xs font-bold text-gray-400 uppercase mb-3">Model Convergence (Loss)</h3>
                    <div class="img-container h-48">
                        <img src="training_loss_curve.png" alt="Training Loss Curve" onerror="this.src='https://placehold.co/400x300/f8fafc/64748b?text=Loss+Curve'">
                    </div>
                    <p class="text-[9px] text-gray-500 mt-2">Weighted loss optimization indicating model stability across 50 epochs.</p>
                </div>
            </div>
        </div>
    </main>

    <footer class="max-w-7xl mx-auto p-6 text-center text-gray-400 text-xs border-t border-gray-100 mt-6">
        <p>S.A.F.A.L | Exploratory Engineering Portfolio Project | Safdarjung Meteorological Dataset (1990–2022)</p>
    </footer>

</body>
</html>
