## Что такое tree shaking?

**Tree shaking** - это оптимизация, используемая в сборщиках для удаления неиспользуемого кода из JavaScript-модулей, такие модули не включаются в окончательную сборку или бандл. Она работает за счёт анализа импортов и экспорта в ES6-модулях (import/export) и эффективна только при статическом анализе.