# Zexus Math Library 🧮

A comprehensive mathematical standard library for the Zexus programming language, featuring advanced numerical computing, linear algebra, signal processing, machine learning, cryptography, and more.

## 🚀 Features

### **Core Mathematics**
- **Complex Numbers**: Full complex arithmetic with polar coordinates
- **Linear Algebra**: Matrices, determinants, inverses, eigenvalues
- **Calculus**: Derivatives, integrals, root finding, differential equations
- **Special Functions**: Gamma, Bessel, Error functions

### **Advanced Computing**
- **Numerical Optimization**: Gradient descent, linear programming
- **Signal Processing**: FFT, digital filters, convolution
- **Machine Learning**: Neural networks, clustering, regression
- **Cryptography**: RSA, elliptic curves, modular arithmetic
- **Geometric Algebra**: Multivector calculus, rotations

### **Zexus-Specific Features**
- **Async Math**: Parallel computation with async/await
- **Event-Driven**: Progress tracking with event system
- **Protocol-Based**: Mathematical abstractions using protocols
- **Renderer Integration**: Function plotting and visualization

## 📦 Installation

```zexus
use "zexus-math" as math
```

🎯 Quick Start

Basic Arithmetic & Algebra

```zexus
use "zexus-math" as math

// Complex numbers
let z1 = math.complex(3, 4)
let z2 = math.complex(1, -2)
let sum = z1.add(z2)  // 4 + 2i

// Matrix operations
let A = math.matrix(2, 2, [1, 2, 3, 4])
let det = A.determinant()  // -2.0
let inv = A.inverse()      // [[-2, 1], [1.5, -0.5]]
```

Calculus & Analysis

```zexus
// Define a function
let f = math.Polynomial{coefficients: [1, -2, 1]}  // x² - 2x + 1

// Find roots
let root = math.newton_raphson(f, 0.5)  // 1.0

// Calculate derivatives
let slope = math.derivative(f, 2.0)     // 2.0

// Definite integrals
let area = math.integrate(f, 0, 1)      // ~0.333
```

Advanced Applications

```zexus
// Signal processing
let signal = [sin(2*math.PI*5*t/64) for t in range(0, 64)]
let spectrum = math.fft(signal)

// Machine learning
let clusters = math.kmeans(data_points, 3)

// Cryptography
let keys = math.generate_rsa_keys(2048)
```

Async Mathematical Computing

```zexus
action async real_time_analysis() {
    // Parallel integration
    let result = await math.parallel_integrate(f, 0, 1, 8)
    
    // Monte Carlo methods
    let mc_result = await math.monte_carlo_integrate(f, 0, 1, 100000)
    
    // Real-time signal processing
    while true {
        let spectrum = math.fft(live_signal)
        await math.sleep(0.1)
    }
}
```

📚 Modules

· core: Constants, basic utilities
· complex: Complex number system
· linalg: Linear algebra
· calculus: Differentiation, integration
· optimization: Numerical optimization
· signal: Signal processing
· diffeq: Differential equations
· ml: Machine learning
· crypto: Cryptographic mathematics
· geometric: Geometric algebra
· async: Async mathematical operations
· stats: Statistics and probability
· special: Special functions

🎨 Visualization

```zexus
// Function plotting
await math.plot_function(f, -10, 10)

// 3D surface plots
await math.plot_surface(math.lorenz_attractor)
```

🔧 Advanced Usage

Custom Mathematical Functions

```zexus
contract MyFunction implements math.MathFunction {
    action evaluate(x: float) -> float {
        return sin(x) * exp(-x*x)
    }
    
    action derivative() -> MathFunction {
        // Implement analytical derivative
        return MyFunctionDerivative{}
    }
}
```

Event-Driven Computation

```zexus
// Track convergence progress
math.on_event("convergence", action(event) {
    print("Iteration " + event.iteration + ": error=" + event.error)
})

let solution = await math.iterative_solver(f, initial_guess)
```

📈 Performance

· Optimized algorithms for numerical stability
· Async parallel computation for heavy workloads
· Memory-efficient matrix operations
· Real-time capable signal processing

🤝 Contributing

1. Follow Zexus protocol-based design patterns
2. Include async versions of computationally intensive functions
3. Add event emission for long-running operations
4. Provide comprehensive mathematical documentation
5. Include usage examples

📄 License

MIT License - Feel free to use in your Zexus projects!