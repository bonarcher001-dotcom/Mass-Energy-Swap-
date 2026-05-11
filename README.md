
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interconvertibility of Mass & Energy</title>
    <style>
        :root { --dark: #1a1a2e; --light: #ffffff; --gold: #f1c40f; --blue: #3498db; }
        body { font-family: 'Segoe UI', sans-serif; background: #fdfdfd; color: #333; line-height: 1.7; margin: 0; padding: 0; }
        header { background: var(--dark); color: white; padding: 60px 20px; text-align: center; }
        .container { max-width: 800px; margin: -40px auto 40px; background: white; padding: 40px; border-radius: 12px; box-shadow: 0 15px 35px rgba(0,0,0,0.1); }
        h1 { margin: 0; font-size: 2.5rem; }
        h2 { color: var(--blue); border-bottom: 2px solid #eee; padding-bottom: 10px; margin-top: 40px; }
        
        /* Interactive Calculator */
        .calc-box { background: #f8f9fa; border: 2px solid var(--blue); padding: 25px; border-radius: 10px; margin: 30px 0; }
        .calc-input { display: flex; gap: 10px; margin-bottom: 20px; }
        input[type="number"] { flex: 1; padding: 10px; border: 1px solid #ccc; border-radius: 5px; font-size: 1rem; }
        .result-display { background: var(--dark); color: var(--gold); padding: 20px; border-radius: 5px; text-align: center; font-family: 'Courier New', monospace; font-size: 1.2rem; }
        
        .formula { text-align: center; font-size: 2rem; margin: 30px 0; color: #e74c3c; font-weight: bold; }
        .info-card { background: #e7f3ff; padding: 20px; border-left: 5px solid var(--blue); border-radius: 4px; }
    </style>
</head>
<body>

<header>
    <h1>Matter and Energy</h1>
    <p>Two sides of the same coin</p>
</header>

<div class="container">
    <h2>1. What is Interconvertibility?</h2>
    <p>
        For centuries, scientists thought mass and energy were separate. However, Albert Einstein proved that mass is actually <strong>highly concentrated energy</strong>. They can be converted back and forth. 
    </p>

    <div class="formula">
        E = mc^2
    </div>

    <p>
        In this equation, c is the speed of light (300,000,000 m/s). Because c^2 is an incredibly large number, even a tiny amount of mass contains a staggering amount of energy.
    </p>

    <div class="calc-box">
        <h3>⚡ Mass-Energy Converter</h3>
        <p>Enter a mass in <strong>grams</strong> to see how much energy it holds:</p>
        <div class="calc-input">
            <input type="number" id="massInput" placeholder="Enter mass (e.g., 1)" min="0">
            <button onclick="calculateEnergy()" style="background: var(--blue); color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer;">Convert</button>
        </div>
        <div class="result-display" id="energyResult">
            Energy Released: 0 Joules
        </div>
        <p style="font-size: 0.8rem; color: #666; margin-top: 10px;">
            *Calculated using c = 299,792,458 m/s
        </p>
    </div>

    <h2>2. Real-World Examples</h2>
    <div class="info-card">
        <strong>Nuclear Fusion:</strong> In the Sun, hydrogen atoms fuse to form helium. The resulting helium weighs slightly <em>less</em> than the original hydrogen. That "missing" mass isn't gone—it was converted into the light and heat that keeps us alive!
    </div>
    
    <p>
        <strong>Pair Production:</strong> This is the opposite. Pure energy (like a high-energy gamma ray) can spontaneously transform into matter, creating an electron and its "twin," a positron. Energy becomes mass.
    </p>

    <h2>3. The Law of Conservation</h2>
    <p>
        Because of this interconvertibility, we no longer say "Mass is conserved" or "Energy is conserved." Instead, we use the <strong>Law of Conservation of Mass-Energy</strong>. The total amount of mass-energy in a closed system remains constant.
    </p>
</div>

<footer style="text-align: center; padding: 20px; color: #888;">
    &copy; 2026 Created by CHMSU TALISAY BSED SCIENCE - 3A
</footer>

<!-- Math Rendering -->
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

<script>
    function calculateEnergy() {
        const massGrams = document.getElementById('massInput').value;
        const massKg = massGrams / 1000;
        const c = 299792458;
        
        if (massGrams > 0) {
            const energy = massKg * Math.pow(c, 2);
            // Format to scientific notation
            document.getElementById('energyResult').innerText = 
                `Energy Released: ${energy.toExponential(4)} Joules`;
        } else {
            document.getElementById('energyResult').innerText = "Please enter a valid mass.";
        }
    }
</script>

</body>
</html>
