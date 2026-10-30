# CCAITrial1

Urban Heat Island introduction webpage:

- Local file: [index.html](./index.html)
- GitHub Pages (after enabling Pages for this repository): [https://bot-bot-bot-bot-bot-bot.github.io/CCAITrial1/](https://bot-bot-bot-bot-bot-bot.github.io/CCAITrial1/)
As mentioned.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Concrete Jungles & Fever Dreams | The UHI Effect</title>
    <style>
        :root {
            --bg-dark: #0f172a;
            --bg-card: rgba(30, 41, 59, 0.7);
            --accent-hot: #ff512f;
            --accent-cool: #00d2ff;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 2rem;
            background: radial-gradient(circle at 50% 50%, rgba(255, 81, 47, 0.15) 0%, rgba(15, 23, 42, 1) 70%);
            position: relative;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 5rem);
            font-weight: 800;
            background: linear-gradient(90deg, var(--accent-hot), var(--accent-cool));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
            letter-spacing: -1px;
        }

        .hero p {
            font-size: 1.25rem;
            color: var(--text-muted);
            max-width: 600px;
            margin-bottom: 2rem;
        }

        .scroll-indicator {
            position: absolute;
            bottom: 2rem;
            animation: bounce 2s infinite;
            color: var(--text-muted);
            font-size: 1.5rem;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(10px); }
        }

        /* Sections */
        section {
            max-width: 1000px;
            margin: 0 auto;
            padding: 4rem 2rem;
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .glass-card {
            background: var(--bg-card);
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass-border);
            border-radius: 16px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
        }

        /* Interactive Slider */
        .simulator {
            text-align: center;
        }

        .temp-display {
            font-size: 4rem;
            font-weight: 800;
            margin: 1rem 0;
            transition: color 0.3s ease;
        }

        .slider-container {
            margin: 2rem 0;
        }

        input[type="range"] {
            -webkit-appearance: none;
            width: 100%;
            height: 8px;
            border-radius: 5px;
            background: linear-gradient(90deg, var(--accent-cool), var(--accent-hot));
            outline: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 24px;
            height: 24px;
            border-radius: 50%;
            background: white;
            cursor: pointer;
            box-shadow: 0 0 10px rgba(255,255,255,0.5);
        }

        /* Deep Dive Grid */
        .grid-2 {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
        }

        @media (max-width: 768px) {
            .grid-2 { grid-template-columns: 1fr; }
        }

        .stat-box {
            text-align: center;
            padding: 1.5rem;
            background: rgba(255,255,255,0.03);
            border-radius: 12px;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--accent-hot);
        }

        .stat-label {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-top: 0.5rem;
        }

        /* Tags */
        .tag {
            display: inline-block;
            padding: 0.25rem 0.75rem;
            background: rgba(0, 210, 255, 0.1);
            border: 1px solid var(--accent-cool);
            color: var(--accent-cool);
            border-radius: 20px;
            font-size: 0.8rem;
            margin-right: 0.5rem;
            margin-bottom: 0.5rem;
        }

        footer {
            text-align: center;
            padding: 2rem;
            color: var(--text-muted);
            font-size: 0.9rem;
            border-top: 1px solid var(--glass-border);
        }
    </style>
</head>
<body>

    <!-- Hero -->
    <header class="hero">
        <h1>Concrete Jungles &<br>Fever Dreams</h1>
        <p>Ever notice how walking across campus in July feels like stepping into an air fryer, but the nearby park feels like a different planet? Welcome to the Urban Heat Island effect.</p>
        <div class="scroll-indicator">↓</div>
    </header>

    <!-- The Basics -->
    <section>
        <h2 class="section-title">🌡️ The Basics: Why is the City Sweating?</h2>
        <div class="glass-card">
            <p>The <strong>Urban Heat Island (UHI)</strong> effect is exactly what it sounds like: cities act like giant sponges for heat. While rural areas might be a comfortable 25°C (77°F) at night, the city center can stay trapped at 30°C+ (86°F+).</p>
            <br>
            <p><strong>The Culprits:</strong></p>
            <ul style="margin-left: 1.5rem; margin-top: 0.5rem;">
                <li><strong>Low Albedo:</strong> Dark asphalt and roofs absorb solar radiation instead of reflecting it.</li>
                <li><strong>Lack of Evapotranspiration:</strong> We paved over the grass. Trees sweat (transpire) to cool the air; concrete just bakes.</li>
                <li><strong>Anthropogenic Heat:</strong> Cars, AC units, and human metabolism literally exhaust heat into the streets.</li>
                <li><strong>Canyon Effect:</strong> Tall buildings trap wind and block the sky, preventing heat from escaping at night.</li>
            </ul>
        </div>
    </section>

    <!-- Interactive Simulator -->
    <section>
        <h2 class="section-title">🎮 The Analytics: See the Data</h2>
        <div class="glass-card simulator">
            <p>As an urban analytics student, I look at Land Surface Temperature (LST) via satellite data. Let's simulate how <strong>Tree Canopy Cover</strong> changes the local microclimate.</p>
            
            <div class="slider-container">
                <label for="canopySlider">Drag to change Tree Canopy %:</label>
                <input type="range" min="0" max="100" value="10" id="canopySlider">
            </div>

            <div class="temp-display" id="tempDisplay">34°C</div>
            <p id="tempContext" style="color: var(--text-muted);">A barren concrete plaza. Time to melt.</p>
        </div>
    </section>

    <!-- Deep Dive -->
    <section>
        <h2 class="section-title">🏙️ The Deep Dive: Heat is a Zip Code Issue</h2>
        <div class="glass-card">
            <p>Here is where Urban Studies meets hard data. UHI isn't just an environmental issue; it's a massive <strong>social equity</strong> issue.</p>
            <br>
            <p>When we overlay historical <em>redlining maps</em> from the 1930s with modern satellite thermal imaging, the correlation is terrifying. Neighborhoods that were historically graded as "hazardous" (mostly minority and low-income areas) were systematically denied green infrastructure investments. Today, those exact same neighborhoods are up to <strong>7°C (12°F) hotter</strong> than wealthy, tree-lined suburbs just a few miles away.</p>
            <br>
            <p>Heat is the deadliest weather-related killer in the US, and it disproportionately targets vulnerable populations who often lack central AC.</p>
        </div>

        <div class="grid-2">
            <div class="glass-card stat-box">
                <div class="stat-number">12°F</div>
                <div class="stat-label">Average temp difference between redlined and greenlined neighborhoods.</div>
            </div>
            <div class="glass-card stat-box">
                <div class="stat-number">700+</div>
                <div class="stat-label">Annual US deaths attributed to extreme urban heat.</div>
            </div>
        </div>
    </section>

    <!-- Solutions -->
    <section>
        <h2 class="section-title">🌿 The Fix: Cooling the Grid</h2>
        <div class="glass-card">
            <p>Urban planning isn't just about zoning; it's about survival. Here is how we hack the city's thermal dynamics:</p>
            <br>
            <p><span class="tag">Cool Roofs</span> Painting roofs white or using reflective materials increases albedo, bouncing sunlight back into space.</p>
            <p><span class="tag">Green Corridors</span> Connecting parks with tree-lined streets creates wind tunnels that funnel cool air into the dense urban core.</p>
            <p><span class="tag">Permeable Pavement</span> Replacing solid concrete with porous materials allows water to seep in and evaporate, creating a natural cooling effect.</p>
            <p><span class="tag">Tech & IoT</span> Using CS and sensor networks to map micro-climates in real-time, allowing city planners to target interventions exactly where they are needed most.</p>
        </div>
    </section>

    <footer>
        <p>Built with ❤️, CSS, and a lot of coffee by a 1st Year CS & Urban Studies Student.</p>
        <p>Data concepts inspired by EPA & Urban Analytics coursework.</p>
    </footer>

    <script>
        // Interactive Temperature Simulator
        const slider = document.getElementById('canopySlider');
        const tempDisplay = document.getElementById('tempDisplay');
        const tempContext = document.getElementById('tempContext');

        slider.addEventListener('input', function() {
            const canopy = parseInt(this.value);
            // Base temp 36C at 0% canopy, drops to 24C at 100% canopy
            const temp = Math.round(36 - (canopy * 0.12)); 
            
            tempDisplay.innerText = `${temp}°C`;
            
            // Change color based on temp
            if (temp > 32) {
                tempDisplay.style.color = '#ff512f';
                tempContext.innerText = "A barren concrete plaza. Time to melt.";
            } else if (temp > 28) {
                tempDisplay.style.color = '#fdd835';
                tempContext.innerText = "A few scattered street trees. Still pretty warm.";
            } else if (temp > 25) {
                tempDisplay.style.color = '#66bb6a';
                tempContext.innerText = "A nice urban park. A gentle breeze helps.";
            } else {
                tempDisplay.style.color = '#00d2ff';
                tempContext.innerText = "A lush urban forest. Nature's air conditioning!";
            }
        });
    </script>
</body>
</html>
