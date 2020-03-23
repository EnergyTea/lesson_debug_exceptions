﻿
# Анализаторы кода

Проект использует следующие статические анализаторы: 

1. [FxCop](https://github.com/dotnet/roslyn-analyzers) - Анализаторы кода от Microsoft.
2. [StyleCop](https://github.com/DotNetAnalyzers/StyleCopAnalyzers) - Стилистический анализатор.
3. [Roslynator](https://github.com/JosefPihrt/Roslynator) - Анализатор для замещения правил, работающих только в Visual Studio.
4. [Sonar](https://github.com/SonarSource/sonar-dotnet) - Анализатор кода для определения плохих участков кода.

## Установка git-hooks для автоматической проверки изменений

Чтобы перед каждым пушем в репозиторий выполнялась проверка анализаторами кода, необходимо добавить локальные хуки в git. Это можно сделать следующим скриптом:

```bash
bash init-hooks.sh
```

## Наборы правил

1. StayStore.ruleset - Набор правил для использования в обычных проектах, содержит переопределения дефолтных настроек анализаторов.
2. StayStore.Test.ruleset - Набор правил для использования в тестовых проектах, наследует правила StayStore.ruleset и переопределяет их.