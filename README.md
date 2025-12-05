# 🍳 Recipe Finder - Production-Grade Food Search Engine

[![Coverage](https://img.shields.io/badge/coverage-100%25-brightgreen)]()
[![Tests](https://img.shields.io/badge/tests-passing-brightgreen)]()
[![TypeScript](https://img.shields.io/badge/TypeScript-strict-blue)]()

A fully tested, production-ready recipe search application built with TDD methodology.

## ✨ Features

- 🔍 Real-time recipe search with debouncing
- 🎨 Responsive design (mobile-first)
- ♿ WCAG AA accessible
- 🧪 100% test coverage (unit + integration)
- 📦 Zero runtime errors (TypeScript strict mode)

## 🏗️ Architecture

Built following Clean Architecture principles:
- Separation of concerns (UI, Business Logic, Data)
- Dependency injection for testability
- Repository pattern for data access

[Add architecture diagram]

## 🧪 Testing Philosophy

This project demonstrates **Test-Driven Development** at its finest:

- ✅ **100% code coverage** (not a goal, but a result of good design)
- ✅ **Tests written FIRST** (Red-Green-Refactor)
- ✅ **Integration tests** for user flows
- ✅ **Unit tests** for business logic
- ✅ **E2E tests** for critical paths
```bash
npm test              # Run all tests
npm run test:coverage # Coverage report
npm run test:watch    # TDD mode
```

## 💡 Technical Highlights

### 1. Type-Safe API Integration
```typescript
// Fully typed, zero `any`
interface Recipe {
  id: string;
  title: string;
  ingredients: Ingredient[];
}
```

### 2. Custom Hooks with Tests
```typescript
// Every hook has 100% coverage
const { recipes, loading, error } = useRecipeSearch(query);
```

### 3. Performance Optimizations
- Debounced search (300ms)
- Memoized components
- Lazy loading images

## 🚀 Tech Stack

- **Frontend:** React 18 + TypeScript
- **Testing:** Vitest + Testing Library
- **Styling:** [Your choice]
- **Build:** Vite
- **CI/CD:** [If you have it]

## 📸 Screenshots

[Add 2-3 beautiful screenshots]

## 🎓 What I Learned

Building this taught me:
- How to achieve 100% coverage without sacrificing pragmatism
- Advanced TypeScript patterns for React
- Performance optimization techniques
- [Add more insights]

## 📦 Installation

[Standard installation instructions]

## 🤝 Contributing

While this started as a technical assessment, I've open-sourced it as a reference for TDD best practices. PRs welcome!

## 📄 License

MIT

---

**Built with ❤️ and TDD by [David García](https://mdavidgm.com)**

*Part of my mission to promote test-driven development in the React community*
