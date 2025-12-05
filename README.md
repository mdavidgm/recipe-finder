# 🍳 Recipe Finder

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://mdavidgm.github.io/recipe-finder/)
[![Test Coverage](https://img.shields.io/badge/coverage-100%25-brightgreen)]()
[![Tests](https://img.shields.io/badge/tests-passing-brightgreen)]()
[![TypeScript](https://img.shields.io/badge/TypeScript-strict-blue)]()
[![License](https://img.shields.io/badge/license-MIT-blue)]()

> A production-ready recipe search application showcasing **Test-Driven Development** best practices and 100% test coverage.

**[🚀 Live Demo](https://mdavidgm.github.io/recipe-finder/)** | **[📖 Documentation](#documentation)** | **[🧪 Testing](#testing-philosophy)**

![Recipe Finder Demo](docs/demo.gif)
*Real-time recipe search with instant results*

---

## ✨ Features

- 🔍 **Instant Search** - Real-time recipe filtering with optimized performance
- 📱 **Responsive Design** - Seamless experience across all devices
- ♿ **Accessible** - WCAG AA compliant, keyboard navigation support
- 🎨 **Modern UI** - Clean interface with smooth animations
- 🧪 **100% Test Coverage** - Every feature fully tested (unit + integration)
- ⚡ **Fast** - Optimized bundle size and runtime performance
- 🔒 **Type-Safe** - Built with TypeScript in strict mode (zero `any`)

## 🎯 Why This Project?

Initially created as a technical assessment, I've transformed it into a **showcase of professional development practices**:

- ✅ **Test-Driven Development** (tests written first)
- ✅ **Clean Architecture** (separation of concerns)
- ✅ **SOLID Principles** (maintainable, scalable code)
- ✅ **Performance optimization** (debouncing, memoization)
- ✅ **Accessibility first** (semantic HTML, ARIA)

This project demonstrates how to build **production-grade applications** with uncompromising quality standards.

---

## 🚀 Quick Start

### Prerequisites
- Node.js 16+ 
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/mdavidgm/recipe-finder.git

# Navigate to project directory
cd recipe-finder

# Install dependencies
npm install

# Start development server
npm start
```

Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

---

## 🧪 Testing Philosophy

This project follows **strict TDD methodology**. Every single line of code was written **after** writing a failing test.

### Coverage Report

```bash
npm run test-coverage
```

📊 **100% Coverage Breakdown:**
- ✅ Statements: 100%
- ✅ Branches: 100%
- ✅ Functions: 100%
- ✅ Lines: 100%

View the full HTML report at: `coverage/lcov-report/index.html`

### Test Commands

```bash
# Run all tests (watch mode)
npm test

# Run tests with coverage
npm run test-coverage

# Run tests in CI mode
npm test -- --coverage --watchAll=false
```

### Testing Stack
- **Framework:** Jest / React Testing Library
- **Approach:** Test-Driven Development (Red-Green-Refactor)
- **Types:** Unit, Integration, and Accessibility tests
- **Coverage:** 100% (not a goal, but a natural result of TDD)

### Example Test

```typescript
describe('RecipeSearch', () => {
  it('should filter recipes by search term', () => {
    render(<RecipeSearch recipes={mockRecipes} />);
    
    const searchInput = screen.getByRole('searchbox');
    fireEvent.change(searchInput, { target: { value: 'pasta' } });
    
    expect(screen.getByText('Pasta Carbonara')).toBeInTheDocument();
    expect(screen.queryByText('Chicken Curry')).not.toBeInTheDocument();
  });
});
```

---

## 🏗️ Architecture

```
src/
├── components/          # React components (atomic design)
│   ├── atoms/          # Basic building blocks
│   ├── molecules/      # Composite components  
│   └── organisms/      # Complex components
├── hooks/              # Custom React hooks
├── services/           # Business logic & API calls
├── utils/              # Helper functions
├── types/              # TypeScript definitions
└── __tests__/          # Test files (co-located)
```

### Key Design Decisions

1. **Component Architecture**
   - Atomic Design for consistency
   - Single Responsibility Principle
   - Fully typed props with TypeScript

2. **State Management**
   - React hooks for local state
   - Context for shared state
   - No unnecessary dependencies

3. **Performance**
   - Debounced search (300ms)
   - Memoized expensive computations
   - Lazy loading for images
   - Code splitting where applicable

4. **Accessibility**
   - Semantic HTML elements
   - ARIA labels and roles
   - Keyboard navigation
   - Screen reader tested

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| **Framework** | React 18 |
| **Language** | TypeScript (strict mode) |
| **Build Tool** | Create React App / Vite |
| **Testing** | Jest + React Testing Library |
| **Styling** | CSS Modules / Styled Components |
| **Linting** | ESLint + Prettier |
| **CI/CD** | GitHub Actions |
| **Deployment** | GitHub Pages |

---

## 📦 Available Scripts

### Development
```bash
npm start              # Start dev server (port 3000)
npm test               # Run tests in watch mode
npm run build          # Production build
```

### Quality Assurance
```bash
npm run test-coverage  # Generate coverage report
npm run lint           # Run ESLint
npm run type-check     # TypeScript validation
```

### Deployment
```bash
npm run deploy         # Deploy to GitHub Pages
```

---

## 🎓 What I Learned

Building this project reinforced key concepts:

1. **TDD is faster in the long run**
   - Initial investment pays off with fewer bugs
   - Refactoring becomes fearless
   - Documentation through tests

2. **100% coverage is achievable**
   - Not by forcing coverage, but by good design
   - Testable code is better code
   - Integration tests catch more bugs than unit tests alone

3. **TypeScript strict mode is worth it**
   - Catches bugs at compile time
   - Better IDE support
   - Self-documenting code

4. **Accessibility shouldn't be an afterthought**
   - Semantic HTML is easier to test
   - ARIA improves UX for everyone
   - Keyboard navigation is a feature, not a burden

---

## 🚀 Deployment

The app is automatically deployed to GitHub Pages on every push to `main`.

**Live URL:** [https://mdavidgm.github.io/recipe-finder/](https://mdavidgm.github.io/recipe-finder/)

### Build Optimization
- Minified bundle
- Tree shaking enabled
- Asset compression
- Cache-busting with hashes

---

## 🤝 Contributing

While this started as a personal project, I've open-sourced it as a **reference for TDD best practices in React**.

If you find it useful:
- ⭐ **Star** the repo
- 🐛 **Report bugs** via issues
- 💡 **Suggest improvements** via discussions
- 🔀 **Submit PRs** for enhancements

### Development Workflow
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Write tests first (TDD)
4. Implement feature
5. Ensure 100% coverage (`npm run test-coverage`)
6. Commit changes (`git commit -m 'Add amazing feature'`)
7. Push to branch (`git push origin feature/amazing-feature`)
8. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Manuel David Garcia Mateos**

- 🌐 Website: [mdavidgm.com](https://www.mdavidgm.com/en/)
- 💼 LinkedIn: [manuel-david-garcia-mateos](https://www.linkedin.com/in/manuel-david-garcia-mateos-ba5b11109/)
- 📧 Email: mdavid29021984@gmail.com
- 🐙 GitHub: [@mdavidgm](https://github.com/mdavidgm)

---

## 🙏 Acknowledgments

- Built as part of my commitment to **Test-Driven Development**
- Inspired by the philosophy that **code quality matters**
- Created to demonstrate that **100% coverage is practical, not idealistic**

---

**⚡ Built with TDD, TypeScript, and ❤️**

*If this project helped you understand TDD better, consider giving it a ⭐!*
