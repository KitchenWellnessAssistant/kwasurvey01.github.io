<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Research Insights: The AI Kitchen Wellness Assistant</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 400px;
        }
        @media (max-width: 768px) {
            .chart-container {
                height: 300px;
            }
        }
        .kpi-card {
            background-color: white;
            border-radius: 0.5rem;
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
            padding: 1.5rem;
            text-align: center;
        }
        .ai-feature-card {
            background-color: white;
            border-radius: 0.5rem;
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
            padding: 1.5rem;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }
    </style>
</head>
<body class="bg-gray-50">

    <header class="text-center p-8 md:p-12" style="background-color: #073B4C; color: white;">
        <h1 class="text-4xl md:text-5xl font-bold mb-2">The Modern Kitchen Dilemma</h1>
        <p class="text-lg md:text-xl max-w-3xl mx-auto" style="color: #FFD166;">Insights from user research on the future of AI-assisted cooking and wellness.</p>
    </header>

    <main class="container mx-auto p-4 md:p-8">

        <section id="demographics" class="mb-12">
            <h2 class="text-3xl font-bold text-center mb-2" style="color: #118AB2;">Who We Surveyed</h2>
            <p class="text-center text-gray-600 mb-8 max-w-2xl mx-auto">The study primarily engaged a young, academically-focused audience in Italy, providing a clear snapshot of a tech-savvy user base facing time constraints.</p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-xl font-semibold text-center mb-4" style="color: #073B4C;">Age Distribution</h3>
                    <div class="chart-container" style="height: 300px;">
                        <canvas id="ageChart"></canvas>
                    </div>
                     <p class="text-sm text-gray-500 mt-4 text-center">A significant majority of respondents are under 35, highlighting a youth-centric perspective on kitchen technology.</p>
                </div>
                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-xl font-semibold text-center mb-4" style="color: #073B4C;">Primary Occupation</h3>
                    <div class="chart-container" style="height: 300px;">
                        <canvas id="occupationChart"></canvas>
                    </div>
                     <p class="text-sm text-gray-500 mt-4 text-center">Over half of the participants are students, often identifying as "Busy Academics," which shapes their need for efficiency.</p>
                </div>
            </div>
        </section>
        
        <section id="priorities" class="mb-12">
            <h2 class="text-3xl font-bold text-center mb-2" style="color: #118AB2;">The Health-Convenience Paradox</h2>
            <p class="text-center text-gray-600 mb-8 max-w-2xl mx-auto">Users are torn. They crave healthy, nutritious meals but are constrained by a lack of time. This core conflict defines the primary opportunity for an AI kitchen assistant.</p>
            <div class="bg-white rounded-lg shadow-md p-6">
                <h3 class="text-xl font-semibold text-center mb-4" style="color: #073B4C;">Top Priorities at Home</h3>
                <div class="chart-container">
                    <canvas id="prioritiesChart"></canvas>
                </div>
                <p class="text-sm text-gray-500 mt-4 text-center">"Health & Nutrition" and "Convenience & Speed" are the dominant, often competing, priorities, with "Creativity" following as a key motivator for hobby cooks.</p>
            </div>
        </section>

        <section id="pain-points" class="mb-12">
            <h2 class="text-3xl font-bold text-center mb-2" style="color: #118AB2;">Key Kitchen Frustrations</h2>
            <p class="text-center text-gray-600 mb-8 max-w-2xl mx-auto">From time-consuming prep to wasted food, users face tangible and costly challenges in their daily kitchen routines.</p>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="kpi-card md:col-span-2 lg:col-span-1">
                    <h3 class="text-xl font-semibold mb-2" style="color: #073B4C;">Not Enough Time</h3>
                    <p class="text-5xl font-bold" style="color: #FF6B6B;">45%</p>
                    <p class="text-gray-600 mt-2">of users feel they lack sufficient time for meal prep, citing busy academic and work schedules.</p>
                </div>
                <div class="bg-white rounded-lg shadow-md p-6 lg:col-span-2">
                    <h3 class="text-xl font-semibold text-center mb-4" style="color: #073B4C;">Grocery Shopping Inefficiencies</h3>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-8">
                        <div>
                             <div class="chart-container" style="height:250px;">
                                <canvas id="impulseBuyChart"></canvas>
                            </div>
                            <p class="text-sm text-gray-500 mt-4 text-center">A majority of users frequently make unplanned purchases, driven by discounts or in-store discoveries.</p>
                        </div>
                        <div>
                             <div class="chart-container" style="height:250px;">
                                <canvas id="forgottenItemsChart"></canvas>
                            </div>
                            <p class="text-sm text-gray-500 mt-4 text-center">Forgetting key recipe ingredients is a common frustration, leading to extra trips or last-minute meal changes.</p>
                        </div>
                    </div>
                </div>
                 <div class="bg-white rounded-lg shadow-md p-6 md:col-span-2 lg:col-span-3">
                    <h3 class="text-xl font-semibold text-center mb-4" style="color: #073B4C;">The Cost of Domestic Food Waste</h3>
                     <p class="text-center text-gray-600 mb-4 max-w-2xl mx-auto">Food waste is a real financial drain, primarily caused by fresh produce spoiling and packaged goods expiring before use.</p>
                    <div class="chart-container" style="height: 300px;">
                        <canvas id="foodWasteChart"></canvas>
                    </div>
                </div>
            </div>
        </section>

        <section id="inventory" class="mb-12">
            <h2 class="text-3xl font-bold text-center mb-2" style="color: #118AB2;">The Inventory Management Gap</h2>
            <p class="text-center text-gray-600 mb-8 max-w-2xl mx-auto">There's a massive disconnect between how users currently track kitchen items and the sophisticated, automated solution they truly desire.</p>
            <div class="bg-white rounded-lg shadow-md p-8">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                    <div class="text-center">
                        <h4 class="text-2xl font-semibold mb-4" style="color: #073B4C;">Current State: Manual & Flawed</h4>
                        <div class="space-y-4">
                            <div class="flex items-center justify-center p-4 rounded-lg bg-red-100">
                                <span class="text-3xl mr-4">🧠</span>
                                <span class="font-semibold text-red-800">Reliance on Memory (70%)</span>
                            </div>
                            <div class="flex items-center justify-center p-4 rounded-lg bg-yellow-100">
                                <span class="text-3xl mr-4">🗒️</span>
                                <span class="font-semibold text-yellow-800">Post-it Notes & Lists</span>
                            </div>
                            <div class="flex items-center justify-center p-4 rounded-lg bg-gray-100">
                                <span class="text-3xl mr-4">🤷</span>
                                <span class="font-semibold text-gray-800">No System At All</span>
                            </div>
                        </div>
                    </div>
                    <div class="text-center">
                         <h4 class="text-2xl font-semibold mb-4" style="color: #073B4C;">Desired AI: Smart & Proactive</h4>
                         <div class="space-y-4">
                            <div class="flex items-center justify-center p-4 rounded-lg bg-green-100">
                                <span class="text-3xl mr-4">🔔</span>
                                <span class="font-semibold text-green-800">Expiry Date Alerts</span>
                            </div>
                             <div class="flex items-center justify-center p-4 rounded-lg bg-blue-100">
                                <span class="text-3xl mr-4">🍲</span>
                                <span class="font-semibold text-blue-800">"Use-it-Up" Recipe Suggestions</span>
                            </div>
                            <div class="flex items-center justify-center p-4 rounded-lg bg-indigo-100">
                                <span class="text-3xl mr-4">🛒</span>
                                <span class="font-semibold text-indigo-800">Automated Grocery Lists</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="perceptions" class="mb-12">
             <h2 class="text-3xl font-bold text-center mb-2" style="color: #118AB2;">Perceptions of an AI Assistant</h2>
            <p class="text-center text-gray-600 mb-8 max-w-2xl mx-auto">Users are open to AI assistance but have clear boundaries on trust and a high sensitivity to price.</p>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                 <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-xl font-semibold text-center mb-4" style="color: #073B4C;">Trust in AI: Suggestions vs. Automation</h3>
                    <div class="chart-container">
                        <canvas id="trustChart"></canvas>
                    </div>
                    <p class="text-sm text-gray-500 mt-4 text-center">Users show moderate trust in AI for dietary advice but are highly skeptical of letting an AI purchase groceries automatically.</p>
                </div>
                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-xl font-semibold text-center mb-4" style="color: #073B4C;">Willingness to Pay (Monthly)</h3>
                    <div class="chart-container">
                        <canvas id="priceChart"></canvas>
                    </div>
                    <p class="text-sm text-gray-500 mt-4 text-center">The market shows extreme price sensitivity, with a vast majority unwilling to pay or only willing to pay a very small monthly fee.</p>
                </div>
            </div>
        </section>

        <section id="ai-features" class="mb-12">
            <h2 class="text-3xl font-bold text-center mb-2" style="color: #118AB2;">Experience the AI Assistant</h2>
            <p class="text-center text-gray-600 mb-8 max-w-2xl mx-auto">See how the AI Kitchen Wellness Assistant can help solve common kitchen dilemmas, powered by generative AI.</p>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="ai-feature-card">
                    <h3 class="text-xl font-semibold text-center" style="color: #073B4C;">✨ AI Meal Plan Generator</h3>
                    <p class="text-gray-600 text-sm">Get a personalized 3-day meal plan based on typical user needs: healthy, quick, and efficient.</p>
                    <button id="generateMealPlanBtn" class="px-6 py-3 rounded-lg font-bold text-white transition-colors duration-300" style="background-color: #06D6A0; hover:bg-[#05a87e];">Generate Meal Plan ✨</button>
                    <div id="mealPlanLoading" class="text-center text-gray-500 hidden">Loading...</div>
                    <div id="mealPlanOutput" class="p-4 border rounded-lg overflow-auto max-h-96" style="border-color: #118AB2; background-color: #F7F7F7; color: #073B4C;"></div>
                </div>

                <div class="ai-feature-card">
                    <h3 class="text-xl font-semibold text-center" style="color: #073B4C;">✨ AI "Use-It-Up" Recipe Suggester</h3>
                    <p class="text-gray-600 text-sm">Enter ingredients you have to get a recipe suggestion, helping reduce food waste.</p>
                    <input type="text" id="ingredientsInput" placeholder="e.g., chicken, broccoli, pasta, cheese" class="p-2 border rounded-lg focus:ring-2" style="border-color: #118AB2; focus:ring-[#118AB2];">
                    <button id="generateRecipeBtn" class="px-6 py-3 rounded-lg font-bold text-white transition-colors duration-300" style="background-color: #FFD166; hover:bg-[#ffc233];">Suggest Recipe ✨</button>
                    <div id="recipeLoading" class="text-center text-gray-500 hidden">Loading...</div>
                    <div id="recipeOutput" class="p-4 border rounded-lg overflow-auto max-h-96" style="border-color: #118AB2; background-color: #F7F7F7; color: #073B4C;"></div>
                </div>
            </div>
        </section>
        
    </main>
    
    <footer class="text-center p-6 mt-8" style="background-color: #073B4C; color: white;">
        <p class="text-sm">Research Conducted June 2025 with the University of Ca’Foscari’s PiNK office.</p>
    </footer>

    <script>
        const energeticPalette = {
            red: '#FF6B6B',
            yellow: '#FFD166',
            green: '#06D6A0',
            blue: '#118AB2',
            darkBlue: '#073B4C',
            lightGray: '#F7F7F7'
        };

        const defaultTooltipCallback = {
            plugins: {
                tooltip: {
                    callbacks: {
                        title: function(tooltipItems) {
                            const item = tooltipItems[0];
                            let label = item.chart.data.labels[item.dataIndex];
                            if (Array.isArray(label)) {
                              return label.join(' ');
                            } else {
                              return label;
                            }
                        }
                    }
                }
            }
        };
        
        function wrapLabel(str, maxWidth) {
            if (str.length <= maxWidth) {
                return str;
            }
            let a = [];
            let words = str.split(' ');
            let currentLine = words[0];
            for (let i = 1; i < words.length; i++) {
                if (currentLine.length + words[i].length + 1 < maxWidth) {
                    currentLine += ' ' + words[i];
                } else {
                    a.push(currentLine);
                    currentLine = words[i];
                }
            }
            a.push(currentLine);
            return a;
        }

        new Chart(document.getElementById('ageChart'), {
            type: 'bar',
            data: {
                labels: ['18-24', '25-34', '35-44', '45-54', '55+'],
                datasets: [{
                    label: 'Age Distribution',
                    data: [53.6, 29.8, 9.5, 6.0, 2.4],
                    backgroundColor: [energeticPalette.green, energeticPalette.yellow, energeticPalette.red, energeticPalette.blue, energeticPalette.darkBlue],
                    borderColor: 'white',
                    borderWidth: 2
                }]
            },
            options: {
                ...defaultTooltipCallback,
                indexAxis: 'y',
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    ...defaultTooltipCallback.plugins,
                    legend: { display: false }
                },
                scales: {
                    x: { ticks: { color: energeticPalette.darkBlue }, grid: { display: false }},
                    y: { ticks: { color: energeticPalette.darkBlue }}
                }
            }
        });
        
        new Chart(document.getElementById('occupationChart'), {
            type: 'doughnut',
            data: {
                labels: ['Student', 'Full-time Job', 'Part-time Job', 'Other'],
                datasets: [{
                    data: [65.5, 31.0, 15.5, 10],
                    backgroundColor: [energeticPalette.blue, energeticPalette.green, energeticPalette.yellow, energeticPalette.red],
                    borderColor: 'white',
                    borderWidth: 4
                }]
            },
            options: {
                ...defaultTooltipCallback,
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                     ...defaultTooltipCallback.plugins,
                    legend: { position: 'bottom', labels: { color: energeticPalette.darkBlue } }
                }
            }
        });

        new Chart(document.getElementById('prioritiesChart'), {
            type: 'radar',
            data: {
                labels: ['Health & Nutrition', 'Convenience & Speed', 'Creativity & New Recipes', 'Affordability', 'Sustainability'],
                datasets: [{
                    label: 'User Priorities',
                    data: [90, 85, 65, 50, 40],
                    backgroundColor: 'rgba(6, 214, 160, 0.2)',
                    borderColor: energeticPalette.green,
                    pointBackgroundColor: energeticPalette.green,
                    pointBorderColor: '#fff',
                    pointHoverBackgroundColor: '#fff',
                    pointHoverBorderColor: energeticPalette.green
                }]
            },
            options: {
                ...defaultTooltipCallback,
                responsive: true,
                maintainAspectRatio: false,
                 plugins: {
                     ...defaultTooltipCallback.plugins,
                    legend: { display: false }
                },
                scales: {
                    r: {
                        angleLines: { color: '#e0e0e0' },
                        grid: { color: '#e0e0e0' },
                        pointLabels: { font: { size: 14 }, color: energeticPalette.darkBlue },
                        ticks: { backdropColor: 'white', color: energeticPalette.blue }
                    }
                }
            }
        });

        new Chart(document.getElementById('impulseBuyChart'), {
            type: 'pie',
            data: {
                labels: ['Often/Sometimes', 'Rarely/Never'],
                datasets: [{
                    data: [68, 32],
                    backgroundColor: [energeticPalette.red, energeticPalette.lightGray],
                    borderColor: 'white',
                    borderWidth: 4
                }]
            },
            options: {
                ...defaultTooltipCallback,
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    ...defaultTooltipCallback.plugins,
                    title: { display: true, text: 'Impulse Buys', color: energeticPalette.darkBlue, font: { size: 16 } },
                    legend: { display: false }
                }
            }
        });

        new Chart(document.getElementById('forgottenItemsChart'), {
            type: 'pie',
            data: {
                labels: ['Often/Occasionally', 'Rarely/Never'],
                datasets: [{
                    data: [75, 25],
                    backgroundColor: [energeticPalette.yellow, energeticPalette.lightGray],
                    borderColor: 'white',
                    borderWidth: 4
                }]
            },
            options: {
                ...defaultTooltipCallback,
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    ...defaultTooltipCallback.plugins,
                    title: { display: true, text: 'Forgotten Items', color: energeticPalette.darkBlue, font: { size: 16 } },
                    legend: { display: false }
                }
            }
        });

        new Chart(document.getElementById('foodWasteChart'), {
            type: 'bar',
            data: {
                labels: ['0-2€', '3-5€', '6-10€', '11-15€', 'More than 16€'],
                datasets: [{
                    label: 'Weekly Food Waste (€)',
                    data: [35, 30, 20, 10, 5],
                    backgroundColor: energeticPalette.red,
                }]
            },
            options: {
                ...defaultTooltipCallback,
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    ...defaultTooltipCallback.plugins,
                    legend: { display: false }
                },
                scales: {
                    y: { beginAtZero: true, ticks: { color: energeticPalette.darkBlue }, grid: { display: false } },
                    x: { ticks: { color: energeticPalette.darkBlue } }
                }
            }
        });

        new Chart(document.getElementById('trustChart'), {
            type: 'bar',
            data: {
                labels: ['Low Trust (1-2)', 'Medium Trust (3)', 'High Trust (4-5)'],
                datasets: [
                    {
                        label: 'Dietary Suggestions',
                        data: [15, 35, 50],
                        backgroundColor: energeticPalette.green,
                    },
                    {
                        label: 'Automated Groceries',
                        data: [75, 15, 10],
                        backgroundColor: energeticPalette.red,
                    }
                ]
            },
            options: {
                ...defaultTooltipCallback,
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                     ...defaultTooltipCallback.plugins,
                    legend: { position: 'bottom' }
                },
                scales: {
                    y: { beginAtZero: true, ticks: { callback: value => value + '%', color: energeticPalette.darkBlue } },
                    x: { ticks: { color: energeticPalette.darkBlue } }
                }
            }
        });

        new Chart(document.getElementById('priceChart'), {
            type: 'polarArea',
            data: {
                labels: ['€0 (Free)', '€1-5', '€6-10', '€11-15', '€15+'],
                datasets: [{
                    label: 'Willingness to Pay',
                    data: [40, 35, 15, 5, 5],
                    backgroundColor: [
                        energeticPalette.red,
                        energeticPalette.yellow,
                        energeticPalette.green,
                        energeticPalette.blue,
                        energeticPalette.darkBlue
                    ],
                    borderWidth: 2,
                    borderColor: '#fff'
                }]
            },
            options: {
                ...defaultTooltipCallback,
                responsive: true,
                maintainAspectRatio: false,
                 plugins: {
                    ...defaultTooltipCallback.plugins,
                    legend: { position: 'bottom', labels: { color: energeticPalette.darkBlue } }
                },
                scales: {
                    r: {
                        ticks: { display: false },
                        grid: { circular: true }
                    }
                }
            }
        });

        document.getElementById('generateMealPlanBtn').addEventListener('click', generateMealPlan);
        document.getElementById('generateRecipeBtn').addEventListener('click', generateRecipeSuggestion);

        async function generateMealPlan() {
            const mealPlanOutput = document.getElementById('mealPlanOutput');
            const mealPlanLoading = document.getElementById('mealPlanLoading');
            mealPlanOutput.innerHTML = '';
            mealPlanLoading.classList.remove('hidden');

            const prompt = "Generate a simple, healthy, and quick 3-day meal plan for a busy student. Focus on minimal ingredients and easy preparation. Include breakfast, lunch, and dinner for each day.";
            const chatHistory = [{ role: "user", parts: [{ text: prompt }] }];
            const payload = { contents: chatHistory };
            const apiKey = "";
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${apiKey}`;

            try {
                const response = await fetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });
                const result = await response.json();
                if (result.candidates && result.candidates.length > 0 &&
                    result.candidates[0].content && result.candidates[0].content.parts &&
                    result.candidates[0].content.parts.length > 0) {
                    const text = result.candidates[0].content.parts[0].text;
                    mealPlanOutput.innerHTML = formatLLMText(text);
                } else {
                    mealPlanOutput.innerHTML = '<p class="text-red-500">Error: Could not generate meal plan. Please try again.</p>';
                }
            } catch (error) {
                console.error('Error fetching meal plan:', error);
                mealPlanOutput.innerHTML = '<p class="text-red-500">Error: Failed to connect to the AI service. Please check your network connection.</p>';
            } finally {
                mealPlanLoading.classList.add('hidden');
            }
        }

        async function generateRecipeSuggestion() {
            const ingredientsInput = document.getElementById('ingredientsInput').value;
            const recipeOutput = document.getElementById('recipeOutput');
            const recipeLoading = document.getElementById('recipeLoading');
            recipeOutput.innerHTML = '';
            recipeLoading.classList.remove('hidden');

            if (!ingredientsInput.trim()) {
                recipeOutput.innerHTML = '<p class="text-red-500">Please enter some ingredients.</p>';
                recipeLoading.classList.add('hidden');
                return;
            }

            const prompt = `Given these ingredients: ${ingredientsInput}. Suggest a simple, quick, and easy recipe that uses them up. Focus on minimizing waste and suggest alternatives for missing common ingredients.`;
            const chatHistory = [{ role: "user", parts: [{ text: prompt }] }];
            const payload = { contents: chatHistory };
            const apiKey = "";
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${apiKey}`;

            try {
                const response = await fetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });
                const result = await response.json();
                if (result.candidates && result.candidates.length > 0 &&
                    result.candidates[0].content && result.candidates[0].content.parts &&
                    result.candidates[0].content.parts.length > 0) {
                    const text = result.candidates[0].content.parts[0].text;
                    recipeOutput.innerHTML = formatLLMText(text);
                } else {
                    recipeOutput.innerHTML = '<p class="text-red-500">Error: Could not generate recipe. Please try again.</p>';
                }
            } catch (error) {
                console.error('Error fetching recipe:', error);
                recipeOutput.innerHTML = '<p class="text-red-500">Error: Failed to connect to the AI service. Please check your network connection.</p>';
            } finally {
                recipeLoading.classList.add('hidden');
            }
        }

        function formatLLMText(text) {
            return text.replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>') // Bold
                       .replace(/\*(.*?)\*/g, '<em>$1</em>') // Italics
                       .replace(/^- (.*)/gm, '<li>$1</li>') // List items
                       .replace(/(\d+\. .*)/gm, '<li>$1</li>') // Numbered list items
                       .replace(/(\n\n|^)(.*?)(?=\n\n|\n$)/g, (match, p1, p2) => {
                           if (p2.startsWith('<li>') || p2.startsWith('<strong>Day') || p2.startsWith('<em>')) {
                               return match;
                           }
                           return `${p1}<p>${p2}</p>`;
                       }) // Paragraphs
                       .replace(/(\n|^)\s*(\d+\.)\s*(.*)/g, '<p>$2 $3</p>') // Handle numbered lists (like 1. Intro)
                       .replace(/### (.*)/g, '<h3>$1</h3>') // H3
                       .replace(/## (.*)/g, '<h2>$1</h2>') // H2
                       .replace(/# (.*)/g, '<h1>$1</h1>'); // H1
        }
    </script>
</body>
</html>
