# ATLAS-Inspired Particle Detector Simulation

## 🔬 Scientific Overview

This interactive web simulation models the **ATLAS Inner Detector** system at CERN, demonstrating real-time particle tracking through multiple detector layers with Kalman filter reconstruction. The project showcases key concepts in high-energy physics detector technology and track reconstruction algorithms used in modern particle physics experiments.

### Physics Concepts Demonstrated

1. **Multi-layer Silicon Detector Geometry**
   - 4 concentric detector layers (Pixel L0/L1, SCT L0/L1)
   - Realistic ATLAS Inner Detector radii and material budget
   - Cylindrical coordinate system with magnetic field

2. **Charged Particle Dynamics**
   - Lorentz force in 2T solenoid magnetic field: **F = q(v × B)**
   - Helical trajectories for charged particles
   - Energy-momentum relationships: **E² = (pc)² + (mc²)²**

3. **Detector Physics Effects**
   - **Multiple Scattering**: θ₀ = 13.6 MeV/(βpc) × √(x/X₀) × [1 + 0.038ln(x/X₀)]
   - Hit efficiency and measurement uncertainties
   - Material budget effects on track resolution

4. **Kalman Filter Track Reconstruction**
   - State vector: [x, y, px, py]
   - Prediction: **x̂ₖ₊₁ = Fₖx̂ₖ**
   - Update: **x̂ₖ = x̂ₖ⁻ + Kₖ(zₖ - Hₖx̂ₖ⁻)**
   - Real-time track fitting with process and measurement noise

## 🚀 Quick Start

### Local Development
```bash
# Clone the repository
git clone https://github.com/username/atlas-detector-simulation
cd atlas-detector-simulation

# Install dependencies
npm install

# Start local server
npm start

# Open browser to http://localhost:3000
```

### Live Demo
🌐 **[View Live Simulation](https://your-deployment-url.vercel.app)**

## 🎮 Interactive Features

### Real-time Controls
- **Beam Parameters**: Particle energy (1-100 GeV), production rate, particle type (μ±, π±, e±)
- **Detector Settings**: Magnetic field strength, material budget, hit efficiency
- **Kalman Filter**: Tunable process and measurement noise parameters
- **Physics Visualization**: Particle tracks, detector hits, reconstructed trajectories

### ROOT-Inspired Analysis
- **Event Statistics**: Live tracking efficiency, χ²/DoF quality metrics
- **Momentum Histograms**: Real-time transverse momentum distributions
- **Hit Patterns**: Visual detector response and reconstruction quality

## 🔧 Technical Implementation

### Core Technologies
- **Three.js**: 3D visualization and particle rendering
- **JavaScript**: Real-time physics simulation and Kalman filtering
- **HTML5 Canvas**: Interactive controls and histogram displays
- **CSS3**: CERN-inspired terminal aesthetic

### Physics Engine Features
```javascript
// Lorentz force calculation
applyLorentzForce(deltaTime) {
    const qOverM = this.charge / this.mass;
    const cyclotronFreq = qOverM * magneticField;
    // Helical motion in B-field
    this.velocity.x = vx * Math.cos(ωt) - vy * Math.sin(ωt);
    this.velocity.y = vx * Math.sin(ωt) + vy * Math.cos(ωt);
}

// Kalman filter update
updateKalmanFilter(hit) {
    // Prediction step: x̂ₖ₊₁ = Fₖx̂ₖ
    // Innovation: ν = zₖ - Hₖx̂ₖ⁻
    // Update: x̂ₖ = x̂ₖ⁻ + Kₖνₖ
}
```

## 🎯 CERN Connection

This simulation directly relates to CERN's research in several ways:

### ATLAS Experiment Relevance
- **Inner Detector Layout**: Accurate representation of ATLAS silicon tracking layers
- **Track Reconstruction**: Real implementation of algorithms used in ATLAS software
- **Physics Processes**: Multiple scattering and energy loss models from particle physics

### Modern Detector Challenges
- **Pattern Recognition**: Identifying particle tracks in high-multiplicity events
- **Real-time Processing**: Fast reconstruction for trigger systems
- **Noise Handling**: Robust tracking in presence of detector inefficiencies

## 📊 Performance Metrics

The simulation tracks key performance indicators used in real detector analysis:

- **Reconstruction Efficiency**: Percentage of generated particles successfully tracked
- **Track Quality**: χ²/DoF distribution for fitted tracks
- **Momentum Resolution**: Accuracy of momentum measurement from curvature
- **Hit Pattern**: Detector layer occupancy and efficiency

## 🚀 Deployment

### Vercel (Recommended)
```bash
# Deploy to Vercel
npx vercel --prod

# Custom domain configuration available
```

### Netlify Alternative
```bash
# Build and deploy
npm run build
# Drag/drop dist folder to Netlify
```

### Local Testing
```bash
# Quick local server
python -m http.server 8000
# or
npx serve .
```

## 🔬 Scientific Accuracy

### Physics Validation
- **Energy-momentum conservation** maintained throughout simulation
- **Realistic material interaction** cross-sections
- **Proper electromagnetic field** equations
- **Statistical noise models** matching detector specifications

### ATLAS Detector Parameters
- **Magnetic field**: 2T solenoid (adjustable 0-4T)
- **Layer radii**: 4, 7, 11, 15 cm (based on ATLAS Inner Detector)
- **Material budget**: ~2% X₀ per layer (typical silicon detector)
- **Hit resolution**: ~10 μm spatial precision

## 📈 Educational Extensions

### Advanced Features to Add
1. **Vertex Reconstruction**: Secondary vertex finding for B-meson decays
2. **Particle Identification**: dE/dx energy loss for mass identification
3. **Event Display**: Multi-track events with jet reconstruction
4. **Machine Learning**: Neural network track finding algorithms

### Research Applications
- **Algorithm Development**: Test new tracking algorithms
- **Detector Optimization**: Study layer placement and material effects
- **Performance Studies**: Efficiency vs. fake rate optimization

## 🤝 Contributing

This project demonstrates advanced understanding of:
- **Particle Physics**: Electromagnetic interactions, detector response
- **Mathematical Methods**: Kalman filtering, statistical estimation
- **Software Engineering**: Real-time simulation, interactive visualization
- **Scientific Computing**: Physics engine development, data analysis

## 📧 Contact

**LinkedIn Summary for CERN Application:**
*"Developed an interactive ATLAS detector simulation featuring real-time Kalman filter track reconstruction, demonstrating deep understanding of particle physics, detector technology, and the mathematical algorithms used in modern high-energy physics experiments. The simulation accurately models electromagnetic interactions, multiple scattering, and statistical reconstruction methods employed in CERN's particle detection systems."*

---

**Created for CERN Internship Application** | **Demonstrates**: Particle Physics, Detector Technology, Kalman Filtering, JavaScript/Three.js, Scientific Computing
